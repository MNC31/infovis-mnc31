---
title: 'AI: Personal or "Personal" data'
emoji: 🔎
colorFrom: blue
colorTo: indigo
sdk: static
pinned: false
---

# AI: Personal or "Personal" data

A browser-only Hugging Face Static Space that explores labeled PII categories in an embedded, source-derived snapshot associated with [`raayraay/privacyleak-pii`](https://huggingface.co/datasets/raayraay/privacyleak-pii).

## What it does

- Shows snapshot-level counts for rows, forget-set membership, context types, and labeled PII categories.
- Lets visitors filter the primary distribution chart by context type, locale, forget-set membership, and PII category.
- Includes a stacked-bar comparison of labeled PII spans across all PII categories. The chart separates rows marked in `inforgetset` from rows not marked in that dataset field.
- Provides abbreviated sample-ID prefixes and category labels without reproducing record text.
- Includes keyboard-operable controls, visible focus styles, responsive layouts, reduced-motion support, and explicit loaded/unavailable states.

## Data and interpretation

The page is a **static embedded snapshot**, not a live query of Hugging Face or any other service. It contains only source-derived label summaries: abbreviated sample IDs, context type, locale, canary marker, forget-set marker, and PII category labels. It intentionally excludes source record text.

The dataset describes the values as synthetic canaries. The visualization must not be read as evidence of real-world personal-data exposure, a model having trained on a record, a successful data deletion, or a successful unlearning procedure.

The comparison chart uses the label “retained” only as visual shorthand for rows **not marked in the supplied `inforgetset` field**. It does not measure retained model knowledge, prove that a model remembers a record, or establish that a deletion or unlearning method failed. Conversely, a forget-set marker is a dataset-membership label—not evidence that any model has forgotten the row.

## Run locally

No installation, build process, package manager, backend, environment variables, or Python runtime is required. Open `index.html` in a modern browser, or serve the directory with any static-file server if you prefer.

## Deployment

This repository is configured as a Hugging Face Static Space through the `sdk: static` metadata above. The Space serves `index.html` directly.

## Attribution

Dataset source: [`raayraay/privacyleak-pii`](https://huggingface.co/datasets/raayraay/privacyleak-pii) on Hugging Face.

The original artifact identifies these public viewer fields: `text`, `piispans`, `contexttype`, `locale`, `iscanary`, `sampleid`, and `inforgetset`.
