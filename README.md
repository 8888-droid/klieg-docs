# Klieg Wire documentation

Bilingual product documentation for Mintlify: 22 Russian pages and 22 matching
English pages. This public repository is the source for the public docs site.

## Mintlify connection

- GitHub repository: `8888-droid/klieg-docs`.
- Documentation branch: `codex/mintlify-bilingual-docs`.
- Content root: repository root, where `docs.json` lives.
- Leave **docs.json is in a subdirectory** disabled.
- Public site: [docs.klieg.net](https://docs.klieg.net).

Install the Mintlify GitHub App with **Only select repositories** and select only
`klieg-docs`. No other repository is needed as context or as a dependency.
The public site is live. On 2026-09-08, both `/ru/introduction` and
`/en/introduction` returned HTTP 200 with a valid HTTPS certificate for
`docs.klieg.net`.

## Editing

Edit matching pages under `ru/` and `en/` together. Keep page slugs, contract
addresses, prices, pass rules, dates, and product availability consistent.
Navigation and language labels live in `docs.json`; brand assets are in
`assets/`. Every advertised price and contract status has a dated source check.
Refresh that check before changing those claims.

Public pages cover the product, user workflows, evidence, coverage, access,
contracts, FAQ, glossary, roadmap, and changelog. Do not add infrastructure,
data-provider details, storage, service operations, credentials, or internal
reports to this repository.

## Preview and validation

The site was prepared with the official `mint@4.2.876` CLI. With that CLI
available, run these commands from this repository root:

```sh
mint validate --telemetry=false
mint broken-links --telemetry=false
mint dev --no-open --telemetry=false
```

Review both languages and mobile layout before publishing. Mintlify excludes
this README from the public site by default.
