## Building with Clang

To build GregsBestFriend with Clang using mingw64, follow these steps:

1. Download and install [mingw-w64](http://mingw-w64.org/doku.php/download) for your system.
2. Open the mingw-w64 terminal or command prompt.
3. Navigate to the `clang++` folder in the GregsBestFriend repository.
4. Run the following command to build the executable with Clang:

`clang++.exe -s -Os GregsBestFriend.cpp -o GregsBestFriend.exe`

## Compiler Flags

Here's what each flag does:

- `-s`: Strip the executable of all symbol table and relocation information, reducing its size.
- `-Os`: Optimize the executable for size. This flag tells Clang to prioritize reducing the size of the generated code over its execution speed.

5. The resulting `GregsBestFriend.exe` executable should be located in the `clang++` folder.

## Adding Shellcode to GregsBestFriend

Note that adding your own shellcode to GregsBestFriend may cause the program to be detected by some AV/EDR systems, depending on the specifics of your shellcode. To add your own shellcode, follow these steps:

1. Open the `GregsBestFriend.cpp` file in your preferred code editor.
2. Locate the `shellcode()` function, which contains the shellcode that will be executed when the program runs.
3. Replace the existing shellcode with your own shellcode. Make sure that the shellcode is in the form of a byte array, where each byte is represented in hexadecimal format.
4. Save the changes to the `GregsBestFriend.cpp` file.
5. Follow the instructions for building the executable with Clang. Once the executable is built, your shellcode will be executed when the program runs.
