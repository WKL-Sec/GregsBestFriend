
## Building with Visual Studio

Note: GregsBestFriend is only supported on 64-bit Windows systems. 32-bit builds are not recommended or supported.

1. Open the solution file `GregsBestFriend.sln` in Visual Studio.

2. Ensure that the build configuration is set to `Release` and the platform is set to `x64`.

3. Select `Build Solution` from the `Build` menu or press `F7` to build the solution.

4. The compiled executable will be located in the `x64/Release` folder.

Note: If you encounter any errors during the build process, ensure that you have installed the necessary dependencies and that your Visual Studio installation is properly configured.

## Compiler and Visual Studio Version

GregsBestFriend is compiled using Microsoft Visual C++ compiler (cl.exe) that is included with Visual Studio. 

We recommend using the latest version of Visual Studio, which includes the latest version of the compiler. At the time of writing, the current version of Visual Studio is Visual Studio 2022, which includes version 14.3 of the compiler.

Please note that while this project is currently configured to use the Visual Studio 2022 compiler, it may be possible to compile the tool with earlier versions of Visual Studio, though we cannot guarantee that the results will be the same.
