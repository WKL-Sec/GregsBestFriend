## Building with cl.exe

To build GregsBestFriend with `cl.exe`, follow these steps:

1. Open a Developer Command Prompt for Visual Studio.

2. Navigate to the directory containing `GregsBestFriend.cpp`.

3. Run the following command to compile `GregsBestFriend.cpp` into an object file:

```cl.exe /TP /O1 /GS- /GL /EHsc /c GregsBestFriend.cpp`

4. Run the following command to link the object file and create the executable:

```link.exe GregsBestFriend.obj /SUBSYSTEM:CONSOLE /NODEFAULTLIB:msvcrt.lib /MT:libcmt.lib /OUT:GregsBestFriend.exe /OPT:REF /OPT:ICF`

5. To add your own shellcode to the code, replace the `shellcode` array in the `shellcode()` function with your own shellcode.

### Explanation of Compiler Flags

- `/TP`: Specifies that the source file is a C++ file.
- `/O1`: Specifies optimization for minimum code size.
- `/GS-`: Disables buffer security checks.
- `/GL`: Enables whole program optimization.
- `/EHsc`: Specifies the type of exception handling model to be used.
- `/c`: Compiles the source file and creates an object file.

### Explanation of Linker Flags

- `/SUBSYSTEM:CONSOLE`: Specifies that the executable is a console application.
- `/NODEFAULTLIB:msvcrt.lib`: Prevents linking against the default C runtime library.
- `/MT:libcmt.lib`: Specifies the C runtime library to be used.
- `/OUT:GregsBestFriend.exe`: Specifies the output file name.
- `/OPT:REF`: Eliminates unused function and data code.
- `/OPT:ICF`: Identifies and eliminates redundant code.

