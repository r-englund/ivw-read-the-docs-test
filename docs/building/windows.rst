Building Inviwo on Windows 
==========================

Requirements
--------------

+----------------------+------------------+----------------------+
| What                 | Required Version | Recommended Version  |
+======================+==================+======================+
| CMake_               | 3.2.0            | 3.9.1                |
+----------------------+------------------+----------------------+
| Visual_ Studio_      | 2015 Update 3    | 2017 (latest update) |
+----------------------+------------------+----------------------+
| Qt_                  | 5.3              | 5.9.1                |
+----------------------+------------------+----------------------+
| Any git client       |                  | SourceTree_          |
|                      |                  | TortoiseGit_         |
+----------------------+------------------+----------------------+

.. _CMake: https://cmake.org/  
.. _Visual: https://www.visualstudio.com/downloads/
.. _Studio: https://www.visualstudio.com/downloads/
.. _Qt: http://download.qt.io/archive/qt/
.. _TortoiseGit: https://code.google.com/p/tortoisegit/

For QT, when installing, select a binary of this sort:  ``qt-opensource-windows-x86-msvc2017_64-5.9.1.exe``. Make sure that you get one for the *Visual Studio* version that you are using. Note, Inviwo only support  64-bit builds make sure you have ``_64`` in the name. After installing make sure that the Qt bin folder is in the system path. Then CMake will have a much easier time finding the dependencies, and Inviwo will be able to find the needed lib/dll files.

Getting the source
------------------
.. include:: source.rst
    :start-line: 3


Generate Visual Studio Solution and Build
-----------------------------------------
Start the CMake-gui app. Set ``Where is the source code`` to the folder where the Inviwo source code is. Set ``Where to build the binaries`` to a folder somewhere outside of the Inviwo source and press ``Configure``. You will be asked which generator you want to use. Select *Visual Studio*, either ``Visual Studio 14 2015 Win64`` or  ``Visual Studio 15 2017 Win64`` depending on which version of *Visual Studio* you have installed. 

TODO CMAKE OPTIONS

If no errors occurred, press ``Generate`` to generate the final solution and the ``Open Project`` to open Visual Studio. In Visual Studio build and run the target inviwo or inviwo-cli

EXTERNAL MODULES ``IVW_EXTERNAL_MODULES``


