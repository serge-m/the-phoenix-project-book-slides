# The Phoenix Project book presentation

This repository contains a Slidev presentation based on the short narrative in `short_version1.md`, with one illustrated scene for each numbered paragraph.

## Requirements

- Node.js and npm
- Dependencies installed with `npm install`
- Chromium available through the installed `playwright-chromium` package for PDF export
- Ghostscript (`gs`) is optional and is used to compress the exported PDF

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
