# Amazon EC2 GPU

↑ **Parent:** [Amazon EC2 HOWTO](amazon-ec2-howto.md)

As of December 2023, the cheapest instance with an [Nvidia GPU](nvidia-gpu.md) is [g4nd.xlarge](g4nd-xlarge.md), so let's try that out. In that instance, [lspci](lspci.md) contains:
```
00:1e.0 3D controller: NVIDIA Corporation TU104GL [Tesla T4] (rev a1)
```
so we see that it runs a [Nvidia T4](nvidia-t4.md) GPU.

Be careful not to confuse it with [g4ad.xlarge](g4ad-xlarge.md), which has an [AMD GPU](amd-gpu.md) instead. TODO meaning of "ad"? "a" presumably means [AMD](amd.md), but what is the "d"?

Some documentation on which GPU is in each instance can seen at: [https://docs.aws.amazon.com/dlami/latest/devguide/gpu.html](https://docs.aws.amazon.com/dlami/latest/devguide/gpu.html) ([archive](https://web.archive.org/web/20231126224245/https://docs.aws.amazon.com/dlami/latest/devguide/gpu.html)) with a list of which GPUs they have at that random point in time. Can the GPU ever change for a given instance name? Likely not. Also as of December 2023 the list is already outdated, e.g. P5 is now shown, though it is mentioned at: [https://aws.amazon.com/ec2/instance-types/p5/](https://aws.amazon.com/ec2/instance-types/p5/)

When selecting the instance to launch, the GPU does not show anywhere apparently on the instance information page, it is so bad!

Also note that this instance has 4 vCPUs, so on a new account you must first make a customer support request to Amazon to increase your limit from the default of 0 to 4, see also: [https://stackoverflow.com/questions/68347900/you-have-requested-more-vcpu-capacity-than-your-current-vcpu-limit-of-0](https://stackoverflow.com/questions/68347900/you-have-requested-more-vcpu-capacity-than-your-current-vcpu-limit-of-0), otherwise instance launch will fail with:

> You have requested more vCPU capacity than your current vCPU limit of 0 allows for the instance bucket that the specified instance type belongs to. Please visit [http://aws.amazon.com/contact-us/ec2-request](http://aws.amazon.com/contact-us/ec2-request) to request an adjustment to this limit.

When starting up the instance, also select:
- image: [Ubuntu 22.04](ubuntu-22-04.md)
- storage size: 30 GB (maximum free tier allowance)
Once you finally managed to [SSH](secure-shell.md) into the instance, first we have to install drivers and reboot:
```
sudo apt update
sudo apt install nvidia-driver-510 nvidia-utils-510 nvidia-cuda-toolkit
sudo reboot
```
and now running:
```
nvidia-smi
```
shows something like:
```
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 525.147.05   Driver Version: 525.147.05   CUDA Version: 12.0     |
|-------------------------------+----------------------+----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  Tesla T4            Off  | 00000000:00:1E.0 Off |                    0 |
| N/A   25C    P8    12W /  70W |      2MiB / 15360MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+

+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|  No running processes found                                                 |
+-----------------------------------------------------------------------------+
```

If we start from the raw [Ubuntu 22.04](ubuntu-22-04.md), first we have to install drivers:
- [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/install-nvidia-driver.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/install-nvidia-driver.html) official docs
- [https://stackoverflow.com/questions/63689325/how-to-activate-the-use-of-a-gpu-on-aws-ec2-instance](https://stackoverflow.com/questions/63689325/how-to-activate-the-use-of-a-gpu-on-aws-ec2-instance)
- [https://askubuntu.com/questions/1109662/how-do-i-install-cuda-on-an-ec2-ubuntu-18-04-instance](https://askubuntu.com/questions/1109662/how-do-i-install-cuda-on-an-ec2-ubuntu-18-04-instance)
- [https://askubuntu.com/questions/1397934/how-to-install-nvidia-cuda-driver-on-aws-ec2-instance](https://askubuntu.com/questions/1397934/how-to-install-nvidia-cuda-driver-on-aws-ec2-instance)

From there basically everything should just work as normal. E.g. we were able to run a [CUDA hello world](cuda-hello-world.md) just fine along:
```
nvcc inc.cu
./a.out
```

One issue with this setup, besides the time it takes to setup, is that you might also have to pay some network charges as it downloads a bunch of stuff into the instance. We should try out some of the pre-built images. But it is also good to know this pristine setup just in case.

We then managed to run [Ollama](ollama.md) just fine with:
```
curl https://ollama.ai/install.sh | sh
/bin/time ollama run llama2 'What is quantum field theory?'
```
which gave:
```
0.07user 0.05system 0:16.91elapsed 0%CPU (0avgtext+0avgdata 16896maxresident)k
0inputs+0outputs (0major+1960minor)pagefaults 0swaps
```
so way faster than on my local desktop [CPU](central-processing-unit.md), hurray.

After setup from: [https://askubuntu.com/a/1309774/52975](https://askubuntu.com/a/1309774/52975) we were able to run:
```
head -n1000 pap.txt | ARGOS_DEVICE_TYPE=cuda time argos-translate --from-lang en --to-lang fr > pap-fr.txt
```
which gave:
```
77.95user 2.87system 0:39.93elapsed 202%CPU (0avgtext+0avgdata 4345988maxresident)k
0inputs+88outputs (0major+910748minor)pagefaults 0swaps
```
so only marginally better than on [P14s](ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md). It would be fun to see how much faster we could make things on a more powerful GPU.

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

## ← Incoming links (1)

- [Ollama](ollama.md)
