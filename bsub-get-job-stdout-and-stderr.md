# bsub get job stdout and stderr

↑ **Parent:** [bsub](bsub.md)

By default, LSF only sends you an email with the stdout and stderr included in it, and does not show or store anything locally.

One option to store things locally is to use:
```
bsub -oo stdout.log -eo stderr.log 'echo myout; echo myerr 1>&2'
```
as documented at:
- [https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=options-eo](https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=options-eo)
- [https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=options-oo](https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=options-oo)
Or to use files with the job id in them:
```
bsub -oo %J.out -eo %J.err 'echo myout; echo myerr 1>&2'
```

By default `bsub -oo`:
- also contains the LSF metadata in addition to the actual submitted process stdout
- prevents the completion email from being sent
To get just the stdout to the file, use `bsub -N -oo` which:
- stores only stdout on the file
- re-enables the completion email
as mentioned at:
- [https://www.ibm.com/support/pages/include-only-job-stdout-lsf-job-output-file](https://www.ibm.com/support/pages/include-only-job-stdout-lsf-job-output-file)
- [https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=o-n](https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=o-n)

Another option is to run with the [bsub `-I` option](bsub-i-option.md):
```
bsub -I 'echo a;sleep 1;echo b;sleep 1;echo c'
```
This immediately prints stdout and stderr to the terminal.

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
