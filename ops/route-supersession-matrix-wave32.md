# Route Supersession Matrix — Wave 32

Date: 2026-02-20  
Companion to: `ops/route-map-single-page-wave31.md`, `ops/metadata-hygiene-audit-wave30.md`, `ops/strategy-control-log.md` (latest entry first).  
Scope: review-routing docs from Waves 20–31 only; classify current role as **primary / supporting / legacy / superseded**.

## Status matrix

| Wave | Document | Status | Rationale | Recommended archive path (legacy only) |
|---|---|---|---|---|
| 20 | `ops/executive-summary-wave20.md` | supporting | Still referenced as status baseline from active routes; no supersession marker. | — |
| 20 | `ops/archive-index-wave20.md` | supporting | Still used as broad catalog pointer from active review routes. | — |
| 21 | `ops/reviewer-checklist-wave21.md` | primary | Explicitly marked as primary go/no-go gate and still used in active decision flow. | — |
| 23 | `ops/handoff-briefing-wave23.md` | primary | Explicitly marked as primary action-queue route and still linked by active docs. | — |
| 24 | `ops/doc-map-dedupe-wave24.md` | supporting | Active dedupe/ownership reference used by consolidation and routing docs. | — |
| 25 | `ops/decision-queue-wave25.md` | supporting | Upstream analysis backlog feeding decision surfaces; not primary answer form. | — |
| 25 | `ops/doc-merge-plan-wave25.md` | supporting | Execution-plan dependency for supersession/routing prep; still referenced. | — |
| 26 | `ops/unresolved-decisions-brief-wave26.md` | legacy | Decision-call surface replaced by later packet/template chain (W29→W30→W31/W32), but still useful as rationale context. | `ops/archive/review-routing-legacy/unresolved-decisions-brief-wave26.md` |
| 26 | `ops/supersession-finalize-wave26.md` | supporting | Still active as supersession control reference for routing consolidation docs. | — |
| 27 | `ops/decision-ballot-pack-wave27.md` | supporting | Input/support artifact for later decision packet forms; not the current top-level answer surface. | — |
| 27 | `ops/doc-routing-prune-wave27.md` | supporting | Route-lock implementation record still referenced by route-map and consolidation docs. | — |
| 28 | `ops/decision-signoff-tracker-wave28.md` | superseded | Explicitly superseded by `ops/decision-ready-packet-wave30.md`. | — |
| 28 | `ops/routing-consolidation-wave28.md` | supporting | Consolidation summary remains active support to route-map and prune lock docs. | — |
| 29 | `ops/decision-resolution-sheet-wave29.md` | superseded | Explicitly superseded by W30 packet and later W31 template. | — |
| 29 | `ops/routing-archive-prep-wave29.md` | supporting | Current non-destructive archive-prep control doc; no direct superseding replacement in scope. | — |
| 30 | `ops/decision-ready-packet-wave30.md` | primary | One-pass decision form and current structured decision surface feeding W31/W32 quick-answer layers. | — |
| 30 | `ops/metadata-hygiene-audit-wave30.md` | supporting | Header/supersession hygiene reference for routing governance. | — |
| 31 | `ops/decision-answers-template-wave31.md` | superseded | Explicitly superseded by `ops/decision-quickfill-card-wave32.md`. | — |
| 31 | `ops/route-map-single-page-wave31.md` | primary | Current one-page routing map defining active review entry surfaces. | — |

## Consolidated notes

- **Current primary review-routing surfaces (within W20–W31 set):**  
  `ops/reviewer-checklist-wave21.md`, `ops/handoff-briefing-wave23.md`, `ops/decision-ready-packet-wave30.md`, `ops/route-map-single-page-wave31.md`.
- **Explicitly superseded chain in decision routing:**  
  `unresolved-decisions-brief-wave26.md` → `decision-resolution-sheet-wave29.md` → `decision-ready-packet-wave30.md` → `decision-answers-template-wave31.md` (now superseded by W32 quickfill card).
- **Legacy recommendation executed as path-only (non-destructive):**  
  `ops/unresolved-decisions-brief-wave26.md` is the only W20–W31 review-routing doc recommended for archive move at this stage.
