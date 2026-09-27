# Blueprints for Scenarios

I'm writing this because I figured this out in May 2026 and I'm going nuts in Sep 2026 trying to remember how I did this.

## Blueprints vs Prefabs

Blueprints save repeating structures that the user can use for building templates, even within the same game world.

KCSG.StructureLayoutDef can be used with Vanilla Expanded Framework to create structures that can be used in scenarios and mods.

Don't fall down a rabbit hole trying to add the Blueprints mod to scenarios, you'll find some bad advice about that online.

It's easier to use VEF prefabs in scenarios, although your mod will require VEF (which is reasonable, almost everything does).

I *do* however recommend saving the structure as a Blueprint as well as a prefab as if it takes multiple tries to save the prefab correctly, it's easier to reload blueprints because you don't need debug commands.

## Mod for saving and loading prefabs

* [Vanilla Expanded Framework](https://steamcommunity.com/sharedfiles/filedetails/?id=2023507013)
* [Vanilla Base Generation Expanded](https://steamcommunity.com/sharedfiles/filedetails/?id=3209927822) -- ONLY NEEDED FOR EXPORT

The trick here is to design your buildings with the minimum number of dependencies your expecting and NO IDEOLOGY. I'd recommend designing without any DLC loaded except for the ones the mod already depends on if you want to create a prefab for a scenario.

Anything with an Ideology style will not be exported properly.

## Designing

Go into Developer Mod, and click on the "god mode" icon to unlock all buildings in the architecture menu.

* [Designator Shapes](https://steamcommunity.com/sharedfiles/filedetails/?id=1235181370) is very useful for quickly creating different shapes to build up a structure.

The `T: Destroy` action is your friend so you don't leave construction material on the floor like you would when you click Deconstruct.

You'll need to unpause to get the pawns to construct the roof area/

## Export

After you are done building your structure, go into Orders and choose Export then select your area.

This will create a KCSG.StructureLayoutDef on your clipboard and you have to paste it into an XML file in your mod within `<Defs>`.

## Scenarios

VEF will add `add custom structure` to the scenario parts which you can use to add your KCSG.StructureLayoutDef to a scenario.
