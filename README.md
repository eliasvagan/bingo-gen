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
    ├── GreatVibes-Regular.ttf   # SIL OFL script face (full Latin + digits + æøå)
    └── OFL-GreatVibes.txt
```

PDF board titles are rasterized with the canvas API using that font. The face
must cover every character you put in the heading template — browsers fall
back *per glyph*, which looks like a mixed font family (e.g. one letter in
Georgia, the rest in script).