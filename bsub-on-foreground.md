# bsub on foreground

↑ **Parent:** [bsub](bsub.md)

Run `bsub` on foreground, show stdout on host stdout live with an interactive with the [bsub `-I` option](bsub-i-option.md):
```
bsub -I 'echo a;sleep 1;echo b;sleep 1;echo c'; echo done
```
Ctrl + C kills the job on remote as well as locally.

Bibliography:
- [https://superuser.com/questions/46312/wait-for-one-or-all-lsf-jobs-to-complete](https://superuser.com/questions/46312/wait-for-one-or-all-lsf-jobs-to-complete)

## ↑ Ancestors (12)

1. [bsub](bsub.md)
2. [LSF command](lsf-command.md)
3. [IBM Spectrum LSF](ibm-spectrum-lsf.md)
4. [Job scheduler](job-scheduler.md)
5. [High performance computing](high-performance-computing.md)
6. [Computer form factor](computer-form-factor.md)
7. [Computer hardware](computer-hardware-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)
