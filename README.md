# dg-versions

Latest released version of each DG script. The scripts read their file on server start (and every
few hours) and print a console message when the server runs an older version. Cfx.re has no public
API for escrowed asset versions, so this public repo is the source of truth.

## Releasing an update

1. Bump `version` in the script's `fxmanifest.lua`.
2. Upload the new version to the Cfx portal.
3. Update the script's file here with the same version and what changed:

```json
{
  "version": "1.1.0",
  "changes": ["Shop logos", "Theme setting in config/main.lua"]
}
```

Servers see the message within a few hours, or straight away on their next restart.

## Files

| File | Script |
| --- | --- |
| `dg-shops.json` | dg-shops |
