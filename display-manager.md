# Display manager

↑ **Parent:** [Graphical user interface](graphical-user-interface.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Display_manager)

Check which you you have:
```
systemctl status display-manager.service
```
Tested on [Ubuntu 23.10](ubuntu-23-10.md) I see:
```
● gdm.service - GNOME Display Manager
     Loaded: loaded (/lib/systemd/system/gdm.service; static)
     Active: active (running) since Sun 2023-12-24 10:34:50 GMT; 23min ago
    Process: 1827 ExecStartPre=/usr/share/gdm/generate-config (code=exited, status=0/SUCCESS)
   Main PID: 1850 (gdm3)
      Tasks: 4 (limit: 71817)
     Memory: 6.8M
        CPU: 119ms
     CGroup: /system.slice/gdm.service
             └─1850 /usr/sbin/gdm3
```
which means I have [GNOME Display Manager](gnome-display-manager.md).

Bibliography:
- [https://unix.stackexchange.com/questions/20370/is-there-a-simple-linux-command-that-will-tell-me-what-my-display-manager-is](https://unix.stackexchange.com/questions/20370/is-there-a-simple-linux-command-that-will-tell-me-what-my-display-manager-is)
- [https://askubuntu.com/questions/584373/how-to-check-using-the-command-line-which-display-manager-is-running](https://askubuntu.com/questions/584373/how-to-check-using-the-command-line-which-display-manager-is-running)

**Table of contents**

- [GNOME Display Manager](gnome-display-manager.md)

## ↑ Ancestors (8)

1. [Graphical user interface](graphical-user-interface.md)
2. [Computer user-interface](computer-user-interface.md)
3. [Software](software-split.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
