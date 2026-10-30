# Doomblade

A plugin for Paper 1.21.11 — an addon for **MMOItems** that adds a "second life" mechanic to a special sword.

## Mechanics

The `TWO_TIMES_BLADE` sword counts mob kills. At **20 kills** the blade becomes charged. When the player is about to die, a totem effect triggers instead of death: the player is revived, but pays for it — a curse halves their maximum health.

| Key | Value | Meaning |
|---|---|---|
| `blade-id` | `TWO_TIMES_BLADE` | MMOItems item ID |
| `charges-to-arm` | `20` | kills required to arm the totem |
| `totem-health-fraction` | `0.5` | fraction of HP the totem revives you with |
| `curse-fraction` | `0.5` | how much of the maximum HP the curse cuts |

## Config

```yaml
blade-id: TWO_TIMES_BLADE
charges-to-arm: 20
totem-health-fraction: 0.5
curse-fraction: 0.5
```

## Technical notes

- Paper API 1.21, `api-version: 1.21`, depends on `MMOItems`.
- Single class: `com.rpg.doomblade.DoombladePlugin`.
- Built as `Doomblade.jar`, version 1.0.0.
- Comments in the config are in English; the in-game lore strings (`lore-marker`, `lore-line`, `lore-armed`) are in Russian, as the server's audience is Russian-speaking.

## Authors

- **Jadeonit** — idea, mechanics, balance, config, testing.
- **ChatGPT 5.6** — co-author: helped with the code implementation.

The authorship is also written into `plugin.yml` inside the JAR (`authors: [Jadeonit, ChatGPT 5.6]`), so it is visible in-game via `/plugins`.
