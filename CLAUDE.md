# TextDetective — Project Instructions

## Documentation Philosophy: Latest Snapshot

All design documentation in this repository must reflect the **current state** of the game design — not its history.

### Rules for maintaining design docs

- **Always refactor, never append.** When a new design decision is made or a prior one changes, update every affected section of every affected document to reflect the new design. Do not add a "changes" section or describe what used to be true.
- **Remove stale content.** Any reference to a superseded design — old mechanic names, old flow descriptions, old UI concepts — must be deleted, not annotated or struck through.
- **No delta sections.** Do not create sections like "v2 changes", "updated design", "new approach", or "revision notes". The document should read as if the current design is the only design that ever existed.
- **Cross-document consistency.** After updating any document, scan all other docs for references to the changed concept and update them to match.
- **README is the entry point.** `README.md` should always give an accurate high-level summary of the current game concept. Update it whenever the core concept or scope shifts.

### When the user describes new design

1. Identify which documents and sections are affected.
2. Rewrite those sections in place to reflect the new design.
3. Remove any content that no longer applies.
4. Ensure consistency across all docs.
5. Do not leave breadcrumbs to the prior design.

## Repository Structure

```
docs/          # Design documentation
  design.md    # Core game design document
README.md      # High-level project overview
CLAUDE.md      # This file
```
