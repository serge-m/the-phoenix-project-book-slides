# The Phoenix Project book presentation

This repository contains a Slidev presentation based on the short narrative in `short_version1.md`, with one illustrated scene for each numbered paragraph.

## Requirements

- Node.js and npm
- Dependencies installed with `npm install`
- Chromium available through the installed `playwright-chromium` package for PDF export
- Ghostscript (`gs`) is optional and is used to compress the exported PDF
- FFmpeg is optional and is used to create presentation JPEGs while preserving the original PNGs

## Create optimized presentation images

The original PNG illustrations are kept in `public/images/`. To create high-quality JPEG copies for faster browser and PDF rendering:

```sh
mkdir -p public/images/jpeg
for src in public/images/paragraph-*.png; do
  base=${src%.png}
  ffmpeg -loglevel error -y -i "$src" -frames:v 1 -q:v 8 -pix_fmt yuvj444p \
    "public/images/jpeg/$(basename "$base").jpg"
done
```

The `-q:v 8` setting balances readable slide text with substantially smaller assets.

The presentation references `public/images/jpeg/`; the PNG originals are never overwritten or deleted.

Both the browser presentation and the exported PDF use these JPEG copies. The current `q:v 8` compression keeps the 1672×941 illustrations sharp enough for slide text while reducing the complete PDF to approximately 6.7 MB. The original PNG assets remain available for future regeneration or higher-quality exports.

## Render the HTML presentation

```sh
npm install
npm run build
```

The static HTML presentation is generated in `dist/`. Open or serve `dist/index.html` with a static web server.

## Render the PDF presentation

```sh
npx slidev export --output dist/the-phoenix-project.pdf
```

The PDF is written to `dist/`, which is ignored by Git. Source images in `public/images/` are not modified.

## Compress the PDF

To create a smaller PDF while keeping the source images unchanged:

```sh
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dNOPAUSE -dBATCH -dSAFER \
  -dDownsampleColorImages=true -dColorImageResolution=180 \
  -dGrayImageResolution=180 -dMonoImageResolution=240 \
  -dAutoFilterColorImages=false -dColorImageFilter=/DCTEncode \
  -dJPEGQ=82 -sOutputFile=dist/the-phoenix-project-compressed.pdf \
  dist/the-phoenix-project.pdf
```

Generated PDFs and the Slidev HTML build remain in `dist/` and are intentionally not committed.
