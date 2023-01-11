# CMake
CMake is a cross-platform build system generator. It is used to build, test, and package software. It can generate native build files for a variety of platforms, including Windows, MacOS, and Linux. CMake is particularly useful for building large, complex software projects that need to be built on multiple platforms or with multiple build configurations.

CMake uses a simple, human-readable script format (CMakeLists.txt) to describe the build process for a project. This script is then used to generate platform-specific build files, such as Makefiles on Linux or Visual Studio solutions on Windows. This allows developers to use a single build system that can be used on multiple platforms, rather than having to maintain multiple build scripts for different systems.

CMake is also used to manage dependencies and to configure software at build time. For example, it can be used to check for the presence of certain system libraries and to set build flags accordingly.

The system summarization:

-   Cross-platform build system
-   Can generate native build files
-   Uses CMakeLists.txt to describe the build process
-   Manages dependencies
-   Configures software at build time

CMake, allow for using a single build system that can be used on multiple platforms which makes the development, deployment and maintainance of software much more simpler and straightforward, it is widely used on many open source and closed source projects making it a common standard.

i found this in jnilibs folder what platform r they describe in atable ├───arm64-v8a ├───armeabi-v7a ├───x86 └───x86\_64

The jniLibs folder you're looking at contains native libraries for different CPU architectures. The subfolders in the jniLibs folder correspond to different CPU architectures that the libraries have been compiled for. The specific subfolders and their meaning are:

-   arm64-v8a: Libraries for 64-bit ARM CPUs. These CPUs are typically found in newer smartphones and tablets.
-   armeabi-v7a: Libraries for 32-bit ARM CPUs with at least ARMv7 instruction set. These CPUs are typically found in older smartphones and tablets.
-   x86: Libraries for 32-bit x86 CPUs. These CPUs are typically found in older personal computers and mobile devices running Android-x86.
-   x86\_64: Libraries for 64-bit x86 CPUs. These CPUs are typically found in newer personal computers and some mobile devices.

Each of these folders will contain the native binaries that have been built for that specific architecture and the app can use at runtime to access specific features that is not available in java level.

 common CMake commands and their usage:

| Command | Explanation | Example |
| --- | --- | --- |
| `cmake_minimum_required` | Specifies the minimum version of CMake required to build the project. | `cmake_minimum_required(VERSION 3.10)` |
| `project` | Sets the name and language of the project. | `project(myproject CXX)` |
| `add_executable` | Adds an executable target to be built from the specified source files. | `add_executable(myapp main.cpp foo.cpp bar.cpp)` |
| `add_library` | Adds a library target to be built from the specified source files. | `add_library(mylib STATIC foo.cpp bar.cpp)` |
| `target_include_directories` | Specifies the include directories for a target. | `target_include_directories(mylib PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)` |
| `target_link_libraries` | Specifies libraries that a target links to. | `target_link_libraries(myapp PRIVATE mylib)` |
| `find_package` | Finds and loads a package. | `find_package(OpenCV REQUIRED)` |
| `include_directories` | Adds directories to the include search path. | `include_directories(${OpenCV_INCLUDE_DIRS})` |
| `set` | Creates or modifies a variable. | `set(MYVAR foo bar baz)` |
| `list` | Manipulates lists. | `list(GET MYLIST 2 MYVAR)` |
| `if` | Conditionally performs commands. | `if(WIN32) message( "Windows system") endif()` |
| `add_subdirectory` | Adds a subdirectory to the build. | `add_subdirectory(subdir)` |
| `set_target_properties` | set properties of the specified target. | `set_target_properties(mylib PROPERTIES COMPILE_FLAGS "-O3")` |
| `install` | Installs files or targets to the specified location. | `install(TARGETS myapp DESTINATION bin)` |
| `add_definitions` | Adds preprocessor definitions to the build. | `add_definitions(-DDEBUG)` |
| `file` | Perform file operations such as reading or writing. | `file(READ "file.txt" CONTENTS)` |
| `include` | Includes a CMake script file into the current script. | `include(MyModule.cmake)` |
| `add_custom_command` | Adds a custom command to be executed during the build. | `add_custom_command(OUTPUT ${CMAKE_CURRENT_BINARY_DIR}/out.txt COMMAND ${CMAKE_COMMAND} -E copy ${CMAKE_CURRENT_SOURCE_DIR}/in.txt ${CMAKE_CURRENT_BINARY_DIR}/out.txt)` |
| `add_custom_target` | Adds a custom target to the build. | `add_custom_target(mytarget DEPENDS myapp COMMAND ${CMAKE_COMMAND} -E echo "My custom target")` |
| `message` | Prints a message to the user. | `message("Compiling with flags ${MY_FLAGS}")` |
| `add_dependencies` | Adds dependencies between targets. | `add_dependencies(myapp mylib)` |
| `configure_file` | Copies a file and substitute variables during the copy. | `configure_file(config.h.in config.h)` |
| `set_property` | Set properties for directories or targets. | `set_property(TARGET mylib PROPERTY POSITION_INDEPENDENT_CODE ON)` |
| `execute_process` | Executes an external process and captures its output. | `execute_process(COMMAND ${CMAKE_COMMAND} -E echo_append "Hello, world!" OUTPUT_VARIABLE GREETING)` |
| `add_test` | Adds a test to the build. | `add_test(mytest myapp)` |
| `enable_testing` | Enables testing for the build. | `enable_testing()` |
| `configure_file` | Copies a file and substitute variables during the copy. | `configure_file(config.h.in config.h)` |
| `set_property` | Set properties for directories or targets. | `set_property(TARGET mylib PROPERTY POSITION_INDEPENDENT_CODE ON)` |
| `get_filename_component` | Extracts parts of a file path. | `get_filename_component(MYVAR ${CMAKE_CURRENT_SOURCE_DIR}/subdir ABSOLUTE)` |
| `get_property` | Get value of a property for given scope (e.g. target, directory or source file) | `get_property(MYVAR TARGET mylib PROPERTY POSITION_INDEPENDENT_CODE)` |
| `set_source_files_properties` | Sets properties of source files. | `set_source_files_properties(foo.c PROPERTIES LANGUAGE CXX)` |
| `string` | performs string operation. | `string(TOUPPER myvar MYVAR)` |
| `try_compile` | Attempts to compile and link a small program to determine whether the compiler and linker are functioning correctly. | `try_compile(COMPILED ${CMAKE_BINARY_DIR}/compile_test ${CMAKE_SOURCE_DIR}/compile_test.c)` |
| `get_directory_property` | Gets the value of a directory property. | `get_directory_property(MYVAR DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} COMPILE_OPTIONS)` |
| `set_directory_properties` | Sets properties for a directory. | `set_directory_properties(PROPERTIES INCLUDE_DIRECTORIES ${CMAKE_CURRENT_SOURCE_DIR}/include)` |
| `add_compile_options` | Adds options to the compilation of source files. | `add_compile_options(-Wall -Wextra)` |
| `add_compile_definitions` | Adds preprocessor definitions to the compilation of source files. | `add_compile_definitions(MYDEF=1)` |
| `math` | performs math operations on variables or expressions. | `math(EXPR MYVAR "1 + 2")` |
| `install(FILES)` | Installs files to the specified location. | `install(FILES myfile.txt DESTINATION share/myapp)` |
| `install(PROGRAMS)` | Installs executables to the specified location. | `install(PROGRAMS myapp DESTINATION bin)` |
| `install(DIRECTORY)` | Installs directories recursively to the specified location. | `install(DIRECTORY mydir DESTINATION include/myapp PATTERN "*.h")` |
| `make_directory` | creates a new directory. | `make_directory(${CMAKE_CURRENT_BINARY_DIR}/mydir)` |
| `break()` | Stop processing if in a loop, similar to the break statement in C/C++ | `foreach(myvar a b c) if(myvar STREQUAL "b") break() endif() endforeach()` |
| `get_source_file_property` | Retrieves a property of a source file. | `get_source_file_property(MYVAR ${CMAKE_CURRENT_SOURCE_DIR}/main.c COMPILE_DEFINITIONS)` |
| `set_source_files_properties` | Sets properties of source files. | `set_source_files_properties(main.c PROPERTIES COMPILE_DEFINITIONS MYDEF=1)` |
| `install(EXPORT)` | exports targets to a file to be included in other projects. | `install(EXPORT mylib DESTINATION share/cmake/mylib NAMESPACE My::)` |
| `export` | exports targets to be included in other projects. | `export(TARGETS mylib FILE mylib.cmake NAMESPACE My::)` |
| `find_path` | searches for a file in a list of directories. | `find_path(MYVAR myfile.h PATHS ${CMAKE_CURRENT_SOURCE_DIR}/include NO_DEFAULT_PATH)` |
| `find_library` | Searches for a library in a list of directories. | `find_library(MYVAR mylib PATHS ${CMAKE_CURRENT_SOURCE_DIR}/lib NO_DEFAULT_PATH)` |
| `find_file` | Searches for a file in a list of directories. | `find_file(MYVAR myfile.txt PATHS ${CMAKE_CURRENT_SOURCE_DIR}/data NO_DEFAULT_PATH)` |
| `find_program` | Searches for an executable in the system PATH. | `find_program(MYVAR myprogram)` |
| `include_directories` | Adds directories to the include search path. | `include_directories(${OpenCV_INCLUDE_DIRS} ${CMAKE_CURRENT_SOURCE_DIR}/include)` |
| `file(GLOB)` | Allows to specify a search pattern to locate files, it will return a list of all file path matching pattern. | `file(GLOB_RECURSE MYVAR ${CMAKE_CURRENT_SOURCE_DIR}/*.hpp)` |

```c++
cmake_minimum_required(VERSION 3.10)

project(myproject CXX)

# set a variable
set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)

# add source files
file(GLOB_RECURSE SRCS ${SRC_DIR}/*.cpp)

# Add a library
add_library(mylib SHARED ${SRCS})

# Specify include directories for the library
target_include_directories(mylib PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)

# set libary version
set_target_properties(mylib PROPERTIES VERSION 1.2 SOVERSION 1)

# Add an executable
add_executable(myapp ${SRC_DIR}/main.cpp)

# Link the executable to the library
target_link_libraries(myapp mylib)

# Add include paths for dependent package
find_package(Threads REQUIRED)
target_include_directories(mylib PRIVATE ${CMAKE_THREAD_LIBS_INIT})

# Add preprocessor definitions
add_definitions(-DDEBUG)

# Add compile options
add_compile_options(-Wall -Wextra)

# set variable
set(MYVAR "hello")

# define an option
option(ENABLE_MYFEATURE "Enable my feature" ON)

# add if statement to check option
if(ENABLE_MYFEATURE)
  add_definitions(-DUSE_MYFEATURE)
endif()

# Generate export header
include(GenerateExportHeader)
generate_export_header(mylib)

# Retrieve properties of source file
get_source_file_property(MYPROP ${SRC_DIR}/foo.cpp COMPILE_FLAGS)

# Set properties for the source file
set_source_files_properties(${SRC_DIR}/foo.cpp PROPERTIES COMPILE_FLAGS -O2)

# Search for a file in directories
find_path(MYINCLUDE foo.hpp PATHS ${CMAKE_CURRENT_SOURCE_DIR}/include NO_DEFAULT_PATH)

# Search for a library in directories
find_library(MYLIB mylib PATHS ${CMAKE_CURRENT_SOURCE_DIR}/lib NO_DEFAULT_PATH)

# Search for an executable in PATH
find_program(MYPROGRAM myprogram)

# Define project version
set(PROJECT_VERSION "1.0.0")

# Export targets
install(EXPORT mylib DEST
cmake_minimum_required(VERSION 3.10)

project(myproject CXX)

# set a variable
set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)

# add source files
file(GLOB_RECURSE SRCS ${SRC_DIR}/*.cpp)

# Add a library
add_library(mylib SHARED ${SRCS})

# Specify include directories for the library
target_include_directories(mylib PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)

# set libary version
set_target_properties(mylib PROPERTIES VERSION 1.2 SOVERSION 1)

# Add an executable
add_executable(myapp ${SRC_DIR}/main.cpp)

# Link the executable to the library
target_link_libraries(myapp mylib)

# Add include paths for dependent package
find_package(Threads REQUIRED)
target_include_directories(mylib PRIVATE ${CMAKE_THREAD_LIBS_INIT})

# Add preprocessor definitions
add_definitions(-DDEBUG)

# Add compile options
add_compile_options(-Wall -Wextra)

# set variable
set(MYVAR "hello")

# define an option
option(ENABLE_MYFEATURE "Enable my feature" ON)

# add if statement to check option
if(ENABLE_MYFEATURE)
  add_definitions(-DUSE_MYFEATURE)
endif()

# Generate export header
include(GenerateExportHeader)
generate_export_header(mylib)

# Retrieve properties of source file
get_source_file_property(MYPROP ${SRC_DIR}/foo.cpp COMPILE_FLAGS)

# Set properties for the source file
set_source_files_properties(${SRC_DIR}/foo.cpp PROPERTIES COMPILE_FLAGS -O2)

# Search for a file in directories
find_path(MYINCLUDE foo.hpp PATHS ${CMAKE_CURRENT_SOURCE_DIR}/include NO_DEFAULT_PATH)

# Search for a library in directories
find_library(MYLIB mylib PATHS ${CMAKE_CURRENT_SOURCE_DIR}/lib NO_DEFAULT_PATH)

# Search for an executable in PATH
find_program(MYPROGRAM myprogram)

# Define project version
set(PROJECT_VERSION "1.0.0")

# Export targets
install(EXPORT mylib DEST
cmake_minimum_required(VERSION 3.10)

project(myproject CXX)

# set a variable
set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)

# add source files
file(GLOB_RECURSE SRCS ${SRC_DIR}/*.cpp)

# Add a library
add_library(mylib SHARED ${SRCS})

# Specify include directories for the library
target_include_directories(mylib PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)

# set libary version
set_target_properties(mylib PROPERTIES VERSION 1.2 SOVERSION 1)

# Add an executable
add_executable(myapp ${SRC_DIR}/main.cpp)

# Link the executable to the library
target_link_libraries(myapp mylib)

# Add include paths for dependent package
find_package(Threads REQUIRED)
target_include_directories(mylib PRIVATE ${CMAKE_THREAD_LIBS_INIT})

# Add preprocessor definitions
add_definitions(-DDEBUG)

# Add compile options
add_compile_options(-Wall -Wextra)

# set variable
set(MYVAR "hello")

# define an option
option(ENABLE_MYFEATURE "Enable my feature" ON)

# add if statement to check option
if(ENABLE_MYFEATURE)
  add_definitions(-DUSE_MYFEATURE)
endif()

# Generate export header
include(GenerateExportHeader)
generate_export_header(mylib)

# Retrieve properties of source file
get_source_file_property(MYPROP ${SRC_DIR}/foo.cpp COMPILE_FLAGS)

# Set properties for the source file
set_source_files_properties(${SRC_DIR}/foo.cpp PROPERTIES COMPILE_FLAGS -O2)

# Search for a file in directories
find_path(MYINCLUDE foo.hpp PATHS ${CMAKE_CURRENT_SOURCE_DIR}/include NO_DEFAULT_PATH)

# Search for a library in directories
find_library(MYLIB mylib PATHS ${CMAKE_CURRENT_SOURCE_DIR}/lib NO_DEFAULT_PATH)

# Search for an executable in PATH
find_program(MYPROGRAM myprogram)

# Define project version
set(PROJECT_VERSION "1.0.0")

# Export targets
install(EXPORT mylib DESTINATION share/cmake/mylib NAMESPACE My::) export(TARGETS mylib FILE mylib.cmake NAMESPACE My::)

# Install files

install(TARGETS myapp mylib DESTINATION bin) 
install(FILES ${CMAKE\_CURRENT\_SOURCE\_DIR}/include/foo.h DESTINATION include)

# Read a file into a variable

file(READ file.txt MYFILE)

# Write a variable to a file

file(WRITE file.txt "Hello, world!")

# Copy a file

file(COPY input.txt DESTINATION ${CMAKE\_BINARY\_DIR})

# Remove a file

file(REMOVE file.txt)

# Test if a file exists

if(EXISTS file.txt) message("File exists") else() message("File does not exist") endif()

# Define a variable with multiple values

set(MYVAR A B C)

# Loop over the variable

foreach(val ${MYVAR}) message("Value: ${val}") endforeach()
```

