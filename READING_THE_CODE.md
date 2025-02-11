I'll just drop whatever i find here

# Cool links

## FABIEN SANGLARD
- [DOOM3 SOURCE CODE REVIEW: Introduction](https://fabiensanglard.net/doom3/index.php)
- [DOOM3 SOURCE CODE REVIEW: DMAP](https://fabiensanglard.net/doom3/dmap.php) 
- [DOOM3 SOURCE CODE REVIEW: RENDERER](https://fabiensanglard.net/doom3/renderer.php) 
- [DOOM3 SOURCE CODE REVIEW: PROFILING](https://fabiensanglard.net/doom3/profiling.php)
- [DOOM3 SOURCE CODE REVIEW: SCRIPTING](https://fabiensanglard.net/doom3/scripting_vm.php)
- [DOOM3 SOURCE CODE REVIEW: INTERVIEWS](https://fabiensanglard.net/doom3/interviews.php)


# Directories
 
- [/base/](base)
  - Default.cfg: Empty file
  - Possibly a directory that hold the game data that wasn't opensourced ?
- [neo/](neo)
  - [cm/](neo/cm)
    - contain _CollisionModel_ related classes
  - [curl/](neo/curl) : the curl source code (tools & libs)
  - [d3xp/](neo/d3xp) : **Doom3 eXPension** (Ressurection) gameplay
    - [ai/](neo/d3xp/ai)
      - Appears to contain code related to NPC actions
    - [anim/](neo/d3xp/anim)
      - 3D model animation code ?
    - [gamesys/](neo/d3xp/gamesys)
      - various stuff i have yet to understand
    - [physics/](neo/d3xp/physics)
      - Look like the physic engine
    - [script/](neo/d3xp/script)
      - The scripting engine (compilers, etc)
    - many cpp & h files, including the core part of the game engine
  - [framework/](neo/framework)
    - [async/](neo/framework/async)
  - [game](neo/game) : **Doom3 gameplay**
    - ai
    - anim
    - gamesys
    - physics
    - script
  - [idlib](neo/idlib) : id Software library. Includes parser,lexer,dictionary ...
    - bv
    - containers
    - geometry
    - hashing
    - math
  - [MayaImport](neo/MayaImport) : Maya model import/export
  - [openal](neo/openal) : openAL wrapper ?
  - [renderer](neo/renderer) : the mighty rendering engine !
  - [sound](neo/sound) : something about sound, probably.
  - [sys](neo/sys) : look like OS specific code
  - [tools](neo/tools)
  - [TypeInfo](neo/TypeInfo) : For TypeInfo.exe (In-house RTTI helper, according to Fabien Sanglard)
  - [ui](neo/ui) : ?


# Important files

## MAINs

- for linux: [neo/sys/linux/main.cpp](neo/sys/linux/main.cpp)
- for windows: [neo/sys/win32/win_main.cpp](neo/sys/win32/win_main.cpp)
- for osx: [neo/sys/osx/macosx_sys.mm](neo/sys/osx/macosx_sys.mm)

## Game entry point

- [neo/framework/Common.cpp](neo/framework/Common.cpp)
    - Linux main call _idCommonLocal::Init_
    - Windows ... it's complicated, but it call _idCommonLocal::Frame_ (i might have missed call to Init)
    - OSX: Something _NSApplicationMain_ something something probably end up in Common.cpp somehow
