# Bulding Inviwo on Linux
## Required packages
* __CMake 3.2__ 
* __Qt 5.3__ (5.6 Recommended) 
* (git) 

```
sudo apt-get install build-essential cmake cmake-qt-gui git 
```
Note: On Ubuntu versions older than 16.04 CMake 3.2 might not be available through apt-get, read more at  http://askubuntu.com/a/610352 

### QT 5
Recommended QT version is 5.6.1. There have been issues running with earlier version of Qt 5.
Use the following instructions to install QT 5.6.1
```
wget http://download.qt.io/official_releases/qt/5.6/5.6.1/qt-opensource-linux-x64-5.6.1.run
chmod +x qt-opensource-linux-x64-5.6.1.run
./qt-opensource-linux-x64-5.6.1.run
```

## Getting the source and building inviwo
1. clone the source:  ```git clone https://github.com/inviwo/inviwo.git```
1. Start the CMake gui: ```cmake-gui &```
1. 1. Specify the path to the source code and where you want the build directories
1. 1. Hit configure, select Unix Makefiles (repeat until no read options are available) 
1. 1. Hit Generate
1. In a terminal, go to the build folder and run make: ```make -j8``` (where 8 is the number of threads you want to use for building) 
1. When done, start inviwo ```./bin/inviwo```
