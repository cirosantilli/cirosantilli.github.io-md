# Software Guard Extensions

↑ **Parent:** [Trusted execution environment](trusted-execution-environment.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Software_Guard_Extensions)

The hole point of [Intel SGX](software-guard-extensions.md) is to allow users to be certain that a certain code was executed in a remove server that they rent but don't own, like [AWS](amazon-web-services.md). Even if [AWS](amazon-web-services.md) wanted to be malicious, they would still not be able to modify your read your input, output nor modify the program.

The way this seems to work is as follows.

Each chip has its own unique private key embedded in the chip. There is no way for software to read that private key, only the hardware can read it, and Intel does not know that private key, only the corrsponding public one. The entire safety of the system relies on this key never ever leaking to anybody, even if they have the CPU in their hands. A big question is if there are physical forensic methods, e.g. using [electron microscopes](electron-microscope.md), that would allow this key to be identified.

Then, using that private key, you can create enclaves.

Once you have an enclave, you can load a certain code to run into the enclave.

Then, non-secure users can give inputs to that enclave, and as an output, they get not only the output result, but also a public key certificate based on the internal private key.

This certificates states:
- given input X
- program Y
- produced output Z
and that can then be verified online on Intel's website, since they keep a list of public keys. This service is called attestation.

So, if the certificate is verified, you can be certain that a your input was ran by a specific code.

Additionally:
- you can public key encrypt your input to the enclave with the public key, and then ask the enclave to send output back encrypted to your key. This way the hardware owner cannot read neither the input not the output
- all data stored on RAM is encrypted by the enclave, to prevent attacks that rely on using a modified RAM that logs data

## ↑ Ancestors (12)

1. [Trusted execution environment](trusted-execution-environment.md)
2. [CPU feature](cpu-feature.md)
3. [Central processing unit](central-processing-unit.md)
4. [Type of processor](type-of-processor.md)
5. [Processor (computing)](processor-computing.md)
6. [Computer hardware component type](computer-hardware-component-type.md)
7. [Computer hardware](computer-hardware-split.md)
8. [Computer](computer-split.md)
9. [Information technology](information-technology.md)
10. [Area of technology](area-of-technology.md)
11. [Technology](technology-split.md)
12. [Ciro Santilli's Homepage](split.md)
