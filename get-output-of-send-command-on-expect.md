# Get output of `send` command on expect

↑ **Parent:** [Expect HOWTO](expect-howto.md)

This pattern works well:
```
set prompt ">>> "
log_user 0
send "What is quantum field theory?\r"
expect -re "(.+)$prompt"
puts -nonewline [join [lrange [lmap line [split $expect_out(1,string) \n] {regsub {\r$} $line ""}] 1 end] "\n"]
```
Then stdout will contain only the output of the command and nothing else.

Bibliography:
- [https://unix.stackexchange.com/questions/239161/get-the-output-from-expect-script-in-a-variable/792645#792645](https://unix.stackexchange.com/questions/239161/get-the-output-from-expect-script-in-a-variable/792645#792645)
- [https://stackoverflow.com/questions/45210358/expect-output-only-stdout-of-the-command-and-nothing-else/79517903#79517903](https://stackoverflow.com/questions/45210358/expect-output-only-stdout-of-the-command-and-nothing-else/79517903#79517903)
- [https://stackoverflow.com/questions/57975853/how-to-read-the-send-command-output-in-expect-script](https://stackoverflow.com/questions/57975853/how-to-read-the-send-command-output-in-expect-script) title is wrong, OP wants exit status apparently not stdout

## ↑ Ancestors (12)

1. [Expect HOWTO](expect-howto.md)
2. [Expect](expect.md)
3. [List of command line utilities](list-of-command-line-utilities.md)
4. [Command line utility](command-line-utility.md)
5. [Command-line interface](command-line-interface.md)
6. [Computer user-interface](computer-user-interface.md)
7. [Software](software-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)
