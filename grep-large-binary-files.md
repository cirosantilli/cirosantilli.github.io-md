# grep large binary files

↑ **Parent:** [`grep`](grep.md)

This is a weak point of grep, it can't handle large lines that don't fit fully into memory:
- [https://superuser.com/questions/1703029/is-there-a-limit-for-a-line-length-for-grep-command-to-process-correctly](https://superuser.com/questions/1703029/is-there-a-limit-for-a-line-length-for-grep-command-to-process-correctly) what is the grep line limit?
- [https://unix.stackexchange.com/questions/223078/best-way-to-grep-big-binary-file/758528#758528](https://unix.stackexchange.com/questions/223078/best-way-to-grep-big-binary-file/758528#758528) Ciro's `bgrep` canon
- large not required but mentioning bgrep anyways:
  - [https://superuser.com/questions/1368263/use-grep-for-a-long-line-to-get-the-part-of-the-line/1811969#1811969](https://superuser.com/questions/1368263/use-grep-for-a-long-line-to-get-the-part-of-the-line/1811969#1811969)
  - [https://unix.stackexchange.com/questions/217936/equivalent-command-to-grep-binary-files/758544#758544](https://unix.stackexchange.com/questions/217936/equivalent-command-to-grep-binary-files/758544#758544)
  - [https://stackoverflow.com/questions/2034799/how-to-truncate-long-matching-lines-returned-by-grep-or-ack/77263826#77263826](https://stackoverflow.com/questions/2034799/how-to-truncate-long-matching-lines-returned-by-grep-or-ack/77263826#77263826)
  - [https://stackoverflow.com/questions/9988379/how-to-grep-a-text-file-which-contains-some-binary-data](https://stackoverflow.com/questions/9988379/how-to-grep-a-text-file-which-contains-some-binary-data) leaving this one alone for now
- [https://stackoverflow.com/questions/65674717/how-to-check-if-a-binary-file-is-contained-inside-another-binary-from-the-linux](https://stackoverflow.com/questions/65674717/how-to-check-if-a-binary-file-is-contained-inside-another-binary-from-the-linux) search pattern from file

## ↑ Ancestors (11)

1. [`grep`](grep.md)
2. [POSIX](posix.md)
3. [UNIX](unix.md)
4. [Operating system](operating-system.md)
5. [Systems programming](systems-programming-split.md)
6. [Software](software-split.md)
7. [Computer](computer-split.md)
8. [Information technology](information-technology.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
