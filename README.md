# adt-catalog

Remote catalog for [adt](https://github.com/saketananddotme/ai-dev-toolkit) — the AI skill package manager.

This repo provides a list of curated skill sources that `adt` fetches automatically (cached for 24h). 

## How it works

`adt` merges this catalog with its built-in sources and any user-added sources. The raw `catalog.json` is fetched from:

```
https://raw.githubusercontent.com/saketananddotme/adt-catalog/main/catalog.json
```

## Adding a source to the catalog

Open a PR adding an entry to `catalog.json`:

```json
{
  "sources": {
    "your-name": {
      "repo": "https://github.com/you/your-skills.git",
      "label": "Your Name — Short description",
      "ref": "main"
    }
  }
}
```

The repo must follow the [adt source layout](https://github.com/saketananddotme/ai-dev-toolkit#how-source-repos-are-structured): `skills/`, `agents/`, `rules/`, `hooks/`, or `CLAUDE.md` at the repo root.
