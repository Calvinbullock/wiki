# CMakeLists.txt

#### Basic cmake config
```cmake
cmake_minimum_required(VERSION 3.5)
project(runMe) # the name of the binary file

# Include directories for header files
include_directories()

# Set source files
set(SOURCE_FILES ./main.cpp) # include all .cpps or use *.cpp

# Generate executable
add_executable(runMe ${SOURCE_FILES})

# link target library's
# target_link_libraries(SkeetShootingGame -lglut -lGL -lGLU -lGLEW)
```

#### NOTES ABOUT USE
To use this you need to put a `build/` directory in the directory with the cmake.txt
