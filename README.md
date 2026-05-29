# MiloStudio Index

Pre-built metadata index for [Milovana](https://milovana.com) EOS teases, used by [MiloStudio](https://github.com/milo-studio/MiloStudio).

This repository contains **metadata only** -- titles, authors, tags, ratings, and technical enrichment data (page counts, playtime estimates, capability flags). No tease scripts, story text, images, or media files are stored here.

## Structure

- `teases/` -- One JSON file per tease, sharded by ID (e.g., `teases/012/12345.json`)
- `manifest.json` -- All teases: ID to last-modified timestamp mapping
- `eos-manifest.json` -- EOS teases only
- `full-index.json.gz` -- Compressed archive of all teases
- `eos-index.json.gz` -- Compressed archive of EOS teases only

## Usage

MiloStudio clients sync from this repository automatically. Other developers building Milovana tools can use the JSON files or compressed archives directly.

## Updates

A GitHub Action runs the `milostudio-cli scrape` command daily at 04:00 UTC. Manual runs can be triggered via workflow dispatch.
