<p align="center">
  <img src="assets/crow-foodie-logo.svg" alt="Crow Foodie logo: a crow holding a piece of ravioli" width="420">
</p>

# Crow Foodie
*created in 2023 by [Daniel McKeown](https://altaredwood.work)*

Crow Foodie is a tiny game for the [Playdate](https://play.date/) handheld, made with [Pulp](https://play.date/pulp/). You play as a crow trying out tasty snacks. This is version 2 of the game.

## What’s in this repository

- [`Crow-Foodie.pdx/`](Crow-Foodie.pdx/) is the built game, ready to run on Playdate. A `.pdx` is a bundle directory, not itself a ZIP file; this one contains its `pdxinfo` metadata, game data, and other built assets.
- [`Crow Foodie.json`](Crow%20Foodie.json) is Pulp’s full-game JSON export. It contains the editable game data, including rooms, tiles, scripts, music, and sound effects. The built PDX also contains a zipped JSON backup at `Crow-Foodie.pdx/data.json.zip`.
- [`assets/crow-foodie-logo.svg`](assets/crow-foodie-logo.svg) is the README logo.

The PDX folder was extracted from the Pulp export archive `IDFMEJOLZPCrow-Foodie_20261105212227.zip`; that archive is not included here.

## Building or editing the game

The included `.pdx` is already built. To make a new build from the editable project, open or import `Crow Foodie.json` in the [Pulp editor](https://play.date/pulp/) and use Pulp to download/export the game as a PDX. Pulp is a web-based editor and may require signing in.

There is no standalone build script in this repository. The Playdate SDK documents building games from native Lua/C projects, but does not document a command-line build from a Pulp JSON export. In other words, the SDK’s compiler is not a direct replacement for importing the project into Pulp and exporting it. The `.pdx` is the game package, not the editable project; don’t rename it to `.zip` or try to rebuild it by editing its internal files.

For more detail, see the Pulp documentation’s [Publishing a Pulp Game](https://play.date/pulp/docs/#goto-publishing-a-pulp-game) section and the [Playdate SDK documentation](https://sdk.play.date/), including its [`pdxinfo` metadata reference](https://sdk.play.date/Inside%20Playdate.html#pdxinfo).