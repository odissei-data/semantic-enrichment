# Semantic Enrichment

Static files used for semantic enrichment of CBS microdata datasets in the ODISSEI portal.

## Contents

### `alle-beschikbare-catalogus-bestanden.tsv`

A tab-separated file containing the frequency of use of CBS microdata files among
CBS Remote Access (RA) projects. It is used by the
[metadata-enhancer](https://github.com/odissei-data/metadata-enhancer) service to
enrich CBS datasets with a `frequencyOfUse` field (`high`, `medium`, or `low`).

Columns: `Bestandsnaam`, `Freq.`, `Percent`, `Cum.`, `Popularity`

## Updating

This file should be updated with each new CBS release. The source data is provided
by the ODISSEI Coordination Team as an Excel export. To update:

1. Export the frequency sheet to CSV
2. Convert to TSV with columns: `Bestandsnaam`, `Freq.`, `Percent`, `Cum.`, `Popularity`
3. Replace `alle-beschikbare-catalogus-bestanden.tsv` in this repository
4. Update `GITHUB_RAW_URL` in the metadata-enhancer `.env` if the file path changed
