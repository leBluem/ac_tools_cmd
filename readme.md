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
fbx2kn5_car.cmd   (also runs kn5FIX_by_INI.cmd)
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
added "fbx2kn5_lod.cmd" for drag'n'drop to create car LOD files
updated again 20minutes later :(
changed all cmd files to work in a folder with spaces, sorry

v0.6 changelog
-fixed kn52fbx.exe failing on KN5's without materials

v0.7 changelog
-fixed kn52fbx.exe on huge KN5's, timeout was set to 2 minutes only
