# Agent Notes

## Research Project Template Work

When editing the Quarto research project templates in this repo, keep these local rules in mind:

- Do not run `quarto render` unless the user explicitly asks. The user has a GitHub Action for render validation.
- Prefer text-only checks such as `git diff --check`, targeted `rg`, and small file inspections.
- Site navigation links are intentionally removed from the sidebar in `_quarto.yml`; keep `website.sidebar.contents: []` unless the user asks to restore site nav.
- The root `index.qmd` contains the Templates table and should link to `Templates/Research Project Components/Research Project Template.qmd`.

## Editing Pitfalls From This Checkout

- `apply_patch` may fail in this Windows sandbox with a restricted-token writable-root error. If that happens, use a very small targeted PowerShell edit and immediately inspect the diff.
- Be careful when writing multiline YAML from PowerShell. Do not accidentally write the literal text `` `r`n `` into `_quarto.yml`; inspect the affected lines after editing.
- PowerShell can mangle complex `rg` regex quoting, especially with pipes, spaces, or escaped quotes. If a combined check fails oddly, split it into simpler `rg` commands.
