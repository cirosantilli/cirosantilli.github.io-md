# How to report Ubuntu crashes

↑ **Parent:** [Ubuntu HOWTO](ubuntu-howto.md)

Their crash system does not have an amazing user interface.

Tested on [Ubuntu 21.10](ubuntu-21-10.md).

After something crashes, look under `/var/crash` for a crash file, which helps to determine which package to report under on [Launchpad](launchpad-website.md).

E.g. a file `/var/crash/_usr_sbin_gdm3.0.crash` makes you want to file the bug under gdm at: [https://bugs.launchpad.net/ubuntu/+source/gdm/+filebug](https://bugs.launchpad.net/ubuntu/+source/gdm/+filebug)

Then, while reporting the bug, you want to give the developpers access to that `.crash` file. But you can't publicly upload it because it contains memory dumps and could contain secret information. The way to do it is to look at the ID under:
```
sudo cat /var/crash/_usr_sbin_gdm3.0.uploaded
```
Ubuntu's crash report system has already uploaded the `.crash` for you, so you just have to confirm it and give the ID on the ticket.

You can view a list of all your uploaded errors at:
```
xdg-open https://errors.ubuntu.com/user/$(sudo cat /var/lib/whoopsie/whoopsie-id)
```
and each of those contain a link to:
```
https://errors.ubuntu.com/oops/<.uloaded error id>
```
which you yourself cannot see.

[https://askubuntu.com/questions/434431/how-can-i-read-a-crash-file-from-var-crash](https://askubuntu.com/questions/434431/how-can-i-read-a-crash-file-from-var-crash) asks how to read the `.crash` files.

Running:
```
sudo apport-unpack /var/crash/_usr_sbin_gdm3.0.crash /tmp/app
```
splits it up into a few files, but does not make any major improvements.

`apport-retrace`
```
sudo apt install apport-retrace
sudo chmod 666 /var/crash/_usr_sbin_gdm3.0.crash
apport-retrace -g /var/crash/_usr_sbin_gdm3.0.crash
```
opens GDB with the core dump. Debug symbols are supplied as separate packages, which is a really cool idea: so you should be able to download them after the crash to see symbols. [https://askubuntu.com/questions/487222/how-to-install-debug-symbols-for-installed-packages](https://askubuntu.com/questions/487222/how-to-install-debug-symbols-for-installed-packages) mentions how to install them. Official docs at: [https://wiki.ubuntu.com/DebuggingProgramCrash#Debug_Symbol_Packages](https://wiki.ubuntu.com/DebuggingProgramCrash#Debug_Symbol_Packages)

Tried:
```
echo "deb http://ddebs.ubuntu.com $(lsb_release -cs) main restricted universe multiverse" | sudo tee -a /etc/apt/sources.list.d/ddebs.list
echo -e "deb http://ddebs.ubuntu.com $(lsb_release -cs)-updates main restricted universe multiverse\ndeb http://ddebs.ubuntu.com $(lsb_release -cs)-proposed main restricted universe multiverse" | sudo tee -a /etc/apt/sources.list.d/ddebs.list
sudo apt install ubuntu-dbgsym-keyring
```
but then `sudo apt update` fails with:
```
E: The repository 'http://ddebs.ubuntu.com impish-security Release' does not have a Release file.
```

## ↑ Ancestors (13)

1. [Ubuntu HOWTO](ubuntu-howto.md)
2. [Ubuntu](ubuntu.md)
3. [List of Linux distributions](list-of-linux-distributions.md)
4. [Linux](linux.md)
5. [List of operating systems](list-of-operating-systems.md)
6. [Operating system](operating-system.md)
7. [Systems programming](systems-programming-split.md)
8. [Software](software-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)
