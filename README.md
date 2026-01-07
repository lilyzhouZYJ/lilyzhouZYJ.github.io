# lilyzhouzyj.github.io

This repo contains my personal website, build with [Hugo](https://gohugo.io).

## Getting started

### Requirements

To install Hugo, follow the official installation guide.

### Run the site locally

To run the site, use the following command:

```bash
hugo server -D
```

Then open `http://localhost:1313` in your browser.

`-D` includes draft content. Omit it to serve only published content:

```bash
hugo server
```

### Build the static site

To generate the production-ready static files into the `public/` directory, run below:

```bash
hugo
```

The contents of `public/` can be deployed directly (for example, via GitHub Pages).

