# volkm.github.io

Personal academic website of Matthias Volk: https://volkm.github.io

Built with [al-folio](https://github.com/alshedivat/al-folio), a Jekyll starter for academic websites.

## Local development

```bash
docker compose up
```

Then open http://localhost:8080. See [docs/INSTALL.md](docs/INSTALL.md) for non-Docker setup.

## Updating content

Edit `_pages/`, `_bibliography/papers.bib`, `_research/`, `_tools/`, `_data/`, or `assets/img/` and push to
`master` — the `deploy.yml` GitHub Action rebuilds and republishes the site automatically.

## Updating al-folio itself

Since `v1.x`, al-folio is a thin starter: the theme runtime ships as pinned `al_*` gems in the `Gemfile`,
not as files in this repo. To pick up upstream fixes/features:

```bash
bundle update                              # bump the al_* gem versions in Gemfile.lock
bundle exec al-folio upgrade audit         # check for breaking/deprecated patterns
bundle exec al-folio upgrade apply --safe  # apply deterministic codemods, if any
bundle exec al-folio upgrade report        # writes al-folio-upgrade-report.md
```

Fix any **blocking** findings from the report, then rebuild locally (`docker compose up --build`) and check
every page before pushing.

This site keeps one intentional local override — `_layouts/bib.liquid` (renames the "Supp" button to
"Artifact") — tracked in `.al-folio-overrides.yml`. After a gem update, check whether it drifted from
upstream:

```bash
bundle exec al-folio upgrade overrides audit
bundle exec al-folio upgrade overrides diff _layouts/bib.liquid
bundle exec al-folio upgrade overrides accept _layouts/bib.liquid  # after reviewing the diff
```

See [docs/INSTALL.md](docs/INSTALL.md#upgrading-from-a-previous-version) for the full upgrade workflow.
