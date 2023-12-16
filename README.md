# ac_tools_cmd

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
