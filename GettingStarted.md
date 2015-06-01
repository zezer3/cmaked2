This short guide will explain how to install cmaked2 and run the tests on `*`nix and Windows.

# Installation #

  * Clone the cmaked2 repository

> `hg clone http://cmaked2.googlecode.com/hg/ cmaked2`

  * `cd cmaked2/cmaked`

  * `mkdir build`

  * `cd build`

  * You need at least CMake version **2.8.1** for installing cmaked2.

> `cmake ..`

  * You need to have write access to your CMake installation directory.

> `sudo make install`

## Uninstall ##

To uninstall run

`xargs rm < install_manifest.txt`

See http://cmake.org/Wiki/CMake_FAQ#Can_I_do_.22make_uninstall.22_with_CMake.3F

# Testing Your Installation #

  * `cd cmaked2/tests`

  * `mkdir build`

  * `cd build`

  * `cmake ..`

  * `make`

  * `make test`

The last three commands should run without **any** error. Please [submit an issue](http://code.google.com/p/cmaked2/issues/entry) in case of problems.

# Installing with Wine #

  * Download DMD from http://ftp.digitalmars.com/dinstaller.exe and install it.

> `wine dinstaller.exe`

> DMD 2.048 should work.

  * Download MinGW http://sourceforge.net/projects/mingw/files/Automated%20MinGW%20Installer/MinGW%205.1.6/MinGW-5.1.6.exe/download and install it

> `wine MinGW-5.1.6.exe`

**You need to install MinGW Make.**

> MinGW 5.1.6 should work.

  * Download the latest CMake version for Windows from http://www.cmake.org/cmake/resources/software.html. The Win32 Installer should work and install CMake.

> `wine cmake-2.8.2-win32-x86.exe`

> CMake 2.8.2 should work.

  * Install cmaked2.

> `cd /path/to/cmaked2/cmaked`

> `wine ~/.wine/drive_c/path/to/cmake.exe -G "MinGW Makefiles" .`

> `wine ~/.wine/drive_c/path/to/MinGW/bin/mingw32-make.exe install`

  * Testing

> `cd /path/to/cmaked2/cmaked/tests`

> `wine ~/.wine/drive_c/path/to/cmake.exe -G "MinGW Makefiles" .`

> `wine ~/.wine/drive_c/path/to/MinGW/bin/mingw32-make.exe`

> `wine ~/.wine/drive_c/path/to/MinGW/bin/mingw32-make.exe test`

# Installing on Windows #
A prerequisite for building cmaked2 for Windows is Visual Studio.  We tested with the free version, Visual Studio Express.  Download and setup of Visual Studio is not described here.

  * Download cmake http://www.cmake.org/files/v2.8/cmake-2.8.2-win32-x86.exe

  * Download and install DMD http://ftp.digitalmars.com/dinstaller.exe.  We tested with version 2.048.

  * Download and install Mercurial http://mercurial.selenic.com/downloads

  * Using the Visual Studio command prompt, cd to a folder where you want to clone cmaked2.  Make sure the command prompt opens with administrator privileges.

  * `hg clone http://cmaked2.googlecode.com/hg/ cmaked2`

  * `cd cmaked2/cmaked`

  * `mkdir build`

  * `cd build`

  * You need at least CMake version **2.8.1** for installing cmaked2.

> `cmake ..`

  * You need to have write access to your CMake installation directory.

> `nmake install`


## Testing Your Installation ##

  * `cd cmaked2/tests`

  * `mkdir build`

  * `cd build`

  * `cmake ..`

  * `nmake`

  * `nmake test`


# Resources #
[CMake](http://www.cmake.org/cmake/help/documentation.html)