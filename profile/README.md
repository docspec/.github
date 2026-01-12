# DocSpec

**Open document conversion for sovereign collaboration.**

DocSpec is a document specification and conversion system built around a JSON-based Abstract Syntax Tree (AST). It transforms legacy document formats into accessible, reusable content for modern editors.

```
                                       ┌─ HTML
                                       ├─ EPUB
         DOCX ──▶  DocSpec AST  ───────├─ BlockNote
                      (JSON)           └─ Tiptap
```

## Features

- **Universal AST** with [TypeSpec](https://github.com/docspec/docspec) specification for document interchange
- **Import** from DOCX
- **Export** to HTML, EPUB, BlockNote, and Tiptap
- **Accessibility-first** with real-time WCAG validation

## Planned Formats

| Format   | Import | Export |
| -------- | ------ | ------ |
| ODT      | ✓      | ✓      |
| Markdown | ✓      | ✓      |
| Typst    |        | ✓      |

## In Production

DocSpec powers document import for [La Suite Docs](https://github.com/suitenumerique/docs), part of the Franco-German-Dutch sovereign collaboration stack under [DC-EDIC](https://digital-decade-dgs.ec.europa.eu/edic/dc-edic).

## Repositories

| Repository                                    | Description                           |
| --------------------------------------------- | ------------------------------------- |
| [docspec](https://github.com/docspec/docspec) | AST specification and TypeSpec schema |
| [api](https://github.com/docspec/api)         | Conversion API service                |

## Links

- [Contributing](https://github.com/docspec/.github/blob/main/CONTRIBUTING.md)

## License

[EUPL-1.2](https://eupl.eu/)
