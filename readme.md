## Assetto Corsa 'ac_tools_cmd'
 - This package includes 5 commandline programs for use in batch files, and some batchfiles for an easy start.
 - Download on the right under "Releases"

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
 - changes everything different to that ^ , also textures if newer than KN5
 - batch file for that: "kn52_fbxini_only.cmd"
 - -export (or -e), will only export .fbx.ini from a KN5
 - -d param, delete objects from kn5, Mhesfilter: "material:mat?,meshX"
 - -s, delete all AC_START/... objects
 - -x exit after operations

### KN5Join
 - if input is a ini-file (format like "models.ini"), it will join files mentioned there
 - also valid: a KN5-file as input, or a folder, then you need one of the d/s params
 - sections can start at any value ([MODEL_66]...)
 - joins KN5's respecting "POSITION" and "ROTATION" params
 - made specifically for "TrackDecoration" app https://www.overtake.gg/downloads/trackdecoration.76979/
 - -d param, delete objects from kn5, Mhesfilter: "material:mat?,meshX"
 - -s, delete all AC_START/... objects
 - -x exit after operations
 
### ksEditorAT
 - included for convinience, original from https://ascobash.wordpress.com/2015/07/22/kseditor/
 - builds both car+track kn5's via commandline from '.fbx' and '.fbx.ini' files



### Batch files
 - some of the included example batch files:
```
acd_or_data.cmd
fbx2kn5_car.cmd
fbx2kn5_track.cmd
kn52fbx.cmd
kn5FIX_by_INI.cmd
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

v0.9 changelog
--"kn52fbx" and "kn5fix" :
--small fixes for handling multiple files

-"kn5fix":
--added param -export (or -e), it will export .fbx.ini from a KN5
--added new batch file for that "kn52_fbxini_only.cmd"

-all programs:
--small fixes output and waiting after operations

v0.9.1 changelog
"kn5Join":
--joined objects will be renamed continuously
--handy for doing AC_PIT/AC_START/AC_TIME.. objects with "TrackDecoration" app https://www.overtake.gg/downloads/trackdecoration.76979/

v0.9.2 changelog
"kn5Join":
--added -x paramter to close after operation, used in TD

v0.9.3 changelog
"kn5Join":
--fixed not finding objects directory
--added logfile next to binary "kn5join_log.txt"

v0.9.5 changelog
"kn5Join":
--fixed renaming objects correctly

"kn52fbx":
--exported fbx file will have same name as original KN5

"kn5fix":
--tiny fix


v0.9.8 changelog
"kn5join" and "kn5fix"
--added option to remove Objects from KN5's
-s   -strip/remove AC.. objects from KN5
     AC_START/_PIT/_TIME/_HOTLAP/_AB_START/_AB_FINISH/_OPEN_FINISH
-d param -delete custom objects from KN5
      param - meshfilter, comma separated list, ? as universal wildcard
      ie 'str1,str?' or 'material:groove?'

v0.9.9 changelog
"kn5join" and "kn5fix"
--fixed CaseSensitivity for custom mesh filter (-d param)
--up'ed binary version number

