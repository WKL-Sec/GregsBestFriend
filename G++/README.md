## Building with g++

To build GregsBestFriend with g++, follow these steps:

1. Download and install [mingw-w64](https://github.com/niXman/mingw-builds-binaries) for your system.
2. Open the mingw-w64 terminal or command prompt.
3. Navigate to the `g++` folder in the GregsBestFriend repository.
4. Run the following command to build the executable with g++:

`g++.exe -Os -s GregsBestFriend.cpp -static -static-libgcc -static-libstdc++ -Wl,--subsystem,windows -o GregsBestFriend.exe`

## Compiler Flags

Here's what each flag does:

- `-Os`: Optimize the executable for size. This flag tells g++ to prioritize reducing the size of the generated code over its execution speed.
- `-s`: Strip the executable of all symbol table and relocation information, reducing its size.
- `-static`: Link all libraries statically, so that they are included in the executable.
- `-static-libgcc`: Link the GCC library statically.
- `-static-libstdc++`: Link the C++ standard library statically.
- `-Wl,--subsystem,windows`: Set the subsystem to Windows, so that the executable runs as a GUI program instead of a console application.

5. The resulting `GregsBestFriend.exe` executable should be located in the `g++` folder.

## Adding Shellcode to GregsBestFriend

To add your own shellcode to GregsBestFriend, follow these steps:

1. Open the `GregsBestFriend.cpp` file in your preferred code editor.
2. Locate the `shellcode()` function, which contains the shellcode that will be executed when the program runs.
3. Replace the existing shellcode with your own shellcode. Make sure that the shellcode is in the form of a byte array, where each byte is represented in hexadecimal format.
4. Save the changes to the `GregsBestFriend.cpp` file.
5. Follow the instructions for building the executable with your desired compiler. Once the executable is built, your shellcode will be executed when the program runs.

Note that adding your own shellcode to GregsBestFriend may cause the program to be detected by some AV/EDR systems, depending on the specifics of your shellcode. It is recommended that you test your modified version of GregsBestFriend against a range of AV/EDR systems to ensure that it remains effective in bypassing detection.
