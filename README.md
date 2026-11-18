# Purge screenshots

Before and after screenshots for [Purge](https://github.com/jithin-sabu/purge-app) pull requests. Nothing here is needed to build Purge, so the app repo stays small to clone (#403).

## Layout

- `<issue>/<name>-before-dark.webp` and `<issue>/<name>-after-dark.webp`: shots for the PR that fixes that issue.
- `misc/<branch>/`: shots for a PR with no issue.
- `legacy/`: the 991 PNGs that lived in `docs/screenshots/` in the app repo until #403.

## Adding shots

From a purge-app checkout:

```
scripts/publish-screenshots.sh <issue> before-dark.png after-dark.png
```

The script converts the PNGs to WebP, commits them here, pushes, and prints Markdown links pinned to the commit. Paste those into the PR description. Files are never overwritten or deleted, because merged PRs link to them.
