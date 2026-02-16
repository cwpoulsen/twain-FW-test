# Dialogue Engine v1 (Character-Actor Harness)

## Principle
Dialogue is generated as interaction among character agents with distinct cognition, not a single blended narrator voice.

## Runtime Loop
1. Load scene packet + relevant canon/timeline constraints.
2. Load participant character-agent profiles.
3. For each turn, generate per-character:
   - intent
   - spoken line
   - subtext
   - emotional shift
4. Run Twain audit pass:
   - tone fit (Chris preferences)
   - character distinctness
   - continuity/canon checks
   - pacing and tension quality
5. Re-prompt weak turns until pass criteria met.
6. Produce clean dialogue draft + optional annotation layer.

## Non-Negotiables
- No caricature accents.
- Distinct voice through cognition + rhythm, not gimmick spelling.
- Every exchange must move power, information, or emotion.
- Preserve plausible emotional continuity across turns.

## Output Modes
- Clean script mode (reader-facing)
- Annotated mode (intent/subtext visible for editing)
