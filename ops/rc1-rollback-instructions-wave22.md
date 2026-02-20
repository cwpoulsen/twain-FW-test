# RC1 Rollback Instructions — Wave 22

Date: 2026-02-19  
Purpose: safe rollback playbook if RC1 tag/review candidate must be reverted or superseded.

---

## 1) Rollback scenarios

Use this runbook when any of the following occurs after RC1 tag creation:
- Critical checklist failure discovered after tagging.
- Lock/risk regression detected in Wave 21 weekly monitor output.
- Wrong commit was tagged as RC1.
- RC1 docs require correction before external distribution.

---

## 2) Identify current and target commits

From repo root:
```bash
git log --oneline --decorate -n 20
git show rc1-wave22 --no-patch --decorate
```

Record:
- `BAD_SHA` = commit currently tagged `rc1-wave22` (or problematic head)
- `GOOD_SHA` = last known good commit to restore

---

## 3) Rollback modes

### Mode A — Retag only (preferred when code/content history is fine)
Use when branch history is correct but tag points to wrong commit.

```bash
# Move tag locally
git tag -d rc1-wave22
git tag -a rc1-wave22 <GOOD_SHA> -m "RC1 Wave22 retag to known-good snapshot"

# Verify
git show rc1-wave22 --no-patch --decorate
```

If tag already pushed and remote correction is approved:
```bash
git push origin :refs/tags/rc1-wave22
git push origin rc1-wave22
```

### Mode B — Revert offending commit(s) on main (no history rewrite)
Use when bad changes were committed and should be undone safely.

```bash
# Single commit
git revert <BAD_SHA>

# Multiple commits (newest to oldest recommended review first)
git revert <SHA1> <SHA2> <SHA3>
```

Then run readiness checks again and issue a fresh RC tag if needed.

### Mode C — Hard reset (local emergency only; destructive)
Use only for local repair before sharing; requires explicit operator intent.

```bash
git reset --hard <GOOD_SHA>
```

If remote already has bad history, coordinate separately before any force push.

---

## 4) Required post-rollback verification

After any rollback action:

1. Confirm expected commit/tag pointers:
```bash
git rev-parse HEAD
git rev-parse rc1-wave22
```

2. Confirm clean working tree:
```bash
git status --short
```

3. Re-run readiness gates:
- `ops/monitor-pack-wave21.md` command block
- `ops/reviewer-checklist-wave21.md` critical checks

4. Update/change log note:
- append correction note to `ops/rc1-changelog-slice-recent-waves-wave22.md`
- include date, reason, and old/new commit IDs

---

## 5) Communication template (internal)

```text
RC1 rollback executed.
Reason: <brief reason>
Previous tag commit: <BAD_SHA>
Restored commit: <GOOD_SHA>
Verification: monitor/checklist rerun <PASS|FAIL>
Next action: <retag / additional fixes / hold>
```

---

## 6) Safety notes

- Prefer **revert** or **retag** over history rewrite.
- Do not force-push branch history unless explicitly coordinated.
- Keep rollback auditable: record SHAs, commands run, and verification evidence paths.
