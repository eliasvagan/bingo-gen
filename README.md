# Bingo generator

Browser-based wedding bingo sheet generator. Creates randomized, unique cards and downloads them as PDFs.

**Live:** [eliasv.com/projects/bingo-gen/](https://eliasv.com/projects/bingo-gen/) (deployed from `master` by the eliasv.com orchestrator, see [eliasvagan/eliasv_com](https://github.com/eliasvagan/eliasv_com))

## Development

Static files only — serve locally:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Layout

```
.
├── index.html
└── resources/fonts/
    ├── Eyesome-Script.otf              # PDF heading (script)
    ├── CormorantGaramond-Regular.ttf   # PDF subtitle (serif, SIL OFL)
    └── OFL-CormorantGaramond.txt
```

PDF board titles are rasterized with the canvas API (transparent PNG). Heading
uses Eyesome Script; subtitle uses Cormorant Garamond. Faces must cover every
character in the templates — browsers fall back *per glyph*, which looks like
a mixed font family.
