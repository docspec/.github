# DocSpec

**Streaming document conversion for sovereign collaboration.**

Documents, as they flow. DocSpec converts between document formats as a stream of
typed events — one event at a time, in constant memory, never buffering the whole
document. Built in Rust, from the same discipline end to end.

**Funded by** [NLnet](https://nlnet.nl) through the [NGI0 Commons Fund](https://nlnet.nl/commonsfund/), and the Netherlands' [Ministry of the Interior and Kingdom Relations](https://www.rijksoverheid.nl/ministeries/ministerie-van-binnenlandse-zaken-en-koninkrijksrelaties).

<p>
  <a href="https://nlnet.nl"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/docspec/.github/main/assets/nlnet-banner-card.svg"><img src="https://raw.githubusercontent.com/docspec/.github/main/assets/nlnet-banner.svg" alt="NLnet" height="40"></picture></a>
  &nbsp;&nbsp;
  <a href="https://nlnet.nl/commonsfund/"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/docspec/.github/main/assets/ngi0-commons-card.svg"><img src="https://raw.githubusercontent.com/docspec/.github/main/assets/ngi0-commons.svg" alt="NGI0 Commons Fund" height="40"></picture></a>
  &nbsp;&nbsp;
  <a href="https://www.rijksoverheid.nl/ministeries/ministerie-van-binnenlandse-zaken-en-koninkrijksrelaties"><img src="https://github.com/docspec/.github/raw/main/assets/minbzk.jpg" alt="Ministerie van Binnenlandse Zaken en Koninkrijksrelaties" height="40"></a>
</p>

**Used by** [DINUM — La Suite Numérique](https://lasuite.numerique.gouv.fr).

<p>
  <a href="https://lasuite.numerique.gouv.fr"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/docspec/.github/main/assets/dinum-gouv-card.svg"><img src="https://raw.githubusercontent.com/docspec/.github/main/assets/dinum-gouv.svg" alt="Gouvernement" height="36"></picture></a>
  &nbsp;&nbsp;
  <a href="https://lasuite.numerique.gouv.fr"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/docspec/.github/main/assets/lasuite-card.svg"><img src="https://raw.githubusercontent.com/docspec/.github/main/assets/lasuite.svg" alt="La Suite Numérique" height="36"></picture></a>
</p>

## Pipeline

Any reader feeds any writer; the event stream is the only contract between them.

## What works today

- **Reads** DOCX, HTML, Markdown
- **Writes** HTML, Markdown, BlockNote JSON, oxa.dev JSON, Pandoc native
- **HTTP API** — a streaming conversion server, available now: `docspec http`, or the `ghcr.io/docspec/api` image
- **Constant memory** — documents stream through event by event, whatever their size

Planned: ODT, PDF, Typst, EPUB, and Tiptap.

## In production

DocSpec powers document import for [La Suite Docs](https://github.com/suitenumerique/docs),
part of the Franco-German-Dutch sovereign collaboration stack under
[DC-EDIC](https://digital-decade-dgs.ec.europa.eu/edic/dc-edic).

## Repositories

- [docspec/docspec](https://github.com/docspec/docspec) — the Rust workspace: libraries, the CLI, and the HTTP server

## Links

- [Contributing](https://github.com/docspec/.github/blob/main/CONTRIBUTING.md)
- [NLdoc — the original in Elixir](https://gitlab.com/logius/nldoc)

## License

[MIT](https://github.com/docspec/docspec/blob/main/LICENSE)

## Thanks

This work grew out of the mentoring and support of
[@virgile-dev](https://github.com/virgile-dev).
