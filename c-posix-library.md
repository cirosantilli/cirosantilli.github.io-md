# C POSIX library

↑ **Parent:** [C library](c-library.md)  
🏷️ **Tags:** [POSIX](posix.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/C_POSIX_library)

Quick overview at [https://stackoverflow.com/questions/1780599/what-is-the-meaning-of-posix/31865755#31865755](https://stackoverflow.com/questions/1780599/what-is-the-meaning-of-posix/31865755#31865755)

Exmples under [c/posix](c/posix):
- [c/posix/signal_return.c](c/posix/signal_return.c): [https://stackoverflow.com/questions/37063212/where-does-signal-handler-return-back-to](https://stackoverflow.com/questions/37063212/where-does-signal-handler-return-back-to)
- [c/posix/inet/pton.c](c/posix/inet/pton.c): `inet_pton` demo. Adapted from `man inet_pton` on [Ubuntu 23.04](ubuntu-23-04.md). Usage:
  ```
  ./pton.out 192.187.1.42
  ```

  Output:
  ```
  0xc0bb012a
  ```

  So we see that the strings was converted to an integer, e.g.:
  - 0xc0 = 192
  - 0xbb = 187
  - 0x01 = 1
  - 0x2a = 42

  See also: [https://stackoverflow.com/questions/1680622/ip-address-to-integer-c/76520978#76520978](https://stackoverflow.com/questions/1680622/ip-address-to-integer-c/76520978#76520978)
- [c/posix/inet/ntop.c](c/posix/inet/ntop.c): `inet_ntop` demo. Adapted from `man inet_pton` on [Ubuntu 23.04](ubuntu-23-04.md). Usage:
  ```
  ./ntop.out 0x01021AA0
  ```

  Output:
  ```
  ./ntop.out 0x01021AA0
  ```

## ↑ Ancestors (10)

1. [C library](c-library.md)
2. [C (programming language)](c-programming-language.md)
3. [List of programming languages](list-of-programming-languages.md)
4. [Programming language](programming-language-split.md)
5. [Software](software-split.md)
6. [Computer](computer-split.md)
7. [Information technology](information-technology.md)
8. [Area of technology](area-of-technology.md)
9. [Technology](technology-split.md)
10. [Ciro Santilli's Homepage](split.md)
