[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![macOS](https://github.com/AhmetTavli/Badge/blob/master/badges/mac_badge.svg)](https://www.apple.com)
[![CMake](https://github.com/AhmetTavli/Badge/blob/master/badges/cmake_badge.svg)](https://cmake.org/)
[![Python](https://github.com/AhmetTavli/Badge/blob/master/badges/python_badge.svg)](https://www.python.org/)
[![Caffe](https://github.com/AhmetTavli/Badge/blob/master/badges/caffe.svg)](https://caffe.berkeleyvision.org/)

# Caffe Installation Instructions for CPU and
Make sure you've downloaded [caffe-master](https://github.com/BVLC/caffe)
Open the [CMakeList.txt](https://github.com/BVLC/caffe/blob/master/CMakeLists.txt)

Compile Caffe from CMakeList :desktop_computer:
============================

We will be modifying the following lines:

1. Set CPU_ONLY mode on

```cmake
caffe_option(CPU_ONLY  "Build Caffe without CUDA support" ON)
```

2. Add C++11 standard

```cmake
if(UNIX OR APPLE)
  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fPIC -Wall -std=c++11")
endif()
```

3. Set Python 3

```cmake
set(python_version "3" CACHE STRING "Specify which Python version to use")
```