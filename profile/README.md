# DocSpec

**Open document conversion for sovereign collaboration.**

DocSpec is a document specification and conversion system built around a JSON-based Abstract Syntax Tree (AST). It transforms legacy document formats into accessible, reusable content for modern editors.

```
┏━━━━━━┓                                               ┌──────┐
┃ DOCX ┃ ─────────┐                              ┌───➤ │ DOCX │
┗━━━━━━┛          │                              │     └──────┘
┌──────┐          │                              │     ┏━━━━━━┓
│ HTML │ ─────────┤                              ├───➤ ┃ HTML ┃
└──────┘          │                              │     ┗━━━━━━┛
┏━━━━━━━━┓        │                              │     ┏━━━━━━━━┓
┃ Tiptap ┃ ───────┤                              ├───➤ ┃ Tiptap ┃
┗━━━━━━━━┛        │      ┏━━━━━━━━━━━━━━━━━┓     │     ┗━━━━━━━━┛
┌───────────┐     │      ┃ DocSpec         ┃     │     ┏━━━━━━━━━━━┓
│ BlockNote │ ────┼────➤ ┃ Abstract Syntax ┃ ────┼───➤ ┃ BlockNote ┃
└───────────┘     │      ┃ Tree (AST)      ┃     │     ┗━━━━━━━━━━━┛
┌──────────┐      │      ┗━━━━━━━━━━━━━━━━━┛     │     ┌──────────┐
│ Markdown │ ─────┤                              ├───➤ │ Markdown │
└──────────┘      │                              │     └──────────┘
┌─────┐           │                              │     ┌─────┐
│ ODT │ ──────────┤                              ├───➤ │ ODT │
└─────┘           │                              │     └─────┘
┏━━━━━┓           │                              │     ┌───────────────┐
┃ PDF ┃ ──────────┘                              ├───➤ │ Typst and PDF │
┗━━━━━┛                                          │     └───────────────┘
                                                 │     ┏━━━━━━┓
                                                 └───➤ ┃ EPUB ┃
 Legend:                                               ┗━━━━━━┛
┏━━━━━━━━━━━━━┓ ┌────────────────────────┐
┃ Implemented ┃ │ Implementation planned │
┗━━━━━━━━━━━━━┛ └────────────────────────┘
```

## Features

- **Universal AST** with [TypeSpec](https://github.com/docspec/docspec) specification for document interchange
- **Import** from DOCX, Tiptap
- **Export** to HTML, EPUB, BlockNote, and Tiptap
- **Accessibility-first** with real-time WCAG validation

## In Production

DocSpec powers document import for [La Suite Docs](https://github.com/suitenumerique/docs), part of the Franco-German-Dutch sovereign collaboration stack under [DC-EDIC](https://digital-decade-dgs.ec.europa.eu/edic/dc-edic).

## Links

- [Contributing](https://github.com/docspec/.github/blob/main/CONTRIBUTING.md)

## License

[EUPL-1.2](https://eupl.eu/), MIT
