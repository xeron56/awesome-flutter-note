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
