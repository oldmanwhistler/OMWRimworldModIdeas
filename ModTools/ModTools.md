# RimWorld Mod Tools

## Recommended Tools

### VS Code integrated development environment

* A [jetbrains plugin for RimWorld Development that you can use with VS Code](https://plugins.jetbrains.com/plugin/21728-rimworld-development-environment/versions/stable)!
  * dotnet nuget update source "RimWorldDevEnv" --source "C:\Users\USER\Documents\VSCodeDotNet\LocalPackages"

### Markdown to steam BB code .NET tool

It's 2026. Write mod documentation in Markdown and then convert it to BBCode when you publish.

```bash
# also needed to download .NET 7.0
dotnet tool install -g Converter.MarkdownToBBCodeSteam.Tool
```

```json
{
    // See https://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    "version": "2.0.0",
    "tasks": [
        {
            "label": "Convert to Steam bbcode",
            "type": "shell",
            "command": "markdown_to_bbcodesteam -i ${file} -o ${file}.bbcode",
            "group": "build"
        }
    ]
}
```


### [ModMixer](https://github.com/lebek/modmixer)

TUI tool for building RimWorld mods. Has the ability to decompile the game and look up information, so very handy even if you're just using it as an API search since it will do better than an LLM that doesn't have access to the game source.

It makes initializing new mods and publishing to steam a breeze.

### [Rimsort](https://rimsort.github.io/RimSort/)

Tablestakes for organizing mods.

## Mods for Mod Development

* [What's That Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=2258431182) - find the source of a modded item
* [[1.5-1.6] Custom Xenotype Exporter Tool](https://steamcommunity.com/sharedfiles/filedetails/?id=3254345251) - easiest way to make new xenotypes based on existing gene packs
* [Blueprints Forked 1.6](https://steamcommunity.com/sharedfiles/filedetails/?id=3525001145) - can be used to export buildings you can use in a mod

## Don't Recommend

* [This site has a javascript based XML def library](https://rimworld.lattemacchiato.dev/), slow AF though and the def window is too small
  * [RimWorld Auto Documentation](https://github.com/Epicguru/Rimworld-Auto-Documentation) seems to be what was used to generate the RimWorld.lattemacchiato.dev website.
* [Workshop walker lets you do a reverse lookup and find mods that are dependent on a mod](https://workshop-walker.disconsented.com/app/294100). Steam has this builtin with the new workshop UI.
* [rwxml-language-server extension for VS Code](https://github.com/1264600905/rwxml-language-server/tree/pr-rebuild). It has a fork where someone is updating it for 1.6, but I couldn't figure it out how to build an extension with it or how to get language servers to work.

## Haven't Tried

* [Mlie's rimworld modding tools](https://github.com/emipa606/RimworldModdingHelpers)
* [RimSage MCP](https://rimsage.com/) MCP server for rimworld
* [RiMCP Hybrid](https://github.com/h7lu/RiMCP_hybrid) MCP server for rimworld
