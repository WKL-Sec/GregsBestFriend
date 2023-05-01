## Building with Clang LLVM

Clang LLVM is a powerful and flexible compiler that can be used to build Windows executables with high detection evasion rates. One of the advantages of Clang LLVM on Windows is that it uses the Microsoft Visual C++ runtime library, making it easier to integrate with Windows applications.

To build with Clang LLVM, use the following command:

`clang++ -Oz GregsBestFriend.cpp -o GregsBestFriend.exe`

Additional command-line options that can result in lower detection rates lower detection rates by AV/EDR software include:

- `-Os` (both GCC and LLVM): Optimize for size.
- `-Oz` (only LLVM): Optimize for size even more than `-Os`.
- `-fno-unroll-loops`: Do not unroll loops.
- `-fno-exceptions` and `-fno-rtti`: Disable C++ exceptions and RTTI (Run-Time Type Information).
- `-finline-limit=n` (GCC) and `-mllvm -inline-threshold=n` (LLVM): Adjust the inlining threshold. Lowering this value can help prevent stack overflows and improve obfuscation.
- `-flto` and `-flto=thin` (only LLVM): Perform link-time optimization. `-flto=thin` can reduce compilation time but may produce larger binaries.
- `-fmerge-functions` (only LLVM): Merge identical functions into a single one.

Note that these options may not work for every program or system configuration, and may require further experimentation and testing to determine the optimal settings for your use case.

## Stripping

To reduce the size of the binary and remove symbols, you can use the `llvm-strip` tool that comes with Clang LLVM. This tool allows you to strip symbols and debug information from an executable.

Here is an example command to use `llvm-strip` to strip symbols and debug information:

`llvm-strip.exe -s GregsBestFriend.exe -o temp.exe`

This command will create a new executable named `temp.exe` with stripped symbols and debug information.

Note that stripping symbols can make debugging more difficult, so it should be used only for release builds. Additionally, be sure to test the stripped executable thoroughly to ensure that it works as expected.

It is also worth noting that using `-s` flag with `clang` LLVM on Windows does not work. Instead, you can use `-Os` or `-Oz` for optimizing the binary size.

