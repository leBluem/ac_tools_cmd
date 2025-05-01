## ac_tools_cmd

This package includes 4 commandline programs for use in batch files, and some batchfiles for an easy start.

The included programs are:

### acd_file
 - unpack or pack 'data.acd' or 'data' folders

### kn52fbx
 - based on CM code
 - includes some fixes for
 -- texture-filenames with spaces
 -- Transparent/AlphaBlend/AlphaTest flags

### kn5FIX_by_INI
 - excepts single '.kn5' files or and folders
 - from nearby persistence file '.fbx.ini'
 - fixes only bytes:
 -- for mat-alphablend/alphatest
 -- obj-transparency

### ksEditorAT
 - included for convinience, original from https://ascobash.wordpress.com/2015/07/22/kseditor/
 - builds both car+track kn5's via commandline from '.fbx' and '.fbx.ini' files


some of the included example batch files:

```
acd_or_data.cmd
fbx2kn5_car.cmd
fbx2kn5_track.cmd
kn52fbx.cmd
kn5FIX_by_INI.cmd
...
```

v0.3 changelog
-fixed acd-packer
-'acd_file' for packing now accepts both car-folder or car/data-folder
-fixed kn5Fix :)

v0.4 changelog
-more verbose log output
-fixed kn52fbx.exe exporting to "....kn5.kn5" folder

v0.5 changelog
-changelog added "fbx2kn5_lod.cmd" for drag'n'drop to create car LOD files updated again 20minutes later :( changed all cmd files to work in a folder with spaces, sorry

v0.6 changelog
-fixed kn52fbx.exe failing on KN5's without materials

v0.7 changelog
-fixed kn52fbx.exe on huge KN5's, timeout was set to 2 minutes only

v0.8 changelog
-"kn52fbx":
--DAE file is kept after converting to fbx

-"kn5fix":
--input-KN5 will be updated with from all the values in persistence file ...fbx.ini
--also textures if newer ones disk, does not touch the 3d meshes
--note: also updates SHADER= used and all shader vars...

-added new tool "KN5Join"
--wants a "ini" as input, format like "models.ini"
--sections can start at any value ([MODEL_66]...)
--joins KN5's respecting "POSITION" and "ROTATION" params
--made specifically for "TrackDecoration" app https://www.overtake.gg/downloads/trackdecoration.76979/

-removed all shift-key stuff, now there is always a "press any key" pause after programs ran
