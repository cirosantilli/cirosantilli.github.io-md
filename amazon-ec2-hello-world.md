# Amazon EC2 hello world

↑ **Parent:** [Amazon EC2 HOWTO](amazon-ec2-howto.md)  
🏷️ **Tags:** [Hello world](hello-world-program.md)

Let's get [SSH](secure-shell.md) access, instal a package, and run a server.

As of December 2023 on a `t2.micro` instance, the only one part of free tier at the time with advertised 1 vCPU, 1 GiB RAM, 8 GiB disk for the first 12 months, on [Ubuntu 22.04](ubuntu-22-04.md):
```
$ free -h
               total        used        free      shared  buff/cache   available
Mem:           949Mi       149Mi       210Mi       0.0Ki       590Mi       641Mi
Swap:             0B          0B          0B
$ nproc
1
$ df -h /
Filesystem      Size  Used Avail Use% Mounted on
/dev/root       7.6G  1.8G  5.8G  24% /
```

To install software:
```
sudo apt update
sudo apt install cowsay
cowsay asdf
```

Once HTTP inbound traffic is enabled on security rules for port 80, you can:
```
while true; do printf "HTTP/1.1 200 OK\r\n\r\n`date`: hello from AWS" | sudo nc -Nl 80; done
```
and then you are able to `curl` from your local computer and get the response.

## ↑ Ancestors (13)

1. [Amazon EC2 HOWTO](amazon-ec2-howto.md)
2. [Amazon Elastic Compute Cloud](amazon-elastic-compute-cloud.md)
3. [AWS service](aws-service.md)
4. [Amazon Web Services](amazon-web-services.md)
5. [Cloud computing platform](cloud-computing-platform.md)
6. [Cloud computing](cloud-computing.md)
7. [Computer form factor](computer-form-factor.md)
8. [Computer hardware](computer-hardware-split.md)
9. [Computer](computer-split.md)
10. [Information technology](information-technology.md)
11. [Area of technology](area-of-technology.md)
12. [Technology](technology-split.md)
13. [Ciro Santilli's Homepage](split.md)
