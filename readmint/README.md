# Readmint setup

The profile README is rendered by the [Readmint](https://github.com/MrLarkyy/Readmint) Action (`.github/workflows/readmint.yml`, pinned to `v0.5.1`) from the designs in `designs/year-ring/`, listed in the render manifest `designs/year-ring/renders.json` (every entry is rendered light and dark). The generated SVGs (`header.svg`, `header.dark.svg`, ...) are committed here by the workflow; do not edit them by hand.

- **Texts**: everything personal is in `designs/year-ring/settings.json` (intro, index rows, "Shipped for", footer contact). Edit it and push; the workflow runs again.
- **Token**: the workflow reads the repository secret `PROFILE` (Settings, Secrets and variables, Actions). It is a personal access token of the profile owner; with it private contributions are counted in the ring and the totals (no private repository name is ever drawn). Without a token that can read them the sections show a plain fallback line. The token is never written to a file or a log.
- **Repository cards**: the six cards show the pinned repositories in pin order; the links in `README.md` must follow the same order.
- **Update**: raise the tag in `readmint.yml` to a newer Readmint release and replace `designs/year-ring/` with the template of that release.
