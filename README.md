# Login banner & prompt (Ansible)

A [labdex](https://github.com/reykimedev/labdex) plugin. Deploys the inventory's login banner and zone-coloured prompt to hosts over SSH. Plan = ansible --check --diff, apply = the real run.

**Version** 1.0 · **Works with** labdex >=1.3,<2 · **Plugin id** `motd`

> [!WARNING]
> Built with AI, for home labs only: labdex and its plugins were written largely with an AI
> coding assistant (Claude), directed and reviewed by a human. They haven't had an independent
> security audit and may contain security problems. Run them on a trusted home network.

## Install

It ships with labdex: **Plugins › Marketplace**, then *Install* (nothing is downloaded). Updates arrive through the official Marketplace (signed with the labdex project key).

## Settings

| Setting | Notes |
| --- | --- |
| Hosts | Ansible pattern: a host, a group like zone_dc_tc or tag_admin, or status_active |
| SSH user |  |
| SSH private key |  |
| Connection |  |
| Use sudo |  |
| Check SSH host keys |  |
| Banner file |  |
| Prompt file |  |

## Actions

- **Deploy banner and prompt** (plan)
- **Deploy to this host** (plan)

## Releasing

Bump `version` in `plugin.yaml`, add a `## <version>` section to `CHANGELOG.md`, commit, then
publish a GitHub release tagged `v<version>` (web UI, or `gh release create v<version> --target main --notes ""`).
The release workflow signs the plugin with the `LABDEX_SIGNING_KEY` secret and attaches `motd-<version>.zip` to a GitHub release.
