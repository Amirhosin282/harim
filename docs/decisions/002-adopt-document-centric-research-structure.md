# ADR-002: Adopt a Document-Centric Research Structure

- **Status:** Accepted
- **Date:** 2026-07-26
- **Authors:** Amirhossein Asadpour

---

## Context

In the early stages of Harim, research topics were stored as standalone Markdown files under the `research/topics` directory.

As the project evolved, it became clear that research documents should become the project's primary source of knowledge rather than Telegram posts or repository notes.

The previous structure was not suitable for managing multiple document formats, translations, attachments, and future supporting materials within a single research topic.

---

## Decision

Starting from this decision, every research topic SHALL be stored inside its own dedicated directory.

Each research directory represents a single research publication and MAY contain:

- The official Persian document (`*-fa.docx`)
- An English translation (`*-en.docx`) *(optional)*
- A Markdown version for GitHub (`README.md`)
- An English Markdown version (`README-en.md`) *(optional)*
- Attachments, figures, media, or supplementary files

Example:

```text
research/
└── 001-sextortion/
    ├── sextortion-fa.docx
    ├── sextortion-en.docx
    ├── README.md
    ├── README-en.md
    └── attachments/
```

---

## Primary Source

The Persian document (`*-fa.docx`) is considered the official and authoritative version of every research publication.

Markdown documents are intended for online reading on GitHub and are not considered the primary publication format.

Translations are derived from the official Persian document.

Public-facing content—including Telegram posts, website articles, infographics, and future educational material—SHOULD be produced from the official research document rather than written independently.

---

## Rationale

This structure provides a clear separation between research, documentation, and public communication.

It also allows each research topic to grow independently without affecting the overall repository layout.

Benefits include:

- Self-contained research topics.
- Better organization of related assets.
- Support for multilingual publications.
- Easier long-term maintenance.
- A scalable repository structure.
- Clear distinction between official documents and presentation formats.

---

## Consequences

### Positive

- Every research topic becomes an independent publication.
- Related files remain together.
- GitHub provides a readable version through Markdown.
- Future translations fit naturally into the structure.
- Public content always references a documented source.

### Negative

- More directories will exist inside the repository.
- Multiple document formats require synchronization.
- Preparing each publication requires additional effort.

---

## Alternatives Considered

### Standalone Markdown files

Using individual Markdown files for each research topic was considered.

This approach becomes difficult to maintain once translations, attachments, or additional publication formats are introduced.

### Language-based directory structure

Organizing documents into separate language folders (for example `fa/` and `en/`) was also considered.

This approach separates files that belong to the same publication and complicates long-term maintenance.

---

## Notes

Research publications are intended to be permanent references.

Once published, documents should generally remain unchanged except for factual corrections or formatting issues.

Major revisions SHOULD be published as new research documents rather than replacing previous publications.

---

## References

None.

---

**This decision is part of Harim's official project architecture until superseded by a future ADR.**
