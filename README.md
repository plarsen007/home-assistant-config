# Home Assistant Configuration

This repository stores my Home Assistant configuration in a clean, repeatable, Git-backed structure.

## Repository structure

- `configuration.yaml` — main HA configuration entrypoint
- `automations.yaml` — automation definitions
- `scripts.yaml` — script definitions
- `scenes.yaml` — scene definitions
- `groups.yaml` — grouping definitions
- `customize.yaml` — per-entity customization
- `packages/` — modular package files for logical grouping
- `custom_components/` — any custom components or local code

## Best practices used here

- Secrets are kept out of Git via `.secrets.yaml`
- Runtime data such as `.storage/` and databases are ignored
- Modular package configuration keeps the config maintainable
- `configuration.yaml` uses `!include` patterns to keep files organized

## Recommended Home Assistant setup

1. Copy this repo to your Home Assistant machine or use it as a version-controlled source.
2. Create `.secrets.yaml` locally if needed.
3. Adjust `configuration.yaml` with your actual includes and integrations.
4. Validate configuration in Home Assistant before restarting.

## Example secrets file

Create a local file named `.secrets.yaml` that is not committed to Git:

```yaml
wifi_ssid: "Your Wi-Fi SSID"
wifi_password: "Your Wi-Fi password"
```

Then reference it from your YAML files as needed.

## Notes

- This repo intentionally does not include runtime-generated files.
- Keep credentials, tokens, and private network details out of version control.
