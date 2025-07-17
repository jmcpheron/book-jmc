# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Quarto book project documenting the design and development of a 3D-printed flow-restriction filter cap for the AeroPress XL coffee maker. The book combines technical documentation, brewing science, and open-source hardware principles.

## Development Commands

### Preview the book locally
```bash
quarto preview
```

### Build the book
```bash
quarto render
```

### Build specific formats
```bash
quarto render --to html
quarto render --to pdf
```

## Project Structure

The book uses Quarto's standard book structure:
- `_quarto.yml` - Main configuration file defining book metadata, chapter order, and output formats
- `index.qmd` - Book homepage/preface
- `01-*.qmd` through `07-*.qmd` - Individual chapters covering the design process
- `references.bib` - Bibliography for citations
- `images/` - Directory for book images and diagrams
- `.github/workflows/publish.yml` - Automated GitHub Pages deployment

## Writing Guidelines

When editing chapters:
- Use standard Markdown with Quarto extensions
- Place images in the `images/` directory
- Use citations from `references.bib` with `[@key]` syntax
- Keep technical content accessible to makers and coffee enthusiasts
- Include code blocks for OpenSCAD designs and 3D printer settings

## GitHub Pages Deployment

The book automatically publishes to GitHub Pages on push to main branch. The workflow:
1. Renders all formats using latest Quarto
2. Uploads the `_book/` directory as an artifact
3. Deploys to GitHub Pages environment

Ensure GitHub Pages is enabled in repository settings with source set to "GitHub Actions".