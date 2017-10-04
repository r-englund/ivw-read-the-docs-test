# Bulding Inviwo on Mac OSX
To build from source, use [homebrew](http://brew.sh/) to install packages.

**Required packages**
* __XCode__ [Download](https://itunes.apple.com/se/app/xcode/id497799835?mt=12)
* __CMake >= 2.8.4__ ```brew install cmake```
* __Qt5 >= 5.3__ ```brew install qt5```

**Optional packages**
* __Python3__ ```brew install python3```
* __HDF5__ ```brew install hdf5 --with-cxx --c++11```

**Setup Instructions**

1. Clone all repos to your computer. Remember that you choose the parent directory of the repo, such that choosing _~/Inviwo_ for inviwo-dev will put your files in _~/Inviwo/inviwo-dev_

2. Run CMake (terminal or gui) and run configure using the inviwo-dev directory as your source, and a build directory of your choice outside of the source code. For CMake to find Qt5 automatically we have to add the Qt5 install path to CMAKE_PREFIX_PATH. This can be done by: 
```
export CMAKE_PREFIX_PATH=/usr/local/Cellar/qt5/5.4.0/; open /Applications/CMake.app
```

3. Add path to modules outside of inviwo-dev in **IVW_EXTERNAL_MODULES** in the format of "_~/Inviwo/otherrepo/modules;~/mysite/myrepo/mymodules_". Run configure.

4. Then run "make" on your build directory and you will find the application in build/bin/inviwo.

5. DONE!

**Notes**
* Edit the ALL_BUILD Scheme in XCode:
    * Under __Run/Info__ set the __Executable__ to __inviwo.exe__ 
    * Under __Run/Options__ make sure that "__Document Versions__" is deselected