# ! note: bug in v0.1 of 'acd_file', wait for a fix

# ac_tools_cmd

This package includes 4 commandline programs for use in batch files, and some batchfiles for an easy start. All programs make backups for existing files or make a new directory.
 - dl here: https://github.com/leBluem/ac_tools_cmd/releases/tag/0.1

The included programs are:

### acd_file
 - unpack 'data.acd' file -or- pack 'data' folder
 - makes backup of existing files if needed

### kn52fbx
 - based on CM code
 - excepts single '.kn5' files or folders
 - uses fbxConverter.exe (also included)
 - unpacks into new folder
 - includes some fixes for
 -- texture-filenames with spaces
 -- Transparent/AlphaBlend/AlphaTest flags

### kn5FIX_by_INI
 - excepts single '.kn5' files or folders
 - overwrites original, NO (!) backup is made
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
