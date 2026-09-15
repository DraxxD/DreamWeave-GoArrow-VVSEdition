# GoArrow-VVSEdition
Forked GoArrow from Virindi SVN repo


To install download the two files under releases, the DLL and dll.config.

Copy to your goarrow folder, default is C:\Games\VirindiPlugins\GoArrowVVSEdition

Click yes to overwrite the two files

Restart AC if it's already open.

## DreamWeave fork notes

This fork adds a realm-aware locations filter on top of Xanius' GoArrow-VVSEdition. Changed source files: `GoArrow/RouteFinding/Location.cs`, `GoArrow/Huds/MapHud.cs`, `GoArrow/PluginCore.cs`.

For the realm filter to actually work in-game, two things are required:

1. A `GoArrow.dll` compiled from this fork's source (contains the `mRealm` support).
2. A `locations.xml` where entries have the `realm=` attribute set. This data file is maintained separately in the DreamWeave-GoArrow-Data repo, not part of this repo.

`GoArrow.dll.config` and the other bundled dependency (`ICSharpCode.SharpZipLib.dll`) are unchanged from the original fork and do not need to be replaced.
