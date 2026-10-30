# RecipeBookFiller

A plugin for Paper 1.21.11 — an addon for **MMOItems**.

## What it does

The vanilla recipe book knows nothing about MMOItems crafts: a player opens it and sees only vanilla items. This plugin loads MMOItems recipes into the recipe book on player join, so they can be viewed and crafted right from the interface.

Custom recipes are handed out with a delay so the plugin does not race with others that also touch the recipe book on join.

## Config

```yaml
# Delay before recipes are pushed to the book on join (in ticks, 20 = 1 second).
delay-ticks: 40
```

## Technical notes

- Paper API 1.21, `api-version: 1.21`, depends on `MMOItems`.
- Single class: `com.rpg.recipebook.RecipeBookFiller`.
- Built as `RecipeBookFiller.jar`, version 1.0.0.

## Authors

- **Jadeonit** — idea, requirements, config, testing.
- **ChatGPT 5.6** — co-author: helped with the code implementation.

The authorship is also written into `plugin.yml` inside the JAR (`authors: [Jadeonit, ChatGPT 5.6]`).
