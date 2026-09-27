# Blueprints

## Blueprints vs Prefabs

Blueprints save repeating structures that the user can use for building templates.

Prefabs can be used with Vanilla Expanded Framework to create structures that can be used in scenarios and mods.

If you want to create structures you can load from within your mod then you want [KCSG.StructureLayoutDef](ScenarioStructures.md)

## Requirements

* [Blueprints Forked 1.6](https://steamcommunity.com/sharedfiles/filedetails/?id=3525001145)

The trick here is to design your buildings with the minimum number of dependencies your expecting and NO IDEOLOGY. I'd recommend designing without any DLC loaded except for the ones the mod already depends on if you are using a scenario.

Anything with an Ideology style will not be exported properly.

## Creative mod

Go into Developer mode, and click on the "god mode" icon to unlock all buildings in the architecture menu.

The `T: Destroy` action is your friend so you don't leave construction material on the floor like you would when you click Deconstruct.

After you are done building your structure, go into the Blueprint architecture menu, choose Create and then select the parts you want to export.

Name the blueprint, click export.

The exported file will be stored at: `%USERPROFILE%\AppData\LocalLow\Ludeon Studios\RimWorld by Ludeon Studios\Blueprints`

## Universal Blueprints

[Universal Blueprints](https://steamcommunity.com/workshop/filedetails/?id=3540066516) is the more modern version of this, which includes a website for uploading/downloading blueprints to share with different players.
