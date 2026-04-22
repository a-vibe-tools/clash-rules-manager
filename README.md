# Clash Rules Manager

A lightweight browser-based editor for generating Clash rule snippets. Enter rule values by type, choose a target policy group, and the app keeps the YAML configuration in sync.

## Features

- Supports `DOMAIN-KEYWORD`, `DOMAIN-SUFFIX`, `PROCESS-NAME`, and `PROCESS-NAME-REGEX` rules.
- Generates Clash-compatible YAML with `prepend`, `append`, and `delete` sections.
- Keeps the rule inputs and YAML editor synchronized in both directions.
- Extracts the target policy group from pasted YAML rules.
- Sorts and formats rule inputs alphabetically.
- Copies generated YAML to the clipboard.
- Pastes YAML from the clipboard or by global paste detection when no input is focused.
- Stores the latest configuration in `localStorage`.
- Provides YAML syntax highlighting through Shiki.

## Usage

Open `index.html` in a browser. The app is fully static and uses CDN-hosted React, Babel, Tailwind CSS, and Shiki.

1. Enter rule values in the rule cards, one value per line.
2. Set the target policy group, such as `Proxies`.
3. Review or edit the generated YAML in the editor.
4. Use **Format** to sort and clean the rule inputs.
5. Use **Copy** to copy the YAML configuration.
6. Use **Paste Config** or paste a YAML snippet on the page to import an existing configuration.

## YAML Output

The app generates rules in this shape:

```yaml
prepend:
  - 'DOMAIN-KEYWORD,chatgpt,Proxies'
  - 'DOMAIN-SUFFIX,chatgpt.com,Proxies'
append: []
delete: []
```
