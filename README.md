# Bingo generator

Browser-based wedding bingo sheet generator. Creates randomized, unique cards and downloads them as PDFs.

**Live:** [eliasvagan.github.io/projects/bingo-gen/](https://eliasvagan.github.io/projects/bingo-gen/)

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
└── resources/fonts/   # Decorative heading font for PDF output only
```