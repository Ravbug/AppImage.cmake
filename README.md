# AppImage.cmake

This repository contains a CMake script which facilitates generating [AppImage](https://appimage.org/) executables for Linux. 
It handles downloading AppImageTool,  setting up the AppDir, and invoking AppImageTool to generate the AppImage.

## Usage:
Invoke as an install action:
```cmake
INSTALL(CODE 
  "include(../appimage.cmake)
  make_appimage(
        EXE \"path/to/your/built/executable\"
        NAME \"YourAppName\"
        ICON \"path/to/your/icon.svg\"
        DIR_ICON \"path/to/your/diricon.png\"
        OUTPUT_NAME \"where/to/write/App.AppImage\"
        ASSETS \"A list;of all extra files;to copy to the folder\"
    )
	" 
	COMPONENT Runtime
)
```
For an example, see how it is used in [the RavEngine sample projects](https://github.com/ravbug/ravengine-samples).

## Reporting Bugs and Feature Requests
Please report all issues to the Issues section of this repository.
