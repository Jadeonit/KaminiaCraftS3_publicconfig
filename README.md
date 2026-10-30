# Kaminiacraft S3 — plugin configuration

Plugin configuration of the **Kaminiacraft S3** Minecraft server (Purpur 1.21.11): the RPG layer — progression, classes, custom items and mobs — plus my own plugins.

This repository only contains what I actually built myself: the RPG system, permissions and my own plugins. Configs of plugins I had no hand in are not included.

## Stack

| Layer | What is used |
|---|---|
| RPG progression | AuraSkills, MMOCore, MMOItems, MythicLib, MythicMobs |
| Permissions | LuckPerms |
| My own plugins | Doomblade, RecipeBookFiller (MMOItems addons) |

## Layout

```
plugins/
  AuraSkills/                # skills, abilities, loot, menus, rewards
  MMOCore/                   # classes, professions, skill trees, GUI
  MMOItems/                  # items, types, skills, templates
  MythicMobs/                # mobs, drop tables, spawners
  MythicLib/                 # shared stat library
  LuckPerms/                 # config and contexts
custom/
  Doomblade/                 # my plugin: a second life for the blade
  RecipeBookFiller/          # my plugin: MMOItems recipes in the vanilla recipe book
```

## My plugins

Both are MMOItems addons. I designed the mechanics and the requirements; the implementation was written with help from an AI.

| Plugin | What it does |
|---|---|
| **Doomblade** | The `TWO_TIMES_BLADE` sword accumulates 20 mob kills, then acts as a totem: instead of dying, the player is revived at 50% HP, but a curse halves their maximum health |
| **RecipeBookFiller** | Loads MMOItems crafting recipes into the vanilla recipe book when a player joins (with a configurable tick delay) |

The JARs live in `custom/` next to their configs and a description of the mechanics.

**ChatGPT 5.6** is credited as co-author of both plugins (helped with the code implementation). The authorship is written into `plugin.yml` inside each JAR, so it shows up in-game via `/plugins`.

## What is not in this repository

- **Worlds** (`world*`) — map size and content.
- **Databases and player data** — `*userdata*`, `*.db`, `*.mv.db`, save files.
- **Logs, caches, server binaries.**
- **Configs of plugins I did not work on** — CMI/CMILib, FlectonePulse, WorldEdit, AxiomPaper, PlugManX, Vault, spark, bStats.
- **Plugin translations** (`Translations/`, `localizations/`, `language/`) — those files belong to the plugin authors, not to me.

## Roadmap

The world map will be published when the current season ends. This repository will be updated at that point — the season's configs and the map will be added together.

## Note on language

Documentation, file structure and code comments in this repository are in English. In-game content is kept in Russian, because the server's audience is Russian-speaking: item names and lore (`plugins/MMOItems/item/*.yml`), class names (`plugins/MMOCore/classes/*.yml`), GUI titles (`plugins/MMOCore/gui/*.yml`), quest and reward texts (`plugins/AuraSkills/rewards/*.yml`) and the Doomblade lore lines.

## License

The configuration is my work. The plugins these files belong to are owned by their respective authors and distributed under their own licenses.
