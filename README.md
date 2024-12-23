
![Logo](https://www.jakarobotics.com/wp-content/uploads/2022/07/jaka-robotics-logo-1.png)
#### Software Development Kit



## Documentation

All documentation can be found on our [documentation hub](https://www.jaka.com/docs/en/).


## Installation

Download your system specific zip [here](https://github.com/JAKARobotics/sdk-cpp/releases/tag/latest).

#### Visual Studio

Extract the zip folder contents directly into your main project folder.

Now just import the header file:

```cpp
#include "JAKAZuRobot.h"

```

#### Cmake

First extract the zip folder contents directly into your main project folder.

It is recommended to download the installation package for the corresponding platform from the [official Cmake website](https://cmake.org/).

This example uses Cmake version 3.7.2.

___

#### CMakeLists.txt

```cmake
cmake_minimum_required(VERSION 3.7.2)    # Minimum CMake Version 
project(sdk_test VERSION 1.0)     # Project Definition

# C++ Standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED true)

# Source Directory Information
message(${CMAKE_SOURCE_DIR})

# Executable Creation
add_executable(demo main.cpp)

# Set the header file path of the SDK included in the project
target_include_directories(demo PUBLIC ${CMAKE_SOURCE_DIR}/c&c++/inc_of_c++)
  
# Set the SDK dynamic library link path
target_link_libraries(demo ${CMAKE_SOURCE_DIR}/c&c++/x86_64-linux-gnu/shared/libjakaAPI.so pthread)

```

For detailed installation instructions refer to the [documentation](https://www.jaka.com/docs/en/guide/SDK/JAKA%20SDK%20Quick%20Start%20-%20EN.html#creating-c-applications-with-cmake-on-linux).


## Feedback

Our Software Development Kit is still in its early and we are open to any improvements. Please also let us know of any new features you need that the sdk currently does not support.

## FAQ

#### I want "x" new feature.

Please let us know in the [wishlist](https://github.com/JAKARobotics/jakasdk-cpp/issues/1) issue thread.


....




## License

[GNU AGPLv3 ](https://choosealicense.com/licenses/agpl-3.0/)

