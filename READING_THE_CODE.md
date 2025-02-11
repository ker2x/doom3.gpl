I'll just drop whatever i find here

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
  
