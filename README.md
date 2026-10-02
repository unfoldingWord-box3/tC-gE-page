# Verse Explorer

A read-only, donor-facing page for exploring the translation resources behind favorite Bible passages. It works somewhat like gateway-edit: original language (UGNT / UHB), ULT, UST, Translation Notes, Translation Words, Translation Academy, and Translation Questions, all shown for one passage at a time.

**Status: design preview.** Open `index.html` in a browser. It needs no build step and has no dependencies besides Google Fonts.

## What it does
- A favorites rail lets people pick a passage. A passage can be one verse or a range, such as Psalm 23:1–2. Deep links work: `index.html#psalm-23-1-2`.
- Alignment: hover or select an original-language word to highlight the matching ULT words, and the reverse. Selecting a word shows its lemma, Strong's number, grammar, and a link to its Translation Words article.
- Hover a translation note to highlight its quote in both the original text and the ULT.
- Note tags link to their Translation Academy article.

## Branding
Styled to the unfoldingWord Brand Guidelines (2022):
- **Colors:** Tech `#231F20`, Ocean `#014263`, Inspire `#31ADE3` (primary), Cultivate `#70C9CC`, Kindle `#E59D33`, plus 20% tints. The page follows the guide's color-contrast chart.
- **Type:** Avenir Black for headings and Avenir Book for body text. Figtree substitutes where Avenir isn't installed. PT Serif is used for the English scripture text and other long-form reading.
- **Supporting elements:** grainy brand gradients, angled opacity layers, and the brand mark used as a large, cropped design element.
- **Logo:** the mark and wordmark in `index.html` are temporary recreations. Replace the `#uw-mark` symbol and `.logo` wordmark with the official SVGs from the brand library.

## Data
The scripture and resource text in `index.html` is sample content written for the design review. The `PASSAGES`, `TW`, and `TA` objects are shaped after the Door43 sources (USFM with `\zaln` alignments, `tn_*.tsv`, `twl_*.tsv`, `tq_*.tsv`, and the tW/tA markdown), so a loader can fill them from git.door43.org at build time or at runtime.
