# Computer hardware

↑ **Parent:** [Computer](computer.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computer_hardware)

**Table of contents**

- [Moore's law](#moore-s-law)
- [Semiconductor device fabrication](#semiconductor-device-fabrication)
  - [Semiconductor research institute](#semiconductor-research-institute)
    - [IMEC](#imec)
    - [Computer research institute](#computer-research-institute)
      - [Xerox PARC](#xerox-parc)
  - [Semiconductor equipment maker](#semiconductor-equipment-maker)
    - [ASML Holding](#asml-holding)
      - [ASM International](#asm-international)
    - [Applied Materials](#applied-materials)
  - [Power, performance and area](#power-performance-and-area)
  - [Wafer (electronics)](#wafer-electronics)
    - [Czochralski method](#czochralski-method)
  - [Semiconductor fabrication plant](#semiconductor-fabrication-plant)
    - [Company with a semiconductor fabrication plant](#company-with-a-semiconductor-fabrication-plant)
      - [Fairchild Semiconductor](#fairchild-semiconductor)
      - [GlobalFoundries](#globalfoundries)
      - [Infineon Technologies](#infineon-technologies)
      - [SMIC](#smic)
      - [TSMC](#tsmc)
    - [Semiconductor fabrication step](#semiconductor-fabrication-step)
      - [Chemical vapor deposition](#chemical-vapor-deposition)
      - [Photolithography](#photolithography)
        - [Extreme ultraviolet lithography](#extreme-ultraviolet-lithography)
        - [Photomask](#photomask)
  - [Standard cell library](#standard-cell-library)
    - [Open source standard cell library](#open-source-standard-cell-library)
  - [Electronic design automation](#electronic-design-automation)
    - [Electronic design automation phase](#electronic-design-automation-phase)
      - [Logic synthesis](#logic-synthesis)
      - [Place and route](#place-and-route)
        - [Integrated circuit layout](#integrated-circuit-layout)
          - [GDSII](#gdsii)
    - [EDA company](#eda-company)
      - [Cadence Design Systems](#cadence-design-systems)
        - [Alberto Sangiovanni-Vincentelli](#alberto-sangiovanni-vincentelli)
      - [Mentor Graphics](#mentor-graphics)
      - [Synopsys](#synopsys)
    - [Open source EDA tool](#open-source-eda-tool)
      - [qflow](#qflow)
  - [Semiconductor process node](#semiconductor-process-node)
  - [Semiconductor device fabrication bibliography](#semiconductor-device-fabrication-bibliography)
    - [Asianometry](#asianometry)
- [Integrated circuit](#integrated-circuit)
  - [Interconnect (integrated\_circuits)](#interconnect-integrated-circuits)
  - [Application-specific integrated circuit](#application-specific-integrated-circuit)
  - [System on a chip](#system-on-a-chip)
- [Register transfer level](#register-transfer-level)
  - [High-level synthesis](#high-level-synthesis)
  - [Fabless manufacturing](#fabless-manufacturing)
    - [Fabless semiconductor company](#fabless-semiconductor-company)
  - [Logic gate](#logic-gate)
    - [Truth table](#truth-table)
  - [Verilog](#verilog)
    - [Value change dump](#value-change-dump)
    - [Verilator](#verilator)
      - [Verilator interactive example](#verilator-interactive-example)
  - [VHDL](#vhdl)
    - [GHDL](#ghdl)
- [Microarchitecture](#microarchitecture)
  - [Microarchitectural benchmark](#microarchitectural-benchmark)
    - [CPU microbenchmark](#cpu-microbenchmark)
      - [c/inc\_loop.c](#_file/c/inc_loop.c)
      - [c/inc\_loop\_asm.c](#_file/c/inc_loop_asm.c)
      - [c/inc\_loop\_asm\_n.sh](#_file/c/inc_loop_asm_n.sh)
      - [c/mul\_loop\_asm.c](#_file/c/mul_loop_asm.c)
      - [c/mul\_loop\_asm\_2.c](#_file/c/mul_loop_asm_2.c)
      - [c/mul\_loop\_asm\_n.sh](#_file/c/mul_loop_asm_n.sh)
- [Computer hardware component type](#computer-hardware-component-type)
  - [Processor (computing)](#processor-computing)
    - [Instruction set architecture](#instruction-set-architecture)
      - [Assembly language](#assembly-language)
        - [Assembler (computing)](#assembler-computing)
          - [GNU Assembler](#gnu-assembler)
      - [Calling convention](#calling-convention)
      - [List of instruction set architectures](#list-of-instruction-set-architectures)
        - [One instruction set computer](#one-instruction-set-computer)
        - [ARM architecture family](#arm-architecture-family)
        - [PowerPC](#powerpc)
        - [RISC-V](#risc-v)
          - [RISC-V International](#risc-v-international)
          - [RISC-V vendor](#risc-v-vendor)
            - [Codasip](#codasip)
            - [SiFive](#sifive)
            - [SiPearl](#sipearl)
          - [RISC-V timer](#risc-v-timer)
            - [riscv/timer.S](#_file/riscv/timer.S)
          - [RISC-V priviledged ISA](#risc-v-priviledged-isa)
            - [RISC-V MSTATUS register](#risc-v-mstatus-register)
              - [RISC-V MSTATUS.MIE field](#risc-v-mstatus-mie-field)
        - [x86](#x86)
          - [x86 Paging Tutorial](x86-paging.md)
            - [Sample code](x86-paging.md#sample-code)
            - [Intel manual](x86-paging.md#intel-manual)
            - [Application](x86-paging.md#application)
            - [Hardware implementation](x86-paging.md#hardware-implementation)
            - [Segmentation](x86-paging.md#segmentation)
            - [Example: simplified single-level paging scheme](x86-paging.md#example-simplified-single-level-paging-scheme)
              - [Single level paging scheme visualization](x86-paging.md#single-level-paging-scheme-visualization)
              - [Single level paging scheme numerical translation example](x86-paging.md#single-level-paging-scheme-numerical-translation-example)
              - [Multiple addresses translate to a single physical address](x86-paging.md#multiple-addresses-translate-to-a-single-physical-address)
              - [Identity mapping](x86-paging.md#identity-mapping)
              - [Page faults](x86-paging.md#page-faults)
              - [Page table entries](x86-paging.md#page-table-entries)
              - [Page size choice](x86-paging.md#page-size-choice)
            - [Example: multi-level paging scheme](x86-paging.md#example-multi-level-paging-scheme)
              - [The problem with single-level paging](x86-paging.md#the-problem-with-single-level-paging)
              - [K-ary trees to the rescue](x86-paging.md#k-ary-trees-to-the-rescue)
              - [Why not a balanced tree](x86-paging.md#why-not-a-balanced-tree)
              - [How the K-ary tree is used in x86](x86-paging.md#how-the-k-ary-tree-is-used-in-x86)
              - [Multi-level paging scheme numerical translation example](x86-paging.md#multi-level-paging-scheme-numerical-translation-example)
            - [64-bit architectures](x86-paging.md#64-bit-architectures)
            - [PAE](x86-paging.md#pae)
            - [PSE](x86-paging.md#pse)
            - [PAE and PSE page table schemes](x86-paging.md#pae-and-pse-page-table-schemes)
            - [TLB](x86-paging.md#tlb)
              - [Basic TLB operation](x86-paging.md#basic-tlb-operation)
              - [TLB replacement policy](x86-paging.md#tlb-replacement-policy)
              - [CAM](x86-paging.md#cam)
              - [Invalidating TLB entries](x86-paging.md#invalidating-tlb-entries)
            - [Linux kernel usage](x86-paging.md#linux-kernel-usage)
              - [Play with physical addresses in Linux](x86-paging.md#play-with-physical-addresses-in-linux)
              - [Kernel vs process memory layout](x86-paging.md#kernel-vs-process-memory-layout)
              - [Process memory layout](x86-paging.md#process-memory-layout)
              - [Copy-on-write](x86-paging.md#copy-on-write)
              - [Linux source tree](x86-paging.md#linux-source-tree)
            - [Memory management unit](x86-paging.md#memory-management-unit)
            - [Second Level Address Translation](x86-paging.md#second-level-address-translation)
            - [Other architectures](x86-paging.md#other-architectures)
              - [ARM](x86-paging.md#arm)
            - [Bibliography](x86-paging.md#bibliography)
          - [x86 custom instructions](#x86-custom-instructions)
        - [Y86](#y86)
    - [Type of processor](#type-of-processor)
      - [Central processing unit](#central-processing-unit)
        - [Arithmetic logic unit](#arithmetic-logic-unit)
        - [Microcontroller](#microcontroller)
          - [Microcontroller emulation](#microcontroller-emulation)
            - [Microcontroller plus circuit emulation](#microcontroller-plus-circuit-emulation)
              - [Proteus Design Suite](#proteus-design-suite)
              - [Wokwi](#wokwi)
          - [Microcontroller vs CPU](#microcontroller-vs-cpu)
        - [CPU architecture](#cpu-architecture)
          - [Superscalar processor](#superscalar-processor)
            - [CPU functional unit](#cpu-functional-unit)
          - [Instruction pipelining](#instruction-pipelining)
            - [Educational CPU microarchitecture simulator](#educational-cpu-microarchitecture-simulator)
              - [freess](#freess)
              - [JavaScript CPU microarchitecture simulator](#javascript-cpu-microarchitecture-simulator)
                - [y86.js.org](#y86-js-org)
                - [WebRISC-V](#webrisc-v)
            - [Hazard (computer architecture)](#hazard-computer-architecture)
              - [Pipeline stall](#pipeline-stall)
            - [Classic RISC pipeline](#classic-risc-pipeline)
        - [Microprocessor](#microprocessor)
        - [CPU feature](#cpu-feature)
          - [Trusted execution environment](#trusted-execution-environment)
            - [Software Guard Extensions](#software-guard-extensions)
      - [Field-programmable gate array](#field-programmable-gate-array)
        - [FPGA company](#fpga-company)
          - [Xilinx](#xilinx)
      - [Graphics processing unit](#graphics-processing-unit)
        - [Discrete and integrated GPUs](#discrete-and-integrated-gpus)
          - [Discrete GPU](#discrete-gpu)
          - [Integrated GPU](#integrated-gpu)
        - [Video random-access memory](#video-random-access-memory)
        - [General-purpose computing on graphics processing units](#general-purpose-computing-on-graphics-processing-units)
          - [Open source GPU compute benchmark](#open-source-gpu-compute-benchmark)
          - [GPU compute library](#gpu-compute-library)
            - [CUDA](#cuda)
              - [CUDA hello world](#cuda-hello-world)
            - [OpenCL](#opencl)
            - [ROCm](#rocm)
              - [ROCm on Ubuntu](#rocm-on-ubuntu)
      - [AI accelerator](#ai-accelerator)
        - [Amazon AI accelerator silicon](#amazon-ai-accelerator-silicon)
        - [Tensor Processing Unit](#tensor-processing-unit)
        - [Tesla Dojo](#tesla-dojo)
  - [I/O device](#i-o-device)
    - [Punched card](#punched-card)
      - [Hollerith tabulating machine](#hollerith-tabulating-machine)
    - [Computer input device](#computer-input-device)
    - [Computer data storage](#computer-data-storage)
      - [Computer data storage software](#computer-data-storage-software)
        - [Filesystem](#filesystem)
          - [Clustered file system](#clustered-file-system)
            - [9P (protocol)](#9p-protocol)
            - [Network File System](#network-file-system)
          - [Computer file](#computer-file)
            - [File signature](#file-signature)
      - [Computer data storage hardware](#computer-data-storage-hardware)
        - [Tape drive](#tape-drive)
        - [Volatile memory](#volatile-memory)
          - [Random-access memory](#random-access-memory)
            - [Static random-access memory](#static-random-access-memory)
            - [Dynamic random-access memory](#dynamic-random-access-memory)
              - [Synchronous dynamic random-access memory](#synchronous-dynamic-random-access-memory)
                - [DDR SDRAM](#ddr-sdram)
            - [Magnetoresistive RAM](#magnetoresistive-ram)
        - [Non-volatile memory](#non-volatile-memory)
          - [Disk storage](#disk-storage)
            - [Disk read-and-write head](#disk-read-and-write-head)
              - [Magnetoresistive disk head](#magnetoresistive-disk-head)
          - [Optical storage](#optical-storage)
          - [Solid-state storage](#solid-state-storage)
            - [Erase SSD securely](#erase-ssd-securely)
        - [Solid-state drive](#solid-state-drive)
          - [Flash memory](#flash-memory)
    - [Peripheral](#peripheral)
      - [Computer mouse](#computer-mouse)
      - [Computer keyboard](#computer-keyboard)
        - [Keyboard layout](#keyboard-layout)
          - [QWERTY](#qwerty)
          - [Dvorak keyboard layout](#dvorak-keyboard-layout)
        - [Computer keyboard model](#computer-keyboard-model)
          - [Kinesis Advantage keyboard](#kinesis-advantage-keyboard)
          - [Kinesis Advantage 2 keyboard](#kinesis-advantage-2-keyboard)
      - [Display device](#display-device)
        - [Blinkenlights](#blinkenlights)
        - [E Ink](#e-ink)
          - [Amazon Kindle](#amazon-kindle)
          - [Remarkable (tablet)](#remarkable-tablet)
            - [Remarkable 2](#remarkable-2)
        - [Teleprinter](#teleprinter)
      - [Webcam](#webcam)
      - [Peripheral interface](#peripheral-interface)
        - [PCI](#pci)
          - [PCIe](#pcie)
          - [lspci](#lspci)
            - [pciutils](#pciutils)
            - [Get vendor and device ID for each PCI device](#get-vendor-and-device-id-for-each-pci-device)
        - [USB](#usb)
          - [USB Micro-B](#usb-micro-b)
          - [USB-C](#usb-c)
- [Computer form factor](#computer-form-factor)
  - [Embedded system](#embedded-system)
  - [Distributed computing](#distributed-computing)
    - [Fog computing](#fog-computing)
      - [Charity Engine](#charity-engine)
      - [Folding@home](#folding-at-home)
      - [SETI@home](#seti-at-home)
      - [Is fog computing more efficient than cloud computing?](#is-fog-computing-more-efficient-than-cloud-computing)
  - [Mainframe computer](#mainframe-computer)
  - [Cloud computing](#cloud-computing)
    - [Cloud computing market share](#cloud-computing-market-share)
    - [Hyperscale computing](#hyperscale-computing)
    - [Cloud computing platform](#cloud-computing-platform)
      - [Amazon Web Services](#amazon-web-services)
        - [aws-cli](#aws-cli)
        - [AWS service](#aws-service)
          - [Amazon Athena](#amazon-athena)
          - [Amazon Redshift](#amazon-redshift)
          - [Amazon S3](#amazon-s3)
            - [Browse S3 bucket on web browser](#browse-s3-bucket-on-web-browser)
          - [Amazon Elastic Compute Cloud](#amazon-elastic-compute-cloud)
            - [Amazon EC2 HOWTO](#amazon-ec2-howto)
              - [Amazon EC2 hello world](#amazon-ec2-hello-world)
              - [Amazon EC2 GPU](#amazon-ec2-gpu)
            - [Amazon Machine Image](#amazon-machine-image)
              - [List of AWS AMIs](#list-of-aws-amis)
                - [AWS Deep Learning Base GPU AMI (Ubuntu 20.04)](#aws-deep-learning-base-gpu-ami-ubuntu-20-04)
            - [Amazon Elastic Block Store](#amazon-elastic-block-store)
              - [Laucnh Amazin EC2 with existing EBS volume](#laucnh-amazin-ec2-with-existing-ebs-volume)
            - [EC2 instance store volume](#ec2-instance-store-volume)
            - [vCPU](#vcpu)
            - [EC2 instance type](#ec2-instance-type)
              - [g4ad.xlarge](#g4ad-xlarge)
              - [g4nd.xlarge](#g4nd-xlarge)
              - [g5.xlarge](#g5-xlarge)
      - [Alibaba Cloud](#alibaba-cloud)
      - [Google Cloud Platform](#google-cloud-platform)
    - [Type of cloud computing](#type-of-cloud-computing)
      - [Infrastructure as a service](#infrastructure-as-a-service)
      - [Platform as a service](#platform-as-a-service)
        - [AWS Elastic Beanstalk](#aws-elastic-beanstalk)
        - [Heroku](#heroku)
          - [Send free emails from Heroku](#send-free-emails-from-heroku)
  - [High performance computing](#high-performance-computing)
    - [Job scheduler](#job-scheduler)
      - [Borg (cluster manager)](#borg-cluster-manager)
      - [IBM Spectrum LSF](#ibm-spectrum-lsf)
        - [LSF get version](#lsf-get-version)
        - [LSF command](#lsf-command)
          - [bsub](#bsub)
            - [bsub get job stdout and stderr](#bsub-get-job-stdout-and-stderr)
            - [bsub on foreground](#bsub-on-foreground)
            - [bsub option](#bsub-option)
            - [bsub `-I` option](#bsub-i-option)
          - [bpeek](#bpeek)
          - [bkill](#bkill)
          - [bkill all jobs](#bkill-all-jobs)
    - [Slurm Workload Manager](#slurm-workload-manager)
    - [Supercomputer](#supercomputer)
      - [Exascale computing](#exascale-computing)
        - [Exascale hypothesis](#exascale-hypothesis)
      - [TOP500](#top500)
      - [Supercomputer by owner](#supercomputer-by-owner)
        - [Oak Ridge supercomputer](#oak-ridge-supercomputer)
          - [Frontier (supercomputer)](#frontier-supercomputer)
      - [Intel supercomputer market share](#intel-supercomputer-market-share)
  - [Personal computer](#personal-computer)
    - [Laptop](#laptop)
    - [Desktop computer](#desktop-computer)
    - [Mobile phone](#mobile-phone)
      - [History of mobile phone](#history-of-mobile-phone)
      - [The first application of mobile phones was in motor vehicles](#the-first-application-of-mobile-phones-was-in-motor-vehicles)
      - [Smartphone](#smartphone)
      - [Mobile app](#mobile-app)
  - [Workstation](#workstation)
- [Computer manufacturer](#computer-manufacturer)
  - [Dell](#dell)
  - [Lenovo](#lenovo)
    - [ThinkPad](#thinkpad)
      - [ThinkPad series](#thinkpad-series)
  - [Raspberry Pi Foundation](#raspberry-pi-foundation)
    - [Raspberry Pi Foundation project](#raspberry-pi-foundation-project)
      - [Raspberry Pi OS](#raspberry-pi-os)
      - [Raspberry Pi](#raspberry-pi)
        - [Raspberry Pi 1](#raspberry-pi-1)
        - [Raspberry Pi 2](#raspberry-pi-2)
        - [Raspberry Pi 3](#raspberry-pi-3)
        - [Raspberry Pi Pico](#raspberry-pi-pico)
          - [Raspberry Pi Pico getting started](#raspberry-pi-pico-getting-started)
            - [Flash the Raspberry Pi Pico](#flash-the-raspberry-pi-pico)
              - [picotool](#picotool)
          - [Run Zephyr on Raspberry Pi Pico](#run-zephyr-on-raspberry-pi-pico)
            - [Run Zephyr on Raspberry Pi Pico W](#run-zephyr-on-raspberry-pi-pico-w)
          - [Raspberry Pi Pico variant](#raspberry-pi-pico-variant)
            - [Raspberry Pi Pico 1](#raspberry-pi-pico-1)
            - [Raspberry Pi Pico H](#raspberry-pi-pico-h)
            - [Raspberry Pi Pico W](#raspberry-pi-pico-w)
              - [Raspberry Pi Pico W UART](#raspberry-pi-pico-w-uart)
              - [Program Raspberry Pi Pico W with X](#program-raspberry-pi-pico-w-with-x)
                - [Program Raspberry Pi Pico W with MicroPython](#program-raspberry-pi-pico-w-with-micropython)
                  - [How to run a MicroPython script from a file on the Raspberry Pi Pico W from the command line?](#how-to-run-a-micropython-script-from-a-file-on-the-raspberry-pi-pico-w-from-the-command-line)
                  - [MicroPython connection tool](#micropython-connection-tool)
                    - [ampy](#ampy)
                    - [rshell](#rshell)
                      - [How to exit from repl in rshell?](#how-to-exit-from-repl-in-rshell)
                  - [Raspberry Pi Pico W freezes a few seconds after after screen disconnects from UART](#raspberry-pi-pico-w-freezes-a-few-seconds-after-after-screen-disconnects-from-uart)
                  - [Program Raspberry Pi Pico W with MicroPython code from the command line](#program-raspberry-pi-pico-w-with-micropython-code-from-the-command-line)
                  - [Program the Raspberry Pi Pico W with MicroPython from Thonny](#program-the-raspberry-pi-pico-w-with-micropython-from-thonny)
                  - [Raspberry Pi Pico W MicroPython example](#raspberry-pi-pico-w-micropython-example)
                    - [rpi-pico-w/upython/blink.py](#_file/rpi-pico-w/upython/blink.py)
                    - [rpi-pico-w/upython/blink\_gpio.py](#_file/rpi-pico-w/upython/blink_gpio.py)
                    - [rpi-pico-w/upython/uart.py](#_file/rpi-pico-w/upython/uart.py)
                    - [rpi-pico-w/upython/adc.py](#_file/rpi-pico-w/upython/adc.py)
                    - [rpi-pico-w/upython/thermistor\_fan\_control.py](#_file/rpi-pico-w/upython/thermistor_fan_control.py)
                - [Program Raspberry Pi Pico W with C](#program-raspberry-pi-pico-w-with-c)
- [Semiconductor industry](#semiconductor-industry)
  - [Semiconductor industry bibliography](#semiconductor-industry-bibliography)
    - [Crystal Fire: The Birth of the Information Age](#crystal-fire-the-birth-of-the-information-age)
  - [Film about the semiconductor industry](#film-about-the-semiconductor-industry)
    - [Halt and Catch Fire (TV series)](#halt-and-catch-fire-tv-series)
  - [Semiconductor company](#semiconductor-company)
    - [Acorn Computers](#acorn-computers)
    - [AMD](#amd)
      - [AMD product](#amd-product)
        - [AMD CPU](#amd-cpu)
          - [Ryzen](#ryzen)
            - [Ryzen 7](#ryzen-7)
              - [Ryzen 7 microarchitecture](#ryzen-7-microarchitecture)
                - [Zen 4](#zen-4)
                  - [AMD 7840U](#amd-7840u)
          - [Epyc](#epyc)
        - [AMD GPU](#amd-gpu)
          - [AMD GPU driver](#amd-gpu-driver)
            - [AMDGPU](#amdgpu)
          - [RDNA](#rdna)
            - [RDNA 3](#rdna-3)
              - [gfx1103](#gfx1103)
          - [Radeon](#radeon)
          - [AMD Instinct](#amd-instinct)
          - [ATI Technologies](#ati-technologies)
      - [AMD employee](#amd-employee)
        - [Jerry Sanders](#jerry-sanders)
        - [Lisa Su](#lisa-su)
    - [Arm (company)](#arm-company)
      - [Allen Wu](#allen-wu)
      - [Arm product](#arm-product)
        - [Arm Artisan](#arm-artisan)
        - [ARM CPU](#arm-cpu)
          - [ARM Cortex-M](#arm-cortex-m)
            - [ARM Cortex-M0+](#arm-cortex-m0-plus)
    - [Broadcom](#broadcom)
    - [Cerebras](#cerebras)
    - [Graphcore](#graphcore)
    - [Intel](#intel)
      - [Intel employee](#intel-employee)
        - [Intel employee grade](#intel-employee-grade)
          - [Intel fellow](#intel-fellow)
      - [Intel hardware](#intel-hardware)
        - [Intel CPU](#intel-cpu)
          - [Intel i7-7820HQ](#intel-i7-7820hq)
        - [Intel GPU](#intel-gpu)
          - [Intel discrete GPU](#intel-discrete-gpu)
            - [Intel Xe](#intel-xe)
            - [Intel Arc](#intel-arc)
          - [Intel Graphics Technology](#intel-graphics-technology)
      - [Intel department](#intel-department)
        - [Intel Research](#intel-research)
    - [Nvidia](#nvidia)
      - [Software developed by Nvidia](#software-developed-by-nvidia)
        - [nvidia-smi](#nvidia-smi)
      - [Nvidia GPU](#nvidia-gpu)
        - [Nvidia GPU feature](#nvidia-gpu-feature)
          - [Nvidia tensor core](#nvidia-tensor-core)
        - [Nvidia compute GPU](#nvidia-compute-gpu)
          - [Nvidia Tesla](#nvidia-tesla)
          - [List of Nvidia compute GPUs](#list-of-nvidia-compute-gpus)
            - [Nvidia T4](#nvidia-t4)
            - [Nvidia A10](#nvidia-a10)
              - [Nvidia A10G](#nvidia-a10g)
    - [Qualcomm](#qualcomm)
    - [Silicon Graphics](#silicon-graphics)
  - [Chinese semiconductor industry](#chinese-semiconductor-industry)

<h2 id="moore-s-law">Moore's law</h2>

↑ **Parent:** [Computer hardware](computer-hardware.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Moore's_law)

Born: 1965

Died: 2010+-ish

## Semiconductor device fabrication

↑ **Parent:** [Computer hardware](computer-hardware.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Semiconductor_device_fabrication)

[https://en.wikipedia.org/wiki/Semiconductor_device](https://en.wikipedia.org/wiki/Semiconductor_device)

This is the lowest level of abstraction computer, at which the basic gates and power are described.

At this level, you are basically thinking about the 3D layered structure of a chip, and how to make machines that will allow you to create better, usually smaller, gates.

### Semiconductor research institute

↑ **Parent:** [Semiconductor device fabrication](#semiconductor-device-fabrication)  
🏷️ **Tags:** [Research institute](research-institute.md)

#### IMEC

↑ **Parent:** [Semiconductor research institute](#semiconductor-research-institute)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/IMEC)

<a id="video-imec-the-semiconductor-watering-hole-by-asianometry-2022"></a>
**[Video 1](#video-imec-the-semiconductor-watering-hole-by-asianometry-2022). imec: The Semiconductor Watering Hole by Asianometry (2022)** [Source](https://www.youtube.com/watch?v=RO7E7RX0L2Y). A key thing they do is have a small prototype fab that brings in-development equipment from different vendors together to make sure the are working well together. Cool.

#### Computer research institute

↑ **Parent:** [Semiconductor research institute](#semiconductor-research-institute)

##### Xerox PARC

↑ **Parent:** [Computer research institute](#computer-research-institute)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PARC_(company))

What a legendary place.

### Semiconductor equipment maker

↑ **Parent:** [Semiconductor device fabrication](#semiconductor-device-fabrication)

As mentioned at [https://youtu.be/16BzIG0lrEs?t=397](https://youtu.be/16BzIG0lrEs?t=397) from [Video 4. "Applied Materials by Asianometry (2021)"](#video-applied-materials-by-asianometry-2021), originally the companies [fabs](#semiconductor-fabrication-plant) would make their own equipment. But eventually things got so complicated that it became worth it for separate companies to focus on equipment, which then then sell to the fabs.

#### ASML Holding

↑ **Parent:** [Semiconductor equipment maker](#semiconductor-equipment-maker)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ASML_Holding)

As of 2020 leading makers of the most important [fab](#semiconductor-fabrication-plant) [photolithography](#photolithography) equipment.

<a id="video-asml-tsmc-s-critical-supplier-by-asianometry-2021"></a>
**[Video 2](#video-asml-tsmc-s-critical-supplier-by-asianometry-2021). ASML: TSMC's Critical Supplier by Asianometry (2021)** [Source](https://www.youtube.com/watch?v=CFsn1CUyXWs).

<a id="video-how-asml-won-lithography-by-asianometry-2021"></a>
**[Video 3](#video-how-asml-won-lithography-by-asianometry-2021). How ASML Won Lithography by Asianometry (2021)** [Source](https://www.youtube.com/watch?v=SB8qIO6Ti_M). First there were dominant Elmer and Geophysics Corporation of America dominating the market.

Then a Japanese government project managed to make Nikon and Canon Inc. catch up, and in 1989, when [Ciro Santilli](ciro-santilli.md) was born, they had 70% of the market.

[https://youtu.be/SB8qIO6Ti_M?t=240](https://youtu.be/SB8qIO6Ti_M?t=240) In 1995, ASML had reached 25% market share. Then it managed the folloging faster than the others:
- TwinScan, reached 50% market share in 2002
- Immersion litography
- EUV. There was a big split between EUV vs particle beams, and ASML bet on EUV and EUV won.
- [https://youtu.be/SB8qIO6Ti_M?t=459](https://youtu.be/SB8qIO6Ti_M?t=459) they have an insane number of [software engineers](software.md#software-engineer) working on software for the machine, which is insanely complex. They are big on [UML](computer.md#unified-modeling-language).
- [https://youtu.be/SB8qIO6Ti_M?t=634](https://youtu.be/SB8qIO6Ti_M?t=634) they use [ZEISS](photon.md#carl-zeiss-ag) optics, don't develop their own. More precisely, the majority owned subsidiary [Carl Zeiss SMT](photon.md#carl-zeiss-smt).
- [https://youtu.be/SB8qIO6Ti_M?t=703](https://youtu.be/SB8qIO6Ti_M?t=703) [IMEC](#imec) collaborations worked well. Notably the [ASML](#asml-holding)/[Philips](electronics.md#philips)/[ZEISS](photon.md#carl-zeiss-ag) trinity

---

- [https://www.youtube.com/watch?v=XLNsYecX_2Q](https://www.youtube.com/watch?v=XLNsYecX_2Q) ASML: Chip making goes vacuum with EUV (2009) Self promotional video, some good shots of their buildings.

##### ASM International

↑ **Parent:** [ASML Holding](#asml-holding)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ASM_International)

Parent/predecessor of [ASML](#asml-holding).

#### Applied Materials

↑ **Parent:** [Semiconductor equipment maker](#semiconductor-equipment-maker)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Applied_Materials)

<a id="video-applied-materials-by-asianometry-2021"></a>
**[Video 4](#video-applied-materials-by-asianometry-2021). Applied Materials by Asianometry (2021)** [Source](https://www.youtube.com/watch?v=16BzIG0lrEs). They are [chemical vapor deposition](#chemical-vapor-deposition) fanatics basically.

### Power, performance and area

↑ **Parent:** [Semiconductor device fabrication](#semiconductor-device-fabrication)

[https://en.wikichip.org/wiki/power-performance-area](https://en.wikichip.org/wiki/power-performance-area)

This is the mantra of the [semiconductor industry](#semiconductor-industry):
- power and area are the main limiting factors of chips, i.e., your budget:
  - chip area is ultra expensive because there are sporadic errors in the fabrication process, and each error in any part of the chip can potentially break the entire chip. Although there are 

    The percentage of working chips is called the yield.

    In some cases however, e.g. if the error only affects single CPU of a multi-core CPU, then they actually deactivate the broken CPU after testing, and sell the worse CPU cheaper with a clear branding of that: this is called binning [https://www.tomshardware.com/uk/reviews/glossary-binning-definition,5892.html](https://www.tomshardware.com/uk/reviews/glossary-binning-definition,5892.html)
  - power is a major semiconductor limit as of 2010's and onwards. If everything turns on at once, the chip would burn. Designs have to account for that.
- performance is the goal.

  Conceptually, this is basically a set of algorithms that you want your hardware to solve, each one with a respective weight of importance.

  Serial performance is fundamentally limited by the [longest path](computer-science.md#critical-path) that electrons have to travel in a given clock cycle.

  The way to work around it is to create pipelines, splitting up single operations into multiple smaller operations, and storing intermediate results in memories.

### Wafer (electronics)

↑ **Parent:** [Semiconductor device fabrication](#semiconductor-device-fabrication)

#### Czochralski method

↑ **Parent:** [Wafer (electronics)](#wafer-electronics)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Czochralski_method)

### Semiconductor fabrication plant

↑ **Parent:** [Semiconductor device fabrication](#semiconductor-device-fabrication)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Semiconductor_fabrication_plant)

They put a lot of expensive equipment together, much of it [made by other companies](#semiconductor-equipment-maker), and they make the entire chip for companies ordering them.

#### Company with a semiconductor fabrication plant

↑ **Parent:** [Semiconductor fabrication plant](#semiconductor-fabrication-plant)

A list of [fabs](#semiconductor-fabrication-plant) can be seen at: [https://en.wikipedia.org/wiki/List_of_semiconductor_fabrication_plants](https://en.wikipedia.org/wiki/List_of_semiconductor_fabrication_plants) and basically summarizes all the companies that have fabs.

##### Fairchild Semiconductor

↑ **Parent:** [Company with a semiconductor fabrication plant](#company-with-a-semiconductor-fabrication-plant)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fairchild_Semiconductor)

Some nice insights at: [Robert Noyce: The Man Behind the Microchip by Leslie Berlin (2006)](computer.md#robert-noyce-the-man-behind-the-microchip-by-leslie-berlin-2006).

##### GlobalFoundries

↑ **Parent:** [Company with a semiconductor fabrication plant](#company-with-a-semiconductor-fabrication-plant)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/GlobalFoundries)

[AMD](#amd) just gave up this risky part of the business amidst the [fabless](#fabless-manufacturing) boom. Sound like a wise move. They then fell more and more away from the state of the art, and moved into more niche areas.

##### Infineon Technologies

↑ **Parent:** [Company with a semiconductor fabrication plant](#company-with-a-semiconductor-fabrication-plant)  
🏷️ **Tags:** [Siemens spinoff](company.md#siemens-spinoff)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Infineon_Technologies)

##### SMIC

↑ **Parent:** [Company with a semiconductor fabrication plant](#company-with-a-semiconductor-fabrication-plant)  
🏷️ **Tags:** [Chinese semiconductor industry](#chinese-semiconductor-industry)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SMIC)

<a id="video-smic-explained-by-asianometry-2021"></a>
**[Video 5](#video-smic-explained-by-asianometry-2021). SMIC, Explained by Asianometry (2021)** [Source](https://www.youtube.com/watch?v=aL_kzMlqgt4).

##### TSMC

↑ **Parent:** [Company with a semiconductor fabrication plant](#company-with-a-semiconductor-fabrication-plant)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/TSMC)

One of the companies that has fabs, which buys machines from companies such as ASML and puts them together in so called "silicon fabs" to make the chips

As the quintessential [fabless](#fabless-manufacturing) [fab](#semiconductor-fabrication-plant), there is on thing TSMC can never ever do: sell their own design! It must forever remain a [fab](#semiconductor-fabrication-plant)-only company, that will never compete with its customers. This is highlighted e.g. at [https://youtu.be/TRZqE6H-dww?t=936](https://youtu.be/TRZqE6H-dww?t=936) from [Video 34. "How Nvidia Won Graphics Cards by Asianometry (2021)"](#video-how-nvidia-won-graphics-cards-by-asianometry-2021).

<a id="video-how-taiwan-created-tsmc-by-asianometry-2020"></a>
**[Video 6](#video-how-taiwan-created-tsmc-by-asianometry-2020). How Taiwan Created TSMC by Asianometry (2020)** [Source](https://www.youtube.com/watch?v=9fVrWDdll0g). Some points:
- UCM failed because it focused too much on the internal market, and was shielded from external competition, so it didn't become world leading
- one of TSMC's great advances was the [fabless](#fabless-manufacturing) business model approach.
- they managed to do large technology transfers from the West to kickstart things off
- one of their main victories was investing early in [CMOS](electronics.md#cmos), before it became huge, and winning that market

---

<a id="video-the-early-years-at-tsmc-by-asianometry"></a>
**[Video 7](#video-the-early-years-at-tsmc-by-asianometry). The Early Years at TSMC by Asianometry.** [Source](https://www.youtube.com/watch?v=Ml54fLhMXGg). 2023.

#### Semiconductor fabrication step

↑ **Parent:** [Semiconductor fabrication plant](#semiconductor-fabrication-plant)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Semiconductor_fabrication_step)

##### Chemical vapor deposition

↑ **Parent:** [Semiconductor fabrication step](#semiconductor-fabrication-step)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Chemical_vapor_deposition)

##### Photolithography

↑ **Parent:** [Semiconductor fabrication step](#semiconductor-fabrication-step)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Photolithography)

###### Extreme ultraviolet lithography

↑ **Parent:** [Photolithography](#photolithography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Extreme_ultraviolet_lithography)

###### Photomask

↑ **Parent:** [Photolithography](#photolithography)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Photomask)

### Standard cell library

↑ **Parent:** [Semiconductor device fabrication](#semiconductor-device-fabrication)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Standard_cell_library)

Basically what [register transfer level](#register-transfer-level) compiles to in order to achieve a real chip implementation.

After this is done, the final step is [place and route](#place-and-route).

They can be designed by third parties besides the [semiconductor fabrication plants](#semiconductor-fabrication-plant). E.g. [Arm Ltd.](#arm-company) markets its [Artisan](#arm-artisan) Standard Cell Libraries as mentioned e.g. at: [https://web.archive.org/web/20211007050341/https://developer.arm.com/ip-products/physical-ip/logic](https://web.archive.org/web/20211007050341/https://developer.arm.com/ip-products/physical-ip/logic) This came from a 2004 acquisition: [https://www.eetimes.com/arm-to-acquire-artisan-components-for-913-million/](https://www.eetimes.com/arm-to-acquire-artisan-components-for-913-million/), [obviously](social-technology.md#if-a-product-of-a-big-company-has-a-catchy-name-it-came-from-an-acquisition).

The standard cell library is typically composed of a bunch of versions of somewhat simple gates, e.g.:
- AND with 2 inputs
- AND with 3 inputs
- AND with 4 inputs
- OR with 2 inputs
- OR with 3 inputs
and so on.

Each of those gates has to be designed by hand as a [3D](calculus.md#real-coordinate-space-of-dimension-three) structure that can be produced in a given [fab](#semiconductor-fabrication-plant).

Simulations are then carried out, and the electric properties of those structures are characterized in a standard way as a bunch of tables of numbers that specify things like:
- how long it takes for electrons to pass through
- how much heat it produces
Those are then used in [power, performance and area](#power-performance-and-area) estimates.

#### Open source standard cell library

↑ **Parent:** [Standard cell library](#standard-cell-library)

Open source ones:
- [https://www.quora.com/Are-there-good-open-source-standard-cell-libraries-to-learn-IC-synthesis-with-EDA-tools/answer/Ciro-Santilli](https://www.quora.com/Are-there-good-open-source-standard-cell-libraries-to-learn-IC-synthesis-with-EDA-tools/answer/Ciro-Santilli) Are there good open source standard cell libraries to learn IC synthesis with EDA tools?

### Electronic design automation

↑ **Parent:** [Semiconductor device fabrication](#semiconductor-device-fabrication)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Electronic_design_automation)

A set of software programs that [compile](software.md#compiler) high level [register transfer level](#register-transfer-level) languages such as [Verilog](#verilog) into something that a [fab](#semiconductor-fabrication-plant) can actually produce. One is reminded of a [compiler toolchain](software.md#compiler-toolchain) but on a lower level.

The most important steps of that include:
- [logic synthesis](#logic-synthesis): mapping the [Verilog](#verilog) to a [standard cell library](#standard-cell-library)
- [place and route](#place-and-route): mapping the synthesis output into the 2D surface of the chip

#### Electronic design automation phase

↑ **Parent:** [Electronic design automation](#electronic-design-automation)

##### Logic synthesis

↑ **Parent:** [Electronic design automation phase](#electronic-design-automation-phase)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Logic_synthesis)

Step of [electronic design automation](#electronic-design-automation) that maps the [register transfer level](#register-transfer-level) input (e.g. [Verilog](#verilog)) to a [standard cell library](#standard-cell-library).

The output of this step is another [Verilog](#verilog) file, but one that exclusively uses interlinked cell library components.

##### Place and route

↑ **Parent:** [Electronic design automation phase](#electronic-design-automation-phase)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Place_and_route)

Given a bunch of interlinked [standard cell library](#standard-cell-library) elements from the [logic synthesis](#logic-synthesis) step, actually decide where exactly they are going to go on 2D (stacked 2D) [integrated circuit](#integrated-circuit) surface.

Sample output format of place and route would be [GDSII](#gdsii).

###### Integrated circuit layout

↑ **Parent:** [Place and route](#place-and-route)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Integrated_circuit_layout)

###### GDSII

↑ **Parent:** [Integrated circuit layout](#integrated-circuit-layout)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/GDSII)

<a id="image-3d-rendering-of-a-gdsii-file"></a>
![](https://upload.wikimedia.org/wikipedia/commons/a/aa/Silicon_chip_3d.png)

**[Figure 1](#image-3d-rendering-of-a-gdsii-file). 3D rendering of a GDSII file.** [Source](https://commons.wikimedia.org/wiki/File:Silicon_chip_3d.png).

#### EDA company

↑ **Parent:** [Electronic design automation](#electronic-design-automation)  
🏷️ **Tags:** [Technology company](company.md#technology-company)

The main ones as of 2020 are:
- [Mentor Graphics](#mentor-graphics), which was bought by [Siemens](company.md#siemens) in 2017
- [Cadence Design Systems](#cadence-design-systems)
- [Synopsys](#synopsys)

##### Cadence Design Systems

↑ **Parent:** [EDA company](#eda-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cadence_Design_Systems)

###### Alberto Sangiovanni-Vincentelli

↑ **Parent:** [Cadence Design Systems](#cadence-design-systems)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Alberto_Sangiovanni-Vincentelli)

<a id="video-the-italian-professor-who-founded-2-billion-dollar-companies-by-marcello-ascani"></a>
**[Video 8](#video-the-italian-professor-who-founded-2-billion-dollar-companies-by-marcello-ascani). The Italian PROFESSOR who founded 2 BILLION-DOLLAR Companies by Marcello Ascani.** [Source](https://www.youtube.com/watch?v=fMwJHIL5ms0).

##### Mentor Graphics

↑ **Parent:** [EDA company](#eda-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mentor_Graphics)

##### Synopsys

↑ **Parent:** [EDA company](#eda-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Synopsys)

#### Open source EDA tool

↑ **Parent:** [Electronic design automation](#electronic-design-automation)

##### qflow

↑ **Parent:** [Open source EDA tool](#open-source-eda-tool)

Cool looking [open source EDA toolchain](#open-source-eda-tool):
- [http://opencircuitdesign.com/qflow/](http://opencircuitdesign.com/qflow/)
- [https://github.com/RTimothyEdwards/qflow](https://github.com/RTimothyEdwards/qflow)

They apparently even produced a real working small [RISC-V](#risc-v) chip with the flow, not bad.

### Semiconductor process node

↑ **Parent:** [Semiconductor device fabrication](#semiconductor-device-fabrication)

### Semiconductor device fabrication bibliography

↑ **Parent:** [Semiconductor device fabrication](#semiconductor-device-fabrication)

#### Asianometry

↑ **Parent:** [Semiconductor device fabrication bibliography](#semiconductor-device-fabrication-bibliography)  
🏷️ **Tags:** [The best technology YouTube channels](technology.md#the-best-technology-youtube-channels)

[https://www.youtube.com/channel/UC1LpsuAUaKoMzzJSEt5WImw](https://www.youtube.com/channel/UC1LpsuAUaKoMzzJSEt5WImw)

Very good channel to learn some basics of [semiconductor device fabrication](#semiconductor-device-fabrication)!

Focuses mostly on the [semiconductor industry](#semiconductor-industry).

[https://youtu.be/aL_kzMlqgt4?t=661](https://youtu.be/aL_kzMlqgt4?t=661) from [Video 5. "SMIC, Explained by Asianometry (2021)"](#video-smic-explained-by-asianometry-2021) from mentions he is of Chinese ascent, ancestors from Ningbo. Earlier in the same video he mentions he worked on some startups. He doesn't appear to speak perfect Mandarin Chinese anymore though based on pronounciation of Chinese names.

[https://asianometry.substack.com/](https://asianometry.substack.com/) gives an abbreviated name "Jon Y".

<a id="video-reflecting-on-asianometry-in-2022-by-asianometry-2022"></a>
**[Video 9](#video-reflecting-on-asianometry-in-2022-by-asianometry-2022). Reflecting on Asianometry in 2022 by Asianometry (2022)** [Source](https://www.youtube.com/watch?v=X9Zm3K05Utk). Mentions his insane work schedule: 4 hours research in the morning, then day job, then editing and uploading until midnight. Appears to be based in [Taipei](continent.md#taipei). Two videos a week. So even at the current 400k subs, he still can't make a living.

## Integrated circuit

↑ **Parent:** [Computer hardware](computer-hardware.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Integrated_circuit)

It is quite amazing to read through books such as [The Supermen: The Story of Seymour Cray by Charles J. Murray (1997)](computer.md#the-supermen-the-story-of-seymour-cray-by-charles-j-murray-1997), as it makes you notice that earlier [CPUs](#central-processing-unit) (all before the 70's) were not made with [integrated circuits](#integrated-circuit), but rather smaller pieces glued up on [PCBs](electronics.md#printed-circuit-board)! E.g. the [arithmetic logic unit](#arithmetic-logic-unit) was actually a discrete component at one point.

The reason for this can also be understood quite clearly by reading books such as [Robert Noyce: The Man Behind the Microchip by Leslie Berlin (2006)](computer.md#robert-noyce-the-man-behind-the-microchip-by-leslie-berlin-2006). The first [integrated circuits](#integrated-circuit) were just too small for this. It was initially unimaginable that a CPU would fit in a single chip! Even just having a very small number of components on a chip was already revolutionary and enough to kick-start the industry. Just imagine how much money any level of integration saved in those early days for production, e.g. as opposed to manually soldering [point-to-point constructions](electronics.md#point-to-point-construction). Also the reliability, size an weight gains were amazing. In particular for military and spacial applications originally.

<a id="video-a-briefing-on-semiconductors-by-fairchild-semiconductor-1967"></a>
**[Video 10](#video-a-briefing-on-semiconductors-by-fairchild-semiconductor-1967). A briefing on semiconductors by Fairchild Semiconductor (1967)** [Source](https://www.youtube.com/watch?v=z47Gv2cdFtA). Uploaded by the [Computer History Museum](science.md#computer-history-museum). [There is value in tutorials written by early pioneers of the field](physics.md#there-is-value-in-tutorials-written-by-early-pioneers-of-the-field), this is pure [gold](chemistry.md#gold).

Shows:
- [photomasks](#photomask)
- [silicon](chemistry.md#silicon) [ingots](condensed-matter-physics.md#ingot) and [wafer](#wafer-electronics) processing

---

<h3 id="interconnect-integrated-circuits">Interconnect (integrated_circuits)</h3>

↑ **Parent:** [Integrated circuit](#integrated-circuit)

### Application-specific integrated circuit

↑ **Parent:** [Integrated circuit](#integrated-circuit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Application-specific_integrated_circuit)

### System on a chip

↑ **Parent:** [Integrated circuit](#integrated-circuit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/System_on_a_chip)

## Register transfer level

↑ **Parent:** [Computer hardware](computer-hardware.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Register_transfer_level)

Register transfer level is the abstraction level at which computer chips are mostly designed.

The only two truly relevant RTL languages as of 2020 are: [Verilog](#verilog) and [VHDL](#vhdl). Everything else compiles to those, because that's all that [EDA vendors](#eda-company) support.

Much like a [C](programming-language.md#c-programming-language) compiler abstracts away the [CPU](#central-processing-unit) assembly to:
- increase portability across ISAs
- do optimizations that programmers can't feasibly do without going crazy

Compilers for RTL languages such as Verilog and [VHDL](#vhdl) abstract away the details of the specific [semiconductor technology](#semiconductor-device-fabrication) used for those exact same reasons.

The compilers essentially compile the RTL languages into a [standard cell library](#standard-cell-library).

Examples of companies that work at this level include:
- [Intel](#intel). Intel also has [semiconductor fabrication plants](#semiconductor-fabrication-plant) however.
- [Arm](#arm-company) which does not have [fabs](#semiconductor-fabrication-plant), and is therefore called a "[fabless](#fabless-manufacturing)" company.

### High-level synthesis

↑ **Parent:** [Register transfer level](#register-transfer-level)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/High-level_synthesis)

### Fabless manufacturing

↑ **Parent:** [Register transfer level](#register-transfer-level)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fabless_manufacturing)

In the past, most computer designers would have their own [fabs](#semiconductor-fabrication-plant).

But once designs started getting very complicated, it started to make sense to separate concerns between designers and [fabs](#semiconductor-fabrication-plant).

What this means is that design companies would primarily write [register transfer level](#register-transfer-level), then use [electronic design automation](#electronic-design-automation) tools to get a final manufacturable chip, and then send that to the [fab](#semiconductor-fabrication-plant).

It is in this point of time that [TSMC](#tsmc) came along, and benefied and helped establish this trend.

The term "Fabless" could in theory refer to other areas of industry besides the [semiconductor industry](#semiconductor-industry), but it is mostly used in that context.

#### Fabless semiconductor company

↑ **Parent:** [Fabless manufacturing](#fabless-manufacturing)

### Logic gate

↑ **Parent:** [Register transfer level](#register-transfer-level)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Logic_gate)

#### Truth table

↑ **Parent:** [Logic gate](#logic-gate)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Truth_table)

### Verilog

↑ **Parent:** [Register transfer level](#register-transfer-level)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Verilog)

Examples under [verilog](verilog), more details at [Verilator](#verilator).

#### Value change dump

↑ **Parent:** [Verilog](#verilog)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Value_change_dump)

#### Verilator

↑ **Parent:** [Verilog](#verilog)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Verilator)

[Verilog](#verilog) simulator that [transpiles](software.md#source-to-source-compiler) to [C++](programming-language.md#c-plus-plus).

One very good thing about this is that it makes it easy to create test cases directly in C++. You just supply inputs and clock the simulation directly in a C++ loop, then read outputs and assert them with `assert()`. And you can inspect variables by printing them or with GDB. This is infinitely more convenient than doing these IO-type tasks in [Verilog](#verilog) itself.

Some simulation examples under [verilog](verilog).

First install [Verilator](#verilator). On [Ubuntu](systems-programming.md#ubuntu):
```
sudo apt install verilator
```
Tested on Verilator 4.038, [Ubuntu 22.04](systems-programming.md#ubuntu-22-04).

Run all examples, which have assertions in them:
```
cd verilator
make run
```

File structure is for example:
- [verilog/counter.v](verilog/counter.v): [Verilog](#verilog) file
- [verilog/counter.cpp](verilog/counter.cpp): [C++](programming-language.md#c-plus-plus) loop which clocks the design and runs tests with assertions on the outputs
- [verilog/counter.params](verilog/counter.params): [gcc](software.md#gnu-compiler-collection) compilation flags for this example
- [verilog/counter_tb.v](verilog/counter_tb.v): [Verilog](#verilog) version of the [C++](programming-language.md#c-plus-plus) test. Not used by Verilator. Verilator can't actually run out `_tb` files, because they do in Verilog IO things that we do better from [C++](programming-language.md#c-plus-plus) in Verilator, so Verilator didn't bother implementing them. This is a good thing.

Example list:
- [verilog/negator.v](verilog/negator.v), [verilog/negator.cpp](verilog/negator.cpp): the simplest non-identity combinatorial circuit!
- [verilog/counter.v](verilog/counter.v), [verilog/counter.cpp](verilog/counter.cpp): sequential hello world. Synchronous active high reset with active high enable signal. Adapted from: [http://www.asic-world.com/verilog/first1.html](http://www.asic-world.com/verilog/first1.html)
- [verilog/subleq.v](verilog/subleq.v), [verilog/subleq.cpp](verilog/subleq.cpp): subleq [one instruction set computer](#one-instruction-set-computer) with separated instruction and data RAMs

##### Verilator interactive example

↑ **Parent:** [Verilator](#verilator)

The example under [verilog/interactive](verilog/interactive) showcases how to create a simple interactive visual [Verilog](#verilog) example using [Verilator](#verilator) and [SDL](video-game.md#simple-directmedia-layer).

![](https://raw.githubusercontent.com/cirosantilli/media/master/verilog-interactive.gif)

You could e.g. expand such an example to create a simple (or complex) [video game](video-game.md) for example if you were insane enough. But please don't waste your time doing that, [Ciro Santilli begs you](cirism.md#backward-design).

The example is also described at: [https://stackoverflow.com/questions/38108243/is-it-possible-to-do-interactive-user-input-and-output-simulation-in-vhdl-or-ver/38174654#38174654](https://stackoverflow.com/questions/38108243/is-it-possible-to-do-interactive-user-input-and-output-simulation-in-vhdl-or-ver/38174654#38174654)

Usage: install dependencies:
```
sudo apt install libsdl2-dev verilator
```
then run as either:
```
make run RUN=and2
make run RUN=move
```
Tested on Verilator 4.038, Ubuntu 22.04.

File overview:
- and2
  - [verilog/interactive/and2.cpp](verilog/interactive/and2.cpp)
  - [verilog/interactive/and2.v](verilog/interactive/and2.v)
- move
  - [verilog/interactive/move.cpp](verilog/interactive/move.cpp)
  - [verilog/interactive/move.v](verilog/interactive/move.v)
- [verilog/interactive/display.cpp](verilog/interactive/display.cpp)

In those examples, the more interesting application specific logic is delegated to Verilog (e.g.: move game character on map), while boring timing and display matters can be handled by SDL and C++.

### VHDL

↑ **Parent:** [Register transfer level](#register-transfer-level)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/VHDL)

Examples under [vhdl](vhdl), more details at: [GHDL](#ghdl).

#### GHDL

↑ **Parent:** [VHDL](#vhdl)

[https://github.com/ghdl/ghdl](https://github.com/ghdl/ghdl)

Examples under [vhdl](vhdl).

First install [GHDL](#ghdl). On [Ubuntu](systems-programming.md#ubuntu):
```
sudo apt install verilator
```
Tested on Verilator 1.0.0, [Ubuntu 22.04](systems-programming.md#ubuntu-22-04).

Run all examples, which have assertions in them:
```
cd vhdl
./run
```

Files:
- Examples
  - Basic
    - [vhdl/hello_world_tb.vhdl](vhdl/hello_world_tb.vhdl): hello world
    - [vhdl/min_tb.vhdl](vhdl/min_tb.vhdl): min
    - [vhdl/assert_tb.vhdl](vhdl/assert_tb.vhdl): assert
  - Lexer
    - [vhdl/comments_tb.vhdl](vhdl/comments_tb.vhdl): comments
    - [vhdl/case_insensitive_tb.vhdl](vhdl/case_insensitive_tb.vhdl): case insensitive
    - [vhdl/whitespace_tb.vhdl](vhdl/whitespace_tb.vhdl): whitespace
    - [vhdl/literals_tb.vhdl](vhdl/literals_tb.vhdl): literals
  - Flow control
    - [vhdl/procedure_tb.vhdl](vhdl/procedure_tb.vhdl): procedure
    - [vhdl/function_tb.vhdl](vhdl/function_tb.vhdl): function
  - [vhdl/operators_tb.vhdl](vhdl/operators_tb.vhdl): operators
  - Types
    - [vhdl/integer_types_tb.vhdl](vhdl/integer_types_tb.vhdl): integer types
    - [vhdl/array_tb.vhdl](vhdl/array_tb.vhdl): array
    - [vhdl/record_tb.vhdl.bak](vhdl/record_tb.vhdl.bak): record. TODO fails with "GHDL Bug occurred" on GHDL 1.0.0
    - [vhdl/generic_tb.vhdl](vhdl/generic_tb.vhdl): generic
  - [vhdl/package_test_tb.vhdl](vhdl/package_test_tb.vhdl): Packages
    - [vhdl/standard_package_tb.vhdl](vhdl/standard_package_tb.vhdl): standard package
    - textio  
        \* [vhdl/write_tb.vhdl](vhdl/write_tb.vhdl): write  
        \* [vhdl/read_tb.vhdl](vhdl/read_tb.vhdl): read
    - [vhdl/std_logic_tb.vhdl](vhdl/std_logic_tb.vhdl): std\_logic
  - [vhdl/stop_delta_tb.vhdl](vhdl/stop_delta_tb.vhdl): `--stop-delta`
- Applications
  - Combinatoric
    - [vhdl/adder.vhdl](vhdl/adder.vhdl): adder
    - [vhdl/sqrt8_tb.vhdl](vhdl/sqrt8_tb.vhdl): sqrt8
  - Sequential
    - [vhdl/clock_tb.vhdl](vhdl/clock_tb.vhdl): clock
    - [vhdl/counter.vhdl](vhdl/counter.vhdl): counter
- Helpers  
    \* [vhdl/template_tb.vhdl](vhdl/template_tb.vhdl): template

## Microarchitecture

↑ **Parent:** [Computer hardware](computer-hardware.md)  
🏷️ **Tags:** [Computer architecture](computer.md#computer-architecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Microarchitecture)

### [Microarchitectural](#microarchitecture) [benchmark](software.md#benchmark)

↑ **Parent:** [Microarchitecture](#microarchitecture)

#### CPU microbenchmark

↑ **Parent:** [Microarchitectural benchmark](#microarchitectural-benchmark)

Some examples:

<h5 id="_file/c/inc_loop.c">c/inc_loop.c</h5>

↑ **Parent:** [CPU microbenchmark](#cpu-microbenchmark)

[Ubuntu 25.04](systems-programming.md#ubuntu-25-04) GCC 14.2 -O0 x86\_64 produces a horrendous:
```
11c8:       48 83 45 f0 01          addq   $0x1,-0x10(%rbp)
11cd:       48 8b 45 f0             mov    -0x10(%rbp),%rax
11d1:       48 3b 45 e8             cmp    -0x18(%rbp),%rax
11d5:       72 f1                   jb     11c8 <main+0x7f>
```
To do about 1s on [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd) we need 2.5 billion instructions:
```
time ./inc_loop.out 2500000000
```
and:
```
time ./inc_loop.out 2500000000
```
gives:
```
          1,052.22 msec task-clock                       #    0.998 CPUs utilized             
                23      context-switches                 #   21.858 /sec                      
                12      cpu-migrations                   #   11.404 /sec                      
                60      page-faults                      #   57.022 /sec                      
    10,015,198,766      instructions                     #    2.08  insn per cycle            
                                                  #    0.00  stalled cycles per insn   
     4,803,504,602      cycles                           #    4.565 GHz                       
        20,705,659      stalled-cycles-frontend          #    0.43% frontend cycles idle      
     2,503,079,267      branches                         #    2.379 G/sec                     
           396,228      branch-misses                    #    0.02% of all branches
```

With -O3 it manages to fully unroll the loop removing it entirely and producing:
```
    1078:       e8 d3 ff ff ff          call   1050 <strtoll@plt>
}
    107d:       5a                      pop    %rdx
    107e:       c3                      ret
```
to is it smart enough to just return the return value from strtoll directly as is in `rax`.

<h5 id="_file/c/inc_loop_asm.c">c/inc_loop_asm.c</h5>

↑ **Parent:** [CPU microbenchmark](#cpu-microbenchmark)

This is the only way that we've managed to reliably get a single `inc` instruction loop, by using [inline assembly](programming-language.md#inline-assembly), e.g. on we do [x86](#x86):
```
loop:
  inc %[i];
  cmp %[max], %[i];
  jb loop;
```

For 1s on [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd) [Ubuntu 25.04](systems-programming.md#ubuntu-25-04) GCC 14.2 -O0 x86\_64 we need about 5 billion:
```
time ./inc_loop_asm.out 5000000000
```

<h5 id="_file/c/inc_loop_asm_n.sh">c/inc_loop_asm_n.sh</h5>

↑ **Parent:** [CPU microbenchmark](#cpu-microbenchmark)

This is a quick [Microarchitectural benchmark](#microarchitectural-benchmark) to try and determine how many [functional units](#cpu-functional-unit) our CPU has that can do an `inc` instruction at the same time due to [superscalar architecture](#superscalar-processor).

The generated programs do loops like:
```
loop:
  inc %[i0];
  inc %[i1];
  inc %[i2];
  ...
  inc %[i_n];
  cmp %[max], %[i0];
  jb loop;
```
with different numbers of inc instructions.

<a id="image-c-inc-loop-asm-n-sh-results-for-a-few-cpus"></a>
<img src="https://raw.githubusercontent.com/cirosantilli/media/refs/heads/master/c/inc_loop_asm_n_manual.png" alt="" height="480">

**[Figure 2](#image-c-inc-loop-asm-n-sh-results-for-a-few-cpus). c/inc_loop_asm_n.sh results for a few CPUs**. Quite clearly:
- [AMD 7840U](#amd-7840u) can run INC on 4 functional units
- [Intel i7-7820HQ](#intel-i7-7820hq) can run INC on 2 functional units
and both have low instruction count effects that destroy performance, AMD at 3 and Intel at 3 and 5. TODO it would be cool to understand those better.

Data from multiple CPUs manually collated and plotted manually with [c/inc_loop_asm_n_manual.sh](c/inc_loop_asm_n_manual.sh).

---

Announced at:
- [https://mastodon.social/@cirosantilli/114698665154298332](https://mastodon.social/@cirosantilli/114698665154298332)
- [https://x.com/cirosantilli/status/1934950348663214211](https://x.com/cirosantilli/status/1934950348663214211)
- [https://www.linkedin.com/feed/update/urn:li:ugcPost:7340716961170898944/](https://www.linkedin.com/feed/update/urn:li:ugcPost:7340716961170898944/)

<h5 id="_file/c/mul_loop_asm.c">c/mul_loop_asm.c</h5>

↑ **Parent:** [CPU microbenchmark](#cpu-microbenchmark)

- [https://superuser.com/questions/643442/latency-of-cpu-instructions-on-x86-and-x64-processors](https://superuser.com/questions/643442/latency-of-cpu-instructions-on-x86-and-x64-processors)
- [https://stackoverflow.com/questions/692718/how-many-cpu-cycles-are-needed-for-each-assembly-instruction](https://stackoverflow.com/questions/692718/how-many-cpu-cycles-are-needed-for-each-assembly-instruction)

<h5 id="_file/c/mul_loop_asm_2.c">c/mul_loop_asm_2.c</h5>

↑ **Parent:** [CPU microbenchmark](#cpu-microbenchmark)

<h5 id="_file/c/mul_loop_asm_n.sh">c/mul_loop_asm_n.sh</h5>

↑ **Parent:** [CPU microbenchmark](#cpu-microbenchmark)

## Computer hardware component type

↑ **Parent:** [Computer hardware](computer-hardware.md)

### Processor (computing)

↑ **Parent:** [Computer hardware component type](#computer-hardware-component-type)

#### Instruction set architecture

↑ **Parent:** [Processor (computing)](#processor-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Instruction_set_architecture)

The main interface between the [central processing unit](#central-processing-unit) and [software](software.md).

##### Assembly language

↑ **Parent:** [Instruction set architecture](#instruction-set-architecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Assembly_language)

A human readable way to write instructions for an [instruction set architecture](#instruction-set-architecture).

One of the topics covered in [Ciro Santilli](ciro-santilli.md)'s [Linux Kernel Module Cheat](the-most-important-projects-done-by-ciro-santilli.md#linux-kernel-module-cheat).

###### Assembler (computing)

↑ **Parent:** [Assembly language](#assembly-language)

###### GNU Assembler

↑ **Parent:** [Assembler (computing)](#assembler-computing)  
🏷️ **Tags:** [gcc](software.md#gnu-compiler-collection)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/GNU_Assembler)

##### Calling convention

↑ **Parent:** [Instruction set architecture](#instruction-set-architecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Calling_convention)

##### List of instruction set architectures

↑ **Parent:** [Instruction set architecture](#instruction-set-architecture)

List of [instruction set architecture](#instruction-set-architecture).

###### One instruction set computer

↑ **Parent:** [List of instruction set architectures](#list-of-instruction-set-architectures)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/One_instruction_set_computer)

[https://stackoverflow.com/questions/3711443/minimal-instruction-set-to-solve-any-problem-with-a-computer-program/38523869#38523869](https://stackoverflow.com/questions/3711443/minimal-instruction-set-to-solve-any-problem-with-a-computer-program/38523869#38523869)

###### ARM architecture family

↑ **Parent:** [List of instruction set architectures](#list-of-instruction-set-architectures)  
🏷️ **Tags:** [Arm (company)](#arm-company)

This [ISA](#instruction-set-architecture) basically completely dominated the [smartphone](#smartphone) market of the 2010s and beyond, but it started appearing in other areas as the end of [Moore's law](#moore-s-law) made it more economical logical for large companies to start developing their own semiconductor, e.g. [Google custom silicon](google.md#google-custom-silicon), [Amazon custom silicon](amazon.md#amazon-custom-silicon).

It is exciting to see ARM entering the [server](computer.md#server-computing), [desktop](#desktop-computer) and [supercomputer](#supercomputer) market circa 2020, beyond its dominant mobile position and roots.

[Ciro Santilli](ciro-santilli.md) likes [to see the underdogs rise](ciro-santilli-s-psychology-and-physiology.md#ciro-santilli-s-self-perceived-creative-personality), and bite off dominant ones.

The excitement also applies to [RISC-V](#risc-v) possibly over ARM mobile market one day conversely however.

Basically, as long as were a huge company seeking to develop a [CPU](#central-processing-unit) and able to control your own ecosystem independently of [Windows](microsoft.md#microsoft-windows)' desktop domination (held by the need for backward compatibility with a billion end user programs), ARM would be a possibility on your mind.

- in 2020, the Fugaku supercomputer, which uses an ARM-based [Fujitsu](computer.md#fujitsu) designed chip, because the number 1 fastest supercomputer in [TOP500](#top500): [https://www.top500.org/lists/top500/2021/11/](https://www.top500.org/lists/top500/2021/11/)

  It was later beaten by another [x86](#x86) supercomputer [https://www.top500.org/lists/top500/2022/06/](https://www.top500.org/lists/top500/2022/06/), but the message was clearly heard.
- 2012 [https://hackaday.com/2012/07/09/pedal-powered-32-core-arm-linux-server/](https://hackaday.com/2012/07/09/pedal-powered-32-core-arm-linux-server/) pedal-powered 32-core Arm Linux server. A [publicity stunt](social-technology.md#publicity-stunt), but still, cool.
- [AWS Graviton](amazon.md#aws-graviton)

###### PowerPC

↑ **Parent:** [List of instruction set architectures](#list-of-instruction-set-architectures)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PowerPC)

###### RISC-V

↑ **Parent:** [List of instruction set architectures](#list-of-instruction-set-architectures)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/RISC-V)

The leading no-royalties options as of 2020.

[China](china.md) has been a major [RISC-V](#risc-v) potential user in the late 2010s, since the country is trying to increase its [semiconductor industry](#semiconductor-industry) independence, especially given economic sanctions imposed by the [USA](united-states.md).

E.g. a result of this, the [RISC-V Foundation](#risc-v-international) moved its legal headquarters to [Switzerland](continent.md#switzerland) in 2019 to try and overcome some of the sanctions.

###### RISC-V International

↑ **Parent:** [RISC-V](#risc-v)

###### RISC-V vendor

↑ **Parent:** [RISC-V](#risc-v)

###### Codasip

↑ **Parent:** [RISC-V vendor](#risc-v-vendor)  
🏷️ **Tags:** [German company](company.md#german-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Codasip)

###### SiFive

↑ **Parent:** [RISC-V vendor](#risc-v-vendor)  
🏷️ **Tags:** [American company](company.md#american-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SiFive)

Leading [RISC-V](#risc-v) consultants as of 2020, they are basically trying to become the [Red Hat](software.md#red-hat) of the [semiconductor industry](#semiconductor-industry).

###### SiPearl

↑ **Parent:** [RISC-V vendor](#risc-v-vendor)  
🏷️ **Tags:** [French company](company.md#french-company)

Risky name with the Si prefix, too close to [SiFive](#sifive). Both a reference to [silicon](chemistry.md#silicon) no doubt, but still. If they stick they will one day rename.

###### RISC-V timer

↑ **Parent:** [RISC-V](#risc-v)  
🏷️ **Tags:** [QEMU](systems-programming.md#qemu)

<h6 id="_file/riscv/timer.S">riscv/timer.S</h6>

↑ **Parent:** [RISC-V timer](#risc-v-timer)

TODO: the interrupt is firing only once:
- [https://www.reddit.com/r/RISCV/comments/ov4vhh/timer_interrupt/](https://www.reddit.com/r/RISCV/comments/ov4vhh/timer_interrupt/)

Adapted from: [https://danielmangum.com/posts/risc-v-bytes-timer-interrupts/](https://danielmangum.com/posts/risc-v-bytes-timer-interrupts/)

Tested on [Ubuntu 23.10](systems-programming.md#ubuntu-23-10):
```
sudo apt install binutils-riscv64-unknown-elf qemu-system-misc gdb-multiarch
cd riscv
make
```
Then on shell 1:
```
qemu-system-riscv64 -machine virt -cpu rv64 -smp 1 -s -S -nographic -bios none -kernel timer.elf
```
and on shell 2:
```
gdb-multiarch timer.elf -nh -ex "target remote :1234" -ex 'display /i $pc' -ex 'break *mtrap' -ex 'display *0x2004000' -ex 'display *0x200BFF8'
```
[GDB](software.md#gnu-debugger) should break infinitel many times on `mtrap` as interrupts happen.

###### RISC-V priviledged ISA

↑ **Parent:** [RISC-V](#risc-v)

###### RISC-V MSTATUS register

↑ **Parent:** [RISC-V priviledged ISA](#risc-v-priviledged-isa)

<h6 id="risc-v-mstatus-mie-field">RISC-V MSTATUS.MIE field</h6>

↑ **Parent:** [RISC-V MSTATUS register](#risc-v-mstatus-register)

###### x86

↑ **Parent:** [List of instruction set architectures](#list-of-instruction-set-architectures)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/x86)

<h6 id="x86-paging">x86 Paging Tutorial</h6>

↑ **Parent:** [x86](#x86)

[This section is present in another page, follow this link to view it.](x86-paging.md)

###### x86 custom instructions

↑ **Parent:** [x86](#x86)

[Intel](#intel) is known to have created customized chips for very large clients.

This is mentioned e.g. at: [https://www.theregister.com/2021/03/23/google_to_build_server_socs/](https://www.theregister.com/2021/03/23/google_to_build_server_socs/)

> Intel is known to do custom-ish cuts of Xeons for big customers.

Those chips are then used only in large scale server deployments of those very large clients. [Google](google.md) is one of them most likely, given their penchant for [Google custom hardware](google.md#google-custom-hardware).

TODO better sources.

###### Y86

↑ **Parent:** [List of instruction set architectures](#list-of-instruction-set-architectures)

[https://esolangs.org/wiki/Y86](https://esolangs.org/wiki/Y86) mentions:

> Y86 is a toy RISC CPU instruction set for education purpose.

One specification at: [http://web.cse.ohio-state.edu/~reeves.92/CSE2421sp13/PracticeProblemsY86.pdf](http://web.cse.ohio-state.edu/~reeves.92/CSE2421sp13/PracticeProblemsY86.pdf)

#### Type of processor

↑ **Parent:** [Processor (computing)](#processor-computing)

##### Central processing unit

↑ **Parent:** [Type of processor](#type-of-processor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Central_processing_unit)

###### Arithmetic logic unit

↑ **Parent:** [Central processing unit](#central-processing-unit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Arithmetic_logic_unit)

###### Microcontroller

↑ **Parent:** [Central processing unit](#central-processing-unit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Microcontroller)

As of 2020's, it is basically a cheap/slow/simple CPU used in [embedded system](#embedded-system) applications.

###### Microcontroller [emulation](systems-programming.md#emulator)

↑ **Parent:** [Microcontroller](#microcontroller)  
🏷️ **Tags:** [Emulation](systems-programming.md#emulator)

###### Microcontroller plus circuit emulation

↑ **Parent:** [Microcontroller emulation](#microcontroller-emulation)

There were still no amazing [open source](software.md#open-source-software) implementations as of 2025.

This section is about emulation setups that simulate both the microcontroller as well as the electronics it controls.

Bibliography:
- [https://www.reddit.com/r/embedded/comments/smi37p/emulators_for_microcontrollers/](https://www.reddit.com/r/embedded/comments/smi37p/emulators_for_microcontrollers/)
- [https://www.reddit.com/r/embedded/comments/1fb2yph/tools_for_simulating_microcontroller_boards/](https://www.reddit.com/r/embedded/comments/1fb2yph/tools_for_simulating_microcontroller_boards/)

People seeking [QEMU](systems-programming.md#qemu)-based solutions:
- [https://stackoverflow.com/questions/60764018/how-to-connect-gpio-in-qemu-emulated-machine-to-an-object-in-host](https://stackoverflow.com/questions/60764018/how-to-connect-gpio-in-qemu-emulated-machine-to-an-object-in-host)
- [https://raspberrypi.stackexchange.com/questions/56373/is-it-possible-to-get-the-state-of-the-leds-and-gpios-in-a-qemu-emulation-like-t](https://raspberrypi.stackexchange.com/questions/56373/is-it-possible-to-get-the-state-of-the-leds-and-gpios-in-a-qemu-emulation-like-t)

###### Proteus Design Suite

↑ **Parent:** [Microcontroller plus circuit emulation](#microcontroller-plus-circuit-emulation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Proteus_Design_Suite)

<img src="https://web.archive.org/web/20250731153059im_/https://miro.medium.com/v2/resize:fit:720/format:webp/0*MyhQ0US6SxmftMHr.PNG" alt="" height="600">

**[Figure 3](#_318)** [Source](https://satyamkr80.medium.com/stm32-bluepill-library-simulation-in-proteus-4c9820d64b7b).

###### Wokwi

↑ **Parent:** [Microcontroller plus circuit emulation](#microcontroller-plus-circuit-emulation)  
🏷️ **Tags:** [JavaScript software](programming-language.md#javascript-software)

[https://wokwi.com/](https://wokwi.com/)

<img src="https://web.archive.org/web/20250520035317im_/https://i0.wp.com/subethasoftware.com/wp-content/uploads/2022/12/wokwi-sample.png?resize=624%2C439&amp;ssl=1" alt="" height="600">

**[Figure 4](#_321)** [Source](https://subethasoftware.com/2022/12/18/wokwi-online-arduino-esp32-simulator/).

###### Microcontroller vs CPU

↑ **Parent:** [Microcontroller](#microcontroller)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Microcontroller_vs_CPU)

- [https://electronics.stackexchange.com/questions/1092/whats-the-difference-between-a-microcontroller-and-a-microprocessor](https://electronics.stackexchange.com/questions/1092/whats-the-difference-between-a-microcontroller-and-a-microprocessor)
- [https://electronics.stackexchange.com/questions/227796/why-are-relatively-simpler-devices-such-as-microcontrollers-so-much-slower-than](https://electronics.stackexchange.com/questions/227796/why-are-relatively-simpler-devices-such-as-microcontrollers-so-much-slower-than)

###### CPU architecture

↑ **Parent:** [Central processing unit](#central-processing-unit)  
🏷️ **Tags:** [Microarchitecture](#microarchitecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CPU_architecture)

###### Superscalar processor

↑ **Parent:** [CPU architecture](#cpu-architecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Superscalar_processor)

###### CPU functional unit

↑ **Parent:** [Superscalar processor](#superscalar-processor)

###### Instruction pipelining

↑ **Parent:** [CPU architecture](#cpu-architecture)

The first thing you must understand is the [Classic RISC pipeline](#classic-risc-pipeline) with a concrete example.

###### Educational [CPU microarchitecture](#cpu-architecture) simulator

↑ **Parent:** [Instruction pipelining](#instruction-pipelining)

###### freess

↑ **Parent:** [Educational CPU microarchitecture simulator](#educational-cpu-microarchitecture-simulator)

- [https://github.com/robgiorgi/freess](https://github.com/robgiorgi/freess)
- [https://arxiv.org/abs/2506.07665](https://arxiv.org/abs/2506.07665)

###### [JavaScript](programming-language.md#javascript) [CPU microarchitecture](#cpu-architecture) simulator

↑ **Parent:** [Educational CPU microarchitecture simulator](#educational-cpu-microarchitecture-simulator)  
🏷️ **Tags:** [JavaScript library](programming-language.md#javascript-library)

<h6 id="y86-js-org">y86.js.org</h6>

↑ **Parent:** [JavaScript CPU microarchitecture simulator](#javascript-cpu-microarchitecture-simulator)  
🏷️ **Tags:** [Y86](#y86)

- [https://y86.js.org/](https://y86.js.org/)
- [https://github.com/shuding/y86](https://github.com/shuding/y86)

The good:
- slick [UI](technology.md#user-interface)! But very hard to read characters, they're way too small.
- attempts to show state diffs with a flash. But it goes by too fast, would be better if it were more permanent
- [Reverse debugging](software.md#reverse-debugging)

The bad:
- educational [ISA](#instruction-set-architecture)
- unclear what flags mean from UI, no explanation on hover. Likely the authors assume knowledge of the [Y86](#y86) book.

###### WebRISC-V

↑ **Parent:** [JavaScript CPU microarchitecture simulator](#javascript-cpu-microarchitecture-simulator)  
🏷️ **Tags:** [RISC-V](#risc-v)

[https://webriscv.dii.unisi.it/](https://webriscv.dii.unisi.it/)

The good:
- [Reverse debugging](software.md#reverse-debugging)
- circuit diagram

The bad:
- Clunky [UI](technology.md#user-interface)
- circuit diagram doesn't show any state??

###### Hazard (computer architecture)

↑ **Parent:** [Instruction pipelining](#instruction-pipelining)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hazard_(computer_architecture))

###### Pipeline stall

↑ **Parent:** [Hazard (computer architecture)](#hazard-computer-architecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Pipeline_stall)

###### Classic RISC pipeline

↑ **Parent:** [Instruction pipelining](#instruction-pipelining)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Classic_RISC_pipeline)

###### Microprocessor

↑ **Parent:** [Central processing unit](#central-processing-unit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Microprocessor)

Basically a synonym for [central processing unit](#central-processing-unit) nowadays: [https://electronics.stackexchange.com/questions/44740/whats-the-difference-between-a-microprocessor-and-a-cpu](https://electronics.stackexchange.com/questions/44740/whats-the-difference-between-a-microprocessor-and-a-cpu)

###### CPU feature

↑ **Parent:** [Central processing unit](#central-processing-unit)

###### Trusted execution environment

↑ **Parent:** [CPU feature](#cpu-feature)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Trusted_execution_environment)

###### Software Guard Extensions

↑ **Parent:** [Trusted execution environment](#trusted-execution-environment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Software_Guard_Extensions)

The hole point of [Intel SGX](#software-guard-extensions) is to allow users to be certain that a certain code was executed in a remove server that they rent but don't own, like [AWS](#amazon-web-services). Even if [AWS](#amazon-web-services) wanted to be malicious, they would still not be able to modify your read your input, output nor modify the program.

The way this seems to work is as follows.

Each chip has its own unique private key embedded in the chip. There is no way for software to read that private key, only the hardware can read it, and Intel does not know that private key, only the corrsponding public one. The entire safety of the system relies on this key never ever leaking to anybody, even if they have the CPU in their hands. A big question is if there are physical forensic methods, e.g. using [electron microscopes](microscopy.md#electron-microscope), that would allow this key to be identified.

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

##### Field-programmable gate array

↑ **Parent:** [Type of processor](#type-of-processor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Field-programmable_gate_array)

It basically replaces a bunch of discrete [digital](electronics.md#digital-electronics) components with a single chip. So you don't have to wire things manually.

Particularly fundamental if you would be putting those chips up a thousand cell towers for signal processing, and ever felt the need to reprogram them! Resoldering would be fun, would it? So you just do a over the wire update of everything.

Vs a [microcontroller](#microcontroller): same reason why you would want to use discrete components: speed. Especially when you want to do a bunch of things in parallel fast.

One limitation is that it only handles digital electronics: [https://electronics.stackexchange.com/questions/25525/are-there-any-analog-fpgas](https://electronics.stackexchange.com/questions/25525/are-there-any-analog-fpgas) There are some analog analogs, but they are much more restricted due to signal loss, which is exactly what digital electronics is very good at mitigating.

<a id="video-first-fpga-experiences-with-a-digilent-cora-z7-xilinx-zynq-by-marco-reps-2018"></a>
**[Video 11](#video-first-fpga-experiences-with-a-digilent-cora-z7-xilinx-zynq-by-marco-reps-2018). First FPGA experiences with a Digilent Cora Z7 Xilinx Zynq by Marco Reps (2018)** [Source](https://www.youtube.com/watch?v=gl4CuzOH6I4). Good video, actually gives some rationale of a use case that a [microcontroller](#microcontroller) wouldn't handle because it is not fast enough.

<a id="video-fpga-dev-board-tutorial-by-ben-heck-2016"></a>
**[Video 12](#video-fpga-dev-board-tutorial-by-ben-heck-2016). FPGA Dev Board Tutorial by Ben Heck (2016)** [Source](https://www.youtube.com/watch?v=0zrqYy369NQ).

<a id="video-the-history-of-the-fpga-by-asianometry-2022"></a>
**[Video 13](#video-the-history-of-the-fpga-by-asianometry-2022). The History of the FPGA by Asianometry (2022)** [Source](https://www.youtube.com/watch?v=m-8G1Yixb34).

###### FPGA company

↑ **Parent:** [Field-programmable gate array](#field-programmable-gate-array)  
🏷️ **Tags:** [Semiconductor company](#semiconductor-company)

###### Xilinx

↑ **Parent:** [FPGA company](#fpga-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Xilinx)

##### Graphics processing unit

↑ **Parent:** [Type of processor](#type-of-processor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Graphics_processing_unit)

###### Discrete and integrated GPUs

↑ **Parent:** [Graphics processing unit](#graphics-processing-unit)

###### Discrete GPU

↑ **Parent:** [Discrete and integrated GPUs](#discrete-and-integrated-gpus)

###### Integrated GPU

↑ **Parent:** [Discrete and integrated GPUs](#discrete-and-integrated-gpus)

###### Video random-access memory

↑ **Parent:** [Graphics processing unit](#graphics-processing-unit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Video_random-access_memory)

In [discrete GPUs](#discrete-gpu), [VRAM](#video-random-access-memory) is [RAM](#random-access-memory) memory that lives on the [GPU](#graphics-processing-unit)'s [PCB](electronics.md#printed-circuit-board).

They are located in separate chips to the GPU's compute, since just like for [CPUs](#central-processing-unit), you can't put both on the same [chip](#integrated-circuit) as the manufacturing processes are different and incompatible.

[Integrated GPUs](#integrated-gpu) don't have [VRAM](#video-random-access-memory) and just instead use the same [RAM](#random-access-memory) as the [CPU](#central-processing-unit).

###### General-purpose computing on graphics processing units

↑ **Parent:** [Graphics processing unit](#graphics-processing-unit)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/General-purpose_computing_on_graphics_processing_units)

###### Open source GPU compute benchmark

↑ **Parent:** [General-purpose computing on graphics processing units](#general-purpose-computing-on-graphics-processing-units)

- [https://github.com/ekondis/mixbench](https://github.com/ekondis/mixbench) [GPL](law.md#gnu-general-public-license)
- [https://github.com/ProjectPhysX/OpenCL-Benchmark](https://github.com/ProjectPhysX/OpenCL-Benchmark) custom non-commercial, non-military license

###### GPU compute library

↑ **Parent:** [General-purpose computing on graphics processing units](#general-purpose-computing-on-graphics-processing-units)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/GPU_compute_library)

###### CUDA

↑ **Parent:** [GPU compute library](#gpu-compute-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/CUDA)

###### CUDA hello world

↑ **Parent:** [CUDA](#cuda)

Example: [https://github.com/cirosantilli/cpp-cheat/blob/d18a11865ac105507d036f8f12a457ad9686a664/cuda/inc.cu](https://github.com/cirosantilli/cpp-cheat/blob/d18a11865ac105507d036f8f12a457ad9686a664/cuda/inc.cu)

###### OpenCL

↑ **Parent:** [GPU compute library](#gpu-compute-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/OpenCL)

###### ROCm

↑ **Parent:** [GPU compute library](#gpu-compute-library)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ROCm)

Official hello world: [https://github.com/ROCm/HIP-Examples/blob/ff8123937c8851d86b1edfbad9f032462c48aa05/HIP-Examples-Applications/HelloWorld/HelloWorld.cpp](https://github.com/ROCm/HIP-Examples/blob/ff8123937c8851d86b1edfbad9f032462c48aa05/HIP-Examples-Applications/HelloWorld/HelloWorld.cpp)

###### ROCm on Ubuntu

↑ **Parent:** [ROCm](#rocm)

Tested on [Ubuntu 23.10](systems-programming.md#ubuntu-23-10) with [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd):
```
sudo apt install hipcc
git clone https://github.com/ROCm/HIP-Examples
cd HIP-Examples/HIP-Examples-Applications/HelloWorld
make
```
TODO fails with:
```
/bin/hipcc -g   -c -o HelloWorld.o HelloWorld.cpp
clang: error: cannot find ROCm device library for gfx1103; provide its path via '--rocm-path' or '--rocm-device-lib-path', or pass '-nogpulib' to build without ROCm device library
make: *** [<builtin>: HelloWorld.o] Error 1
```

Generic Ubuntu install bibliograpy:
- [https://askubuntu.com/questions/1429376/how-can-i-install-amd-rocm-5-on-ubuntu-22-04](https://askubuntu.com/questions/1429376/how-can-i-install-amd-rocm-5-on-ubuntu-22-04)
- [https://www.reddit.com/r/ROCm/comments/1438p6t/how_to_install_rocm_opencl_on_ubuntu_2304_rx580/](https://www.reddit.com/r/ROCm/comments/1438p6t/how_to_install_rocm_opencl_on_ubuntu_2304_rx580/)

##### AI accelerator

↑ **Parent:** [Type of processor](#type-of-processor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AI_accelerator)

<a id="video-the-coming-ai-chip-boom-by-asianometry-2022"></a>
**[Video 14](#video-the-coming-ai-chip-boom-by-asianometry-2022). The Coming AI Chip Boom by Asianometry (2022)** [Source](https://www.youtube.com/watch?v=L0948yq2Hqk).

###### Amazon AI accelerator silicon

↑ **Parent:** [AI accelerator](#ai-accelerator)  
🏷️ **Tags:** [Amazon custom silicon](amazon.md#amazon-custom-silicon)

- 2020: Traininum in 2020, e.g. [https://techcrunch.com/2020/12/01/aws-launches-trainium-its-new-custom-ml-training-chip/](https://techcrunch.com/2020/12/01/aws-launches-trainium-its-new-custom-ml-training-chip/)
- 2018: AWS Inferentia, mentioned at [https://en.wikipedia.org/wiki/Annapurna_Labs](https://en.wikipedia.org/wiki/Annapurna_Labs)

###### Tensor Processing Unit

↑ **Parent:** [AI accelerator](#ai-accelerator)  
🏷️ **Tags:** [Google custom hardware](google.md#google-custom-hardware)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tensor_Processing_Unit)

###### Tesla Dojo

↑ **Parent:** [AI accelerator](#ai-accelerator)

<h3 id="i-o-device">I/O device</h3>

↑ **Parent:** [Computer hardware component type](#computer-hardware-component-type)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/I/O_device)

#### Punched card

↑ **Parent:** [I/O device](#i-o-device)  
🏷️ **Tags:** [Display device](#display-device)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Punched_card)

Served as both input, output and [storage](#computer-data-storage) system in the eary days!

<a id="video-1964-ibm-029-keypunch-card-punching-demonstration-by-curiousmarc-2014"></a>
**[Video 15](#video-1964-ibm-029-keypunch-card-punching-demonstration-by-curiousmarc-2014). 1964 IBM 029 Keypunch Card Punching Demonstration by CuriousMarc (2014)** [Source](https://www.youtube.com/watch?v=YnnGbcM-H8c).

<a id="video-using-punch-cards-by-bubbles-whiting-2016"></a>
**[Video 16](#video-using-punch-cards-by-bubbles-whiting-2016). Using Punch Cards by Bubbles Whiting (2016)** [Source](https://www.youtube.com/watch?v=L7jAOcc9kBU). Interview at the [The Centre for Computing History](science.md#the-centre-for-computing-history).

<a id="video-once-upon-a-punched-card-by-ibm-1964"></a>
**[Video 17](#video-once-upon-a-punched-card-by-ibm-1964). Once Upon A Punched Card by IBM (1964)** [Source](https://www.youtube.com/watch?v=BlUWg2nxCz0). Goes on and on a bit too long. But cool still.

##### Hollerith tabulating machine

↑ **Parent:** [Punched card](#punched-card)

<a id="video-the-1890-us-census-and-the-history-of-punchcard-computing-by-stand-up-maths-2020"></a>
**[Video 18](#video-the-1890-us-census-and-the-history-of-punchcard-computing-by-stand-up-maths-2020). The 1890 US Census and the history of punchcard computing by Stand-up Maths (2020)** [Source](https://www.youtube.com/watch?v=YBnBAzrWeF0). It was basically a counting machine! Shows a reconstruction at the [Computer History Museum](science.md#computer-history-museum).

#### Computer input device

↑ **Parent:** [I/O device](#i-o-device)

#### Computer data storage

↑ **Parent:** [I/O device](#i-o-device)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computer_data_storage)

##### Computer data storage software

↑ **Parent:** [Computer data storage](#computer-data-storage)

###### Filesystem

↑ **Parent:** [Computer data storage software](#computer-data-storage-software)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Filesystem)

###### Clustered file system

↑ **Parent:** [Filesystem](#filesystem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Clustered_file_system)

###### 9P (protocol)

↑ **Parent:** [Clustered file system](#clustered-file-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/9P_(protocol))

###### Network File System

↑ **Parent:** [Clustered file system](#clustered-file-system)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Network_File_System)

###### Computer file

↑ **Parent:** [Filesystem](#filesystem)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computer_file)

###### File signature

↑ **Parent:** [Computer file](#computer-file)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/File_signature)

##### Computer data storage hardware

↑ **Parent:** [Computer data storage](#computer-data-storage)

###### Tape drive

↑ **Parent:** [Computer data storage hardware](#computer-data-storage-hardware)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Tape_drive)

One of the most enduring forms of storage! Started in the 1950s, but still used in the 2020s as the cheapest (and slowest access) archival method. Robot arms are needed to load and read them nowadays.

<a id="video-web-camera-mounted-insite-an-ibm-ts4500-tape-library-by-lkaptoor-2020"></a>
**[Video 19](#video-web-camera-mounted-insite-an-ibm-ts4500-tape-library-by-lkaptoor-2020). Web camera mounted insite an IBM TS4500 tape library by lkaptoor (2020)** [Source](https://www.youtube.com/watch?v=sYgnCWOVysY). Footage dated 2018.

###### Volatile memory

↑ **Parent:** [Computer data storage hardware](#computer-data-storage-hardware)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Volatile_memory)

###### Random-access memory

↑ **Parent:** [Volatile memory](#volatile-memory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Random-access_memory)

In conventional speech of the early 2000's, is basically a synonym for [dynamic random-access memory](#dynamic-random-access-memory).

###### Static random-access memory

↑ **Parent:** [Random-access memory](#random-access-memory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Static_random-access_memory)

###### Dynamic random-access memory

↑ **Parent:** [Random-access memory](#random-access-memory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dynamic_random-access_memory)

DRAM is often shortened to just [random-access memory](#random-access-memory).

###### Synchronous dynamic random-access memory

↑ **Parent:** [Dynamic random-access memory](#dynamic-random-access-memory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Synchronous_dynamic_random-access_memory)

###### DDR SDRAM

↑ **Parent:** [Synchronous dynamic random-access memory](#synchronous-dynamic-random-access-memory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/DDR_SDRAM)

###### Magnetoresistive RAM

↑ **Parent:** [Random-access memory](#random-access-memory)  
🏷️ **Tags:** [Non-volatile memory](#non-volatile-memory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Magnetoresistive_RAM)

###### Non-volatile memory

↑ **Parent:** [Computer data storage hardware](#computer-data-storage-hardware)

The opposite of [volatile memory](#volatile-memory).

###### Disk storage

↑ **Parent:** [Non-volatile memory](#non-volatile-memory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Disk_storage)

###### Disk read-and-write head

↑ **Parent:** [Disk storage](#disk-storage)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Disk_read-and-write_head)

###### Magnetoresistive disk head

↑ **Parent:** [Disk read-and-write head](#disk-read-and-write-head)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Disk_read-and-write_head#Magnetoresistive_heads_(MR_heads))

###### Optical storage

↑ **Parent:** [Non-volatile memory](#non-volatile-memory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Optical_storage)

![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2c/Blank_Recordable_DVD-R_Discs_underside_shallow_focus.JPG/500px-Blank_Recordable_DVD-R_Discs_underside_shallow_focus.JPG)

**[Figure 5](#_422)** [Source](https://commons.wikimedia.org/wiki/File:Blank_Recordable_DVD-R_Discs_underside_shallow_focus.JPG).

###### Solid-state storage

↑ **Parent:** [Non-volatile memory](#non-volatile-memory)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Solid-state_storage)

###### Erase SSD securely

↑ **Parent:** [Solid-state storage](#solid-state-storage)

You can't just [shred](systems-programming.md#shred-unix) individual [sSD](#solid-state-storage) files because SSD writes only at large granularities, so hardware/drivers have to copy stuff around all the time to compact it. This means that leftover copies are left around everywhere.

What you can do however is to erase the entire thing with vendor support, which most hardware has support for. On hardware encrypted disks, you can even just erase the keys:
- ATA: [https://www.thomas-krenn.com/en/wiki/Perform_a_SSD_Secure_Erase](https://www.thomas-krenn.com/en/wiki/Perform_a_SSD_Secure_Erase) for ATA.
- NVMe: [http://forum.notebookreview.com/threads/secure-erase-hdds-ssds-sata-nvme-using-hdparm-nvme-cli-on-linux.827525/](http://forum.notebookreview.com/threads/secure-erase-hdds-ssds-sata-nvme-using-hdparm-nvme-cli-on-linux.827525/)

TODO does shredding the

###### Solid-state drive

↑ **Parent:** [Computer data storage hardware](#computer-data-storage-hardware)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Solid-state_drive)

###### Flash memory

↑ **Parent:** [Solid-state drive](#solid-state-drive)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Flash_memory)

<a id="video-the-engineering-puzzle-of-storing-trillions-of-bits-in-your-smartphone-ssd-using-quantum-mechanics-by-branch-education-2020"></a>
**[Video 20](#video-the-engineering-puzzle-of-storing-trillions-of-bits-in-your-smartphone-ssd-using-quantum-mechanics-by-branch-education-2020). The Engineering Puzzle of Storing Trillions of Bits in your Smartphone / SSD using Quantum Mechanics by Branch Education (2020)** [Source](https://www.youtube.com/watch?v=5f2xOxRGKqk). Nice animations show how [quantum tunnelling](quantum-mechanics.md#quantum-tunnelling) is used to set bits in [flash memory](#flash-memory).

#### Peripheral

↑ **Parent:** [I/O device](#i-o-device)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Peripheral)

##### Computer mouse

↑ **Parent:** [Peripheral](#peripheral)  
🏷️ **Tags:** [I/O device](#i-o-device)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computer_mouse)

##### Computer keyboard

↑ **Parent:** [Peripheral](#peripheral)  
🏷️ **Tags:** [I/O device](#i-o-device)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computer_keyboard)

###### Keyboard layout

↑ **Parent:** [Computer keyboard](#computer-keyboard)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Keyboard_layout)

###### QWERTY

↑ **Parent:** [Keyboard layout](#keyboard-layout)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/QWERTY)

###### Dvorak keyboard layout

↑ **Parent:** [Keyboard layout](#keyboard-layout)  
🏷️ **Tags:** [Good](cirism.md#good), [Idealism](science.md#idealism)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dvorak_keyboard_layout)

Dvorak users will automatically go to [Heaven](religion.md#heaven).

###### Computer keyboard model

↑ **Parent:** [Computer keyboard](#computer-keyboard)

###### Kinesis Advantage keyboard

↑ **Parent:** [Computer keyboard model](#computer-keyboard-model)

###### Kinesis Advantage 2 keyboard

↑ **Parent:** [Computer keyboard model](#computer-keyboard-model)

[https://kinesis-ergo.com/shop/advantage2/](https://kinesis-ergo.com/shop/advantage2/)

For [Ciro Santilli](ciro-santilli.md), this is not a [computer keyboard](#computer-keyboard). It is a [fetish](brain.md#fetish).

##### Display device

↑ **Parent:** [Peripheral](#peripheral)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Display_device)

###### Blinkenlights

↑ **Parent:** [Display device](#display-device)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Blinkenlights)

###### E Ink

↑ **Parent:** [Display device](#display-device)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/E_Ink)

Electronic Ink such as that found on Amazon Kindle is the greatest invention ever made by man.

Once E Ink reaches reasonable refresh rates to replace liquid crystal displays, the world will finally be saved.

It would allow [Ciro Santilli](ciro-santilli.md) to spend his entire life in front of a screen rather in the real world without getting tired eyes, and even if it is sunny outside.

Ciro stopped reading non-code non-news a while back though, so the current refresh rates are useless, what a shame.

OMG, this is amazing: [https://getfreewrite.com/](https://getfreewrite.com/)

###### Amazon Kindle

↑ **Parent:** [E Ink](#e-ink)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Amazon_Kindle)

[PDF](computer.md#pdf) table of contents feature requests: [https://twitter.com/cirosantilli/status/1459844683925008385](https://twitter.com/cirosantilli/status/1459844683925008385)

###### Remarkable (tablet)

↑ **Parent:** [E Ink](#e-ink)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Remarkable_(tablet))

[Remarkable 2](#remarkable-2) is really, really good. Relatively fast refresh + touchscreen is amazing.

No official public feedback forum unfortunately:
- [https://twitter.com/cirosantilli/status/1459844683925008385](https://twitter.com/cirosantilli/status/1459844683925008385)
- [https://www.reddit.com/r/RemarkableTablet/comments/7h341m/official_remarkable_feedback_ideas_and/](https://www.reddit.com/r/RemarkableTablet/comments/7h341m/official_remarkable_feedback_ideas_and/)
- [https://www.reddit.com/r/RemarkableTablet/comments/7hxu70/link_for_remarkable_support_and_feature_requests/](https://www.reddit.com/r/RemarkableTablet/comments/7hxu70/link_for_remarkable_support_and_feature_requests/)

[PDF](computer.md#pdf) table of contents could be better: [https://twitter.com/cirosantilli/status/1459844683925008385](https://twitter.com/cirosantilli/status/1459844683925008385)

###### Remarkable 2

↑ **Parent:** [Remarkable (tablet)](#remarkable-tablet)

Display size: 10.3 inches. Perfect size

###### Teleprinter

↑ **Parent:** [Display device](#display-device)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Teleprinter)

Way, way before [instant messaging](messaging-software.md#instant-messaging), there was... teletype!

<a id="video-using-a-1930-teletype-as-a-linux-terminal-by-curiousmarc-2020"></a>
**[Video 21](#video-using-a-1930-teletype-as-a-linux-terminal-by-curiousmarc-2020). Using a 1930 Teletype as a Linux Terminal by CuriousMarc (2020)** [Source](https://www.youtube.com/watch?v=2XLZ4Z8LpEE).

##### Webcam

↑ **Parent:** [Peripheral](#peripheral)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Webcam)

##### Peripheral interface

↑ **Parent:** [Peripheral](#peripheral)

###### PCI

↑ **Parent:** [Peripheral interface](#peripheral-interface)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PCI)

<a id="video-pcie-computer-explained-by-explainingcomputers-2018"></a>
**[Video 22](#video-pcie-computer-explained-by-explainingcomputers-2018). PCIe computer explained by ExplainingComputers (2018)** [Source](https://www.youtube.com/watch?v=PrXwe21biJo).

###### PCIe

↑ **Parent:** [PCI](#pci)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/PCIe)

###### lspci

↑ **Parent:** [PCI](#pci)

`lspci` is the name of several versions of [CLI tools](software.md#command-line-utility) used in [UNIX](systems-programming.md#unix)-like systems to query information about [PCI](#pci) devices in the system.

On [Ubuntu 23.10](systems-programming.md#ubuntu-23-10), it is provided by the [pciutils](#pciutils) package, which is so dominant that when we say "lspci" without qualitication, that's what we mean.

###### pciutils

↑ **Parent:** [lspci](#lspci)

Sotware project that provides [lspci](#lspci).

###### Get vendor and device ID for each PCI device

↑ **Parent:** [lspci](#lspci)

[https://stackoverflow.com/questions/59010671/how-to-get-vendor-id-and-device-id-of-all-pci-devices](https://stackoverflow.com/questions/59010671/how-to-get-vendor-id-and-device-id-of-all-pci-devices)
```
grep PCI_ID /sys/bus/pci/devices/*/uevent
```

[lspci](#lspci) is missing such basic functionality!

###### USB

↑ **Parent:** [Peripheral interface](#peripheral-interface)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/USB)

###### USB Micro-B

↑ **Parent:** [USB](#usb)

###### USB-C

↑ **Parent:** [USB](#usb)  
🏷️ **Tags:** [Good](cirism.md#good)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/USB-C)

## Computer form factor

↑ **Parent:** [Computer hardware](computer-hardware.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Computer_form_factor)

### Embedded system

↑ **Parent:** [Computer form factor](#computer-form-factor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Embedded_system)

### Distributed computing

↑ **Parent:** [Computer form factor](#computer-form-factor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Distributed_computing)

#### Fog computing

↑ **Parent:** [Distributed computing](#distributed-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Fog_computing)

Our definition of fog computing: a system that uses the computational resources of individuals who volunteer their own devices, in which you give each of the volunteers part of a computational problem that you want to solve.

[Folding@home](#folding-at-home) and [SETI@home](#seti-at-home) are perfect example of that definition.

##### Charity Engine

↑ **Parent:** [Fog computing](#fog-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Charity_Engine)

<h5 id="folding-at-home">Folding@home</h5>

↑ **Parent:** [Fog computing](#fog-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Folding@home)

<h5 id="seti-at-home">SETI@home</h5>

↑ **Parent:** [Fog computing](#fog-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/SETI@home)

##### Is fog computing more efficient than cloud computing?

↑ **Parent:** [Fog computing](#fog-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Is_fog_computing_more_efficient_than_cloud_computing?)

Advantages of fog: there is only one, reusing hardware that would be otherwise idle.

Disadvantages:
- in cloud, you can put your datacenter on the location with the cheapest possible power. On fog you can't.
- on fog there is some waste due to network communication.
- you will likely optimize code less well because you might be targeting a wide array of different types of hardware, so more power (and time) wastage. Furthermore, some of the hardware used will not not be optimal for the task, e.g. [CPU](#central-processing-unit) instead of [GPU](#graphics-processing-unit).

All of this makes [Ciro Santilli](ciro-santilli.md) doubtful if it wouldn't be more efficient for volunteers simply to donate money rather than inefficient power usage.

Bibliography:
- [https://greenfoldingathome.com/2018/05/28/is-foldinghome-a-waste-of-electricity/](https://greenfoldingathome.com/2018/05/28/is-foldinghome-a-waste-of-electricity/): useless article, does not compare to centralize, asks if folding the proteins is worth the power usage...

### Mainframe computer

↑ **Parent:** [Computer form factor](#computer-form-factor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mainframe_computer)

### Cloud computing

↑ **Parent:** [Computer form factor](#computer-form-factor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cloud_computing)

#### Cloud computing market share

↑ **Parent:** [Cloud computing](#cloud-computing)

<a id="image-cloud-computing-market-share-in-q2-2022-by-statista-com"></a>
![](https://web.archive.org/web/20220826031044im_/https://cdn.statcdn.com/Infographic/images/normal/18819.jpeg)

**[Figure 6](#image-cloud-computing-market-share-in-q2-2022-by-statista-com). Cloud Computing market share in Q2 2022 by statista.com**. [Source](https://www.statista.com/chart/18819/worldwide-market-share-of-leading-cloud-infrastructure-service-providers/).

#### Hyperscale computing

↑ **Parent:** [Cloud computing](#cloud-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Hyperscale_computing)

Basically means "company with huge server farms, and which usually rents them out like [Amazon AWS](#amazon-web-services) or [Google Cloud Platform](#google-cloud-platform)

<a id="image-global-electricity-use-by-data-center-type-2010-vs-2018"></a>
![](https://web.archive.org/web/20220803073556im_/https://energyinnovation.org/wp-content/uploads/2020/03/Estimated-global-data-electricity-use-by-data-center-type.png)

**[Figure 7](#image-global-electricity-use-by-data-center-type-2010-vs-2018). Global electricity use by data center type: 2010 vs 2018**. [Source](https://energyinnovation.org/2020/03/17/how-much-energy-do-data-centers-really-use/). The growth of [hyperscaler](#hyperscale-computing) cloud vs smaller cloud and private deployments was incredible in that period!

#### Cloud computing platform

↑ **Parent:** [Cloud computing](#cloud-computing)

##### Amazon Web Services

↑ **Parent:** [Cloud computing platform](#cloud-computing-platform)  
🏷️ **Tags:** [Amazon product](amazon.md#amazon-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Amazon_Web_Services)

###### aws-cli

↑ **Parent:** [Amazon Web Services](#amazon-web-services)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/aws-cli)

###### AWS service

↑ **Parent:** [Amazon Web Services](#amazon-web-services)

###### Amazon Athena

↑ **Parent:** [AWS service](#aws-service)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Amazon_Athena)

[Google BigQuery](google.md#google-bigquery) alternative.

###### Amazon Redshift

↑ **Parent:** [AWS service](#aws-service)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Amazon_Redshift)

###### Amazon S3

↑ **Parent:** [AWS service](#aws-service)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Amazon_S3)

###### Browse S3 bucket on web browser

↑ **Parent:** [Amazon S3](#amazon-s3)

They can't even make this basic stuff just work!
- [https://stackoverflow.com/questions/16784052/access-files-stored-on-amazon-s3-through-web-browser](https://stackoverflow.com/questions/16784052/access-files-stored-on-amazon-s3-through-web-browser)

###### Amazon Elastic Compute Cloud

↑ **Parent:** [AWS service](#aws-service)  
🏷️ **Tags:** [Platform as a service](#platform-as-a-service)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Amazon_Elastic_Compute_Cloud)

###### Amazon EC2 HOWTO

↑ **Parent:** [Amazon Elastic Compute Cloud](#amazon-elastic-compute-cloud)

###### Amazon EC2 hello world

↑ **Parent:** [Amazon EC2 HOWTO](#amazon-ec2-howto)  
🏷️ **Tags:** [Hello world](software.md#hello-world-program)

Let's get [SSH](computer.md#secure-shell) access, instal a package, and run a server.

As of December 2023 on a `t2.micro` instance, the only one part of free tier at the time with advertised 1 vCPU, 1 GiB RAM, 8 GiB disk for the first 12 months, on [Ubuntu 22.04](systems-programming.md#ubuntu-22-04):
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

###### Amazon EC2 GPU

↑ **Parent:** [Amazon EC2 HOWTO](#amazon-ec2-howto)

As of December 2023, the cheapest instance with an [Nvidia GPU](#nvidia-gpu) is [g4nd.xlarge](#g4nd-xlarge), so let's try that out. In that instance, [lspci](#lspci) contains:
```
00:1e.0 3D controller: NVIDIA Corporation TU104GL [Tesla T4] (rev a1)
```
so we see that it runs a [Nvidia T4](#nvidia-t4) GPU.

Be careful not to confuse it with [g4ad.xlarge](#g4ad-xlarge), which has an [AMD GPU](#amd-gpu) instead. TODO meaning of "ad"? "a" presumably means [AMD](#amd), but what is the "d"?

Some documentation on which GPU is in each instance can seen at: [https://docs.aws.amazon.com/dlami/latest/devguide/gpu.html](https://docs.aws.amazon.com/dlami/latest/devguide/gpu.html) ([archive](https://web.archive.org/web/20231126224245/https://docs.aws.amazon.com/dlami/latest/devguide/gpu.html)) with a list of which GPUs they have at that random point in time. Can the GPU ever change for a given instance name? Likely not. Also as of December 2023 the list is already outdated, e.g. P5 is now shown, though it is mentioned at: [https://aws.amazon.com/ec2/instance-types/p5/](https://aws.amazon.com/ec2/instance-types/p5/)

When selecting the instance to launch, the GPU does not show anywhere apparently on the instance information page, it is so bad!

Also note that this instance has 4 vCPUs, so on a new account you must first make a customer support request to Amazon to increase your limit from the default of 0 to 4, see also: [https://stackoverflow.com/questions/68347900/you-have-requested-more-vcpu-capacity-than-your-current-vcpu-limit-of-0](https://stackoverflow.com/questions/68347900/you-have-requested-more-vcpu-capacity-than-your-current-vcpu-limit-of-0), otherwise instance launch will fail with:

> You have requested more vCPU capacity than your current vCPU limit of 0 allows for the instance bucket that the specified instance type belongs to. Please visit [http://aws.amazon.com/contact-us/ec2-request](http://aws.amazon.com/contact-us/ec2-request) to request an adjustment to this limit.

When starting up the instance, also select:
- image: [Ubuntu 22.04](systems-programming.md#ubuntu-22-04)
- storage size: 30 GB (maximum free tier allowance)
Once you finally managed to [SSH](computer.md#secure-shell) into the instance, first we have to install drivers and reboot:
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

If we start from the raw [Ubuntu 22.04](systems-programming.md#ubuntu-22-04), first we have to install drivers:
- [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/install-nvidia-driver.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/install-nvidia-driver.html) official docs
- [https://stackoverflow.com/questions/63689325/how-to-activate-the-use-of-a-gpu-on-aws-ec2-instance](https://stackoverflow.com/questions/63689325/how-to-activate-the-use-of-a-gpu-on-aws-ec2-instance)
- [https://askubuntu.com/questions/1109662/how-do-i-install-cuda-on-an-ec2-ubuntu-18-04-instance](https://askubuntu.com/questions/1109662/how-do-i-install-cuda-on-an-ec2-ubuntu-18-04-instance)
- [https://askubuntu.com/questions/1397934/how-to-install-nvidia-cuda-driver-on-aws-ec2-instance](https://askubuntu.com/questions/1397934/how-to-install-nvidia-cuda-driver-on-aws-ec2-instance)

From there basically everything should just work as normal. E.g. we were able to run a [CUDA hello world](#cuda-hello-world) just fine along:
```
nvcc inc.cu
./a.out
```

One issue with this setup, besides the time it takes to setup, is that you might also have to pay some network charges as it downloads a bunch of stuff into the instance. We should try out some of the pre-built images. But it is also good to know this pristine setup just in case.

We then managed to run [Ollama](artificial-intelligence.md#ollama) just fine with:
```
curl https://ollama.ai/install.sh | sh
/bin/time ollama run llama2 'What is quantum field theory?'
```
which gave:
```
0.07user 0.05system 0:16.91elapsed 0%CPU (0avgtext+0avgdata 16896maxresident)k
0inputs+0outputs (0major+1960minor)pagefaults 0swaps
```
so way faster than on my local desktop [CPU](#central-processing-unit), hurray.

After setup from: [https://askubuntu.com/a/1309774/52975](https://askubuntu.com/a/1309774/52975) we were able to run:
```
head -n1000 pap.txt | ARGOS_DEVICE_TYPE=cuda time argos-translate --from-lang en --to-lang fr > pap-fr.txt
```
which gave:
```
77.95user 2.87system 0:39.93elapsed 202%CPU (0avgtext+0avgdata 4345988maxresident)k
0inputs+88outputs (0major+910748minor)pagefaults 0swaps
```
so only marginally better than on [P14s](ciro-santilli-s-hardware.md#lenovo-thinkpad-p14s-gen4-amd). It would be fun to see how much faster we could make things on a more powerful GPU.

###### Amazon Machine Image

↑ **Parent:** [Amazon Elastic Compute Cloud](#amazon-elastic-compute-cloud)

###### List of AWS AMIs

↑ **Parent:** [Amazon Machine Image](#amazon-machine-image)

<h6 id="aws-deep-learning-base-gpu-ami-ubuntu-20-04">AWS Deep Learning Base GPU AMI (Ubuntu 20.04)</h6>

↑ **Parent:** [List of AWS AMIs](#list-of-aws-amis)  
🏷️ **Tags:** [Ubuntu 20.04](systems-programming.md#ubuntu-20-04)

These come with pre-installed drivers, so e.g. [nvidia-smi](#nvidia-smi) just works on them out of the box, tested on [g5.xlarge](#g5-xlarge) which has an [Nvidia A10G](#nvidia-a10g) GPU. Good choice as a starting point for [deep learning](machine-learning.md#deep-learning) experiments.

###### Amazon Elastic Block Store

↑ **Parent:** [Amazon Elastic Compute Cloud](#amazon-elastic-compute-cloud)

###### Laucnh Amazin EC2 with existing EBS volume

↑ **Parent:** [Amazon Elastic Block Store](#amazon-elastic-block-store)

Not possible directly without first creating an AMI image from snapshot? So annoying!
- [https://serverfault.com/questions/639537/booting-an-ec2-instance-from-an-existing-ebs-volume](https://serverfault.com/questions/639537/booting-an-ec2-instance-from-an-existing-ebs-volume)
- [https://stackoverflow.com/questions/71847637/aws-ec2-how-to-use-pre-existing-ebs-volume-as-main-bootable-disk](https://stackoverflow.com/questions/71847637/aws-ec2-how-to-use-pre-existing-ebs-volume-as-main-bootable-disk)

The hot and more expensive sotorage for [Amazon EC2](#amazon-elastic-compute-cloud), where e.g. your [Ubuntu](systems-programming.md#ubuntu) filesystem will lie.

The cheaper and slower alternative is to use [Amazon S3](#amazon-s3).

###### EC2 instance store volume

↑ **Parent:** [Amazon Elastic Compute Cloud](#amazon-elastic-compute-cloud)

Large but ephemeral storage for EC2 instances. Predetermined by the [EC2 instance type](#ec2-instance-type). Stays in the local server disk. Not automatically mounted.
- [https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html) ([archive](https://web.archive.org/web/20231214213241/https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html)) notably highlights what it persists, which is basically nothing
- [https://serverfault.com/questions/433703/how-to-use-instance-store-volumes-storage-in-amazon-ec2](https://serverfault.com/questions/433703/how-to-use-instance-store-volumes-storage-in-amazon-ec2) mentions that you have to mount it

###### vCPU

↑ **Parent:** [Amazon Elastic Compute Cloud](#amazon-elastic-compute-cloud)

###### EC2 instance type

↑ **Parent:** [Amazon Elastic Compute Cloud](#amazon-elastic-compute-cloud)

[Amazon](amazon.md)'s informtion about their own intances is so bad and non-public that this was created: [https://instances.vantage.sh/](https://instances.vantage.sh/)

<h6 id="g4ad-xlarge">g4ad.xlarge</h6>

↑ **Parent:** [EC2 instance type](#ec2-instance-type)

[AMD GPUs](#amd-gpu) as mentioned at: [https://aws.amazon.com/ec2/instance-types/g4/](https://aws.amazon.com/ec2/instance-types/g4/)

<h6 id="g4nd-xlarge">g4nd.xlarge</h6>

↑ **Parent:** [EC2 instance type](#ec2-instance-type)

1 [Nvidia T4](#nvidia-t4) GPU, 4 [vCPUs](#vcpu).

Mentioned at: [https://aws.amazon.com/ec2/instance-types/g4/](https://aws.amazon.com/ec2/instance-types/g4/)

TODO meaning of "nd"? "n" presumably means [Nvidia](#nvidia), but what is the "d"? Compare it [g4ad.xlarge](#g4ad-xlarge) which has AMD GPUs. [https://aws.amazon.com/ec2/instance-types/g4/](https://aws.amazon.com/ec2/instance-types/g4/) mentions:

> G4 instances are available with a choice of NVIDIA GPUs (G4dn) or AMD GPUs (G4ad).

Price:
- 2025-03-10: 0.526 USD / Hour

<h6 id="g5-xlarge">g5.xlarge</h6>

↑ **Parent:** [EC2 instance type](#ec2-instance-type)

1 [Nvidia A10G](#nvidia-a10g) GPU, 4 [vCPUs](#vcpu).

##### Alibaba Cloud

↑ **Parent:** [Cloud computing platform](#cloud-computing-platform)  
🏷️ **Tags:** [Alibaba product](computer.md#alibaba-product)

##### Google Cloud Platform

↑ **Parent:** [Cloud computing platform](#cloud-computing-platform)  
🏷️ **Tags:** [Google product](google.md#google-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Google_Cloud_Platform)

#### Type of cloud computing

↑ **Parent:** [Cloud computing](#cloud-computing)

##### Infrastructure as a service

↑ **Parent:** [Type of cloud computing](#type-of-cloud-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Infrastructure_as_a_service)

You [SSH](computer.md#secure-shell) into a an OS like [Ubuntu](systems-programming.md#ubuntu) and do whatever you want from there. E.g. [Amazon EC2](#amazon-elastic-compute-cloud).

The OS is usually virualized, and you get only a certain share of the CPU by default.

##### Platform as a service

↑ **Parent:** [Type of cloud computing](#type-of-cloud-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Platform_as_a_service)

Highly managed, you don't even see the [Docker](systems-programming.md#docker-software) images, only some higher level [JSON](computer.md#json) configuration file.

These setups are really convenient and cheap, and form a decent way to try out a new website with simple requirements.

###### AWS Elastic Beanstalk

↑ **Parent:** [Platform as a service](#platform-as-a-service)  
🏷️ **Tags:** [Amazon Web Services](#amazon-web-services)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AWS_Elastic_Beanstalk)

###### Heroku

↑ **Parent:** [Platform as a service](#platform-as-a-service)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Heroku)

This feels good.

One problem though is that Heroku is very opinionated, a likely like other PaaSes. So if you are trying something that is slightly off the mos common use case, you might be fucked.

Another problem with Heroku is that it is extremely difficult to debug a build that is broken on Heroku but not locally. We needed a way to be able to drop into a shell in the middle of build in case of failure. Otherwise it is impossible.

Deployment:
```
git push heroku HEAD:master
```

View [stdout](systems-programming.md#standard-output) logs:
```
heroku logs --tail
```

[PostgreSQL](sql.md#postgresql) database, it seems to be delegated to [AWS](#amazon-web-services). How to browse database: [https://stackoverflow.com/questions/20410873/how-can-i-browse-my-heroku-database](https://stackoverflow.com/questions/20410873/how-can-i-browse-my-heroku-database)
```
heroku pg:psql
```

Drop and recreate database:
```
heroku pg:reset --confirm <app-name>
```
All tables are destroyed.

Restart app:
```
heroku restart
```

###### Send free emails from Heroku

↑ **Parent:** [Heroku](#heroku)

Arghh, why so hard... tested 2021:
- [SendGrid](messaging-software.md#sendgrid): this one is the first one I got working on free tier!
- Mailgun: the Heroku add-on creates a free plan. This is smaller than the flex plan and does not allow custom domains, and is not available when signing up on mailgun.com directly: [https://help.mailgun.com/hc/en-us/articles/203068914-What-Are-the-Differences-Between-the-Free-and-Flex-Plans-](https://help.mailgun.com/hc/en-us/articles/203068914-What-Are-the-Differences-Between-the-Free-and-Flex-Plans-) And without custom domains you cannot send emails to anyone, only to people in the 5 manually whitelisted list, thus making this worthless. Also, gmail is not able to verify the DNS of the sandbox emails, and they go to spam.

  Mailgun does feel good otherwise if you are willing to pay. Their Heroku integration feels great, exposes everything you need on environment variables straight away.
- CloudMailin: does not feel as well developed as Mailgun. More focus on receiving. Tried adding TXT xxx.\_domainkey.ourbigbook.com and CNAME mta.ourbigbook.com entires with custom domain to see if it works, took forever to find that page... [https://www.cloudmailin.com/outbound/domains/xxx](https://www.cloudmailin.com/outbound/domains/xxx) Domain verification requires a bit of human contact via email.

  They also don't document their Heroku usage well. The envvars generated on Heroku are useless, only to login on their web UI. The send username and password must be obtained on their confusing web ui.

### High performance computing

↑ **Parent:** [Computer form factor](#computer-form-factor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/High_performance_computing)

#### Job scheduler

↑ **Parent:** [High performance computing](#high-performance-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Job_scheduler)

##### Borg (cluster manager)

↑ **Parent:** [Job scheduler](#job-scheduler)  
🏷️ **Tags:** [Software developed by Google](google.md#software-developed-by-google)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Borg_(cluster_manager))

##### IBM Spectrum LSF

↑ **Parent:** [Job scheduler](#job-scheduler)

###### LSF get version

↑ **Parent:** [IBM Spectrum LSF](#ibm-spectrum-lsf)

Most/all commands have the `-V` option which prints the version, e.g.:
```
bsub -V
```

###### LSF command

↑ **Parent:** [IBM Spectrum LSF](#ibm-spectrum-lsf)

###### bsub

↑ **Parent:** [LSF command](#lsf-command)

Submit a new job. The most important command!

Docs: [https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=bsub-options](https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=bsub-options)

###### bsub get job stdout and stderr

↑ **Parent:** [bsub](#bsub)

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

Another option is to run with the [bsub `-I` option](#bsub-i-option):
```
bsub -I 'echo a;sleep 1;echo b;sleep 1;echo c'
```
This immediately prints stdout and stderr to the terminal.

###### bsub on foreground

↑ **Parent:** [bsub](#bsub)

Run `bsub` on foreground, show stdout on host stdout live with an interactive with the [bsub `-I` option](#bsub-i-option):
```
bsub -I 'echo a;sleep 1;echo b;sleep 1;echo c'; echo done
```
Ctrl + C kills the job on remote as well as locally.

Bibliography:
- [https://superuser.com/questions/46312/wait-for-one-or-all-lsf-jobs-to-complete](https://superuser.com/questions/46312/wait-for-one-or-all-lsf-jobs-to-complete)

###### bsub option

↑ **Parent:** [bsub](#bsub)

<h6 id="bsub-i-option">bsub <code>-I</code> option</h6>

↑ **Parent:** [bsub](#bsub)

[https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=options-i](https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=options-i)

###### bpeek

↑ **Parent:** [LSF command](#lsf-command)

View stdout/stderr of a running job.

Documented at: [https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=reference-bpeek](https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=reference-bpeek)

Documented at:
- [https://www.bsc.es/support/LSF/9.1.2/lsf_command_ref/index.htm?bpeek.1.html~main](https://www.bsc.es/support/LSF/9.1.2/lsf_command_ref/index.htm?bpeek.1.html~main)

###### bkill

↑ **Parent:** [LSF command](#lsf-command)

Kill jobs.

Documented at: [https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=reference-bkill](https://www.ibm.com/docs/en/spectrum-lsf/10.1.0?topic=reference-bkill)

###### bkill all jobs

↑ **Parent:** [LSF command](#lsf-command)

By the current user:
```
bkill 0
```

#### Slurm Workload Manager

↑ **Parent:** [High performance computing](#high-performance-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Slurm_Workload_Manager)

#### Supercomputer

↑ **Parent:** [High performance computing](#high-performance-computing)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Supercomputer)

Some good insights on the earlier history of the industry at: [The Supermen: The Story of Seymour Cray by Charles J. Murray (1997)](computer.md#the-supermen-the-story-of-seymour-cray-by-charles-j-murray-1997).

##### Exascale computing

↑ **Parent:** [Supercomputer](#supercomputer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Exascale_computing)

First publicly reached by [Frontier](#frontier-supercomputer).

###### Exascale hypothesis

↑ **Parent:** [Exascale computing](#exascale-computing)

The "exascale hypothesis" is a name made up by [Ciro Santilli](ciro-santilli.md) to refer to the hypothesis that the real-time human [brain simulation](brain.md#brain-simulation) becomes possible at [exascale computing](#exascale-computing).

It is a simple extrapolation from the [number of synapses in the human brain](brain.md#number-of-synapses-in-the-human-brain) ($10^{15}$) times the number of times each neuron fires per second.

##### TOP500

↑ **Parent:** [Supercomputer](#supercomputer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/TOP500)

##### Supercomputer by owner

↑ **Parent:** [Supercomputer](#supercomputer)

###### Oak Ridge supercomputer

↑ **Parent:** [Supercomputer by owner](#supercomputer-by-owner)  
🏷️ **Tags:** [Oak Ridge National Laboratory](research-institute.md#oak-ridge-national-laboratory)

###### Frontier (supercomputer)

↑ **Parent:** [Oak Ridge supercomputer](#oak-ridge-supercomputer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Frontier_(supercomputer))

##### Intel supercomputer market share

↑ **Parent:** [Supercomputer](#supercomputer)  
🏷️ **Tags:** [Intel](#intel)

<a id="image-intel-supercomputer-market-share-from-1993-to-2020"></a>
![](https://web.archive.org/web/20210908201649im_/https://3s81si1s5ygj3mzby34dq6qf-wpengine.netdna-ssl.com/wp-content/uploads/2020/06/top500-june-2020-chip-technology.jpg)

**[Figure 8](#image-intel-supercomputer-market-share-from-1993-to-2020). Intel supercomputer market share from 1993 to 2020**. [Source](https://www.nextplatform.com/2020/06/22/arm-and-japan-get-their-day-in-the-hpc-sun/). This graph is shocking, they just took over the entire market! Some good pre-Intel context at [The Supermen: The Story of Seymour Cray by Charles J. Murray (1997)](computer.md#the-supermen-the-story-of-seymour-cray-by-charles-j-murray-1997), e.g. in those earlier days, custom architectures like [Cray](computer.md#cray)'s and many others dominated.

### Personal computer

↑ **Parent:** [Computer form factor](#computer-form-factor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Personal_computer)

#### Laptop

↑ **Parent:** [Personal computer](#personal-computer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Laptop)

#### Desktop computer

↑ **Parent:** [Personal computer](#personal-computer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Desktop_computer)

#### Mobile phone

↑ **Parent:** [Personal computer](#personal-computer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mobile_phone)

##### History of mobile phone

↑ **Parent:** [Mobile phone](#mobile-phone)

##### The first application of mobile phones was in motor vehicles

↑ **Parent:** [Mobile phone](#mobile-phone)

Early models were heavy and not practical for people to carry them, so the main niche they initially filled was being carried in [motor vehicles](technology.md#motor-vehicle), notably trucks where drivers are commercially driving all day long.

It also helps in the case of trucks that you only need to cover a one-dimensional region of the main roads.

For example, this niche was the original entry point of companies such as:
- [Qualcomm](#qualcomm)
- [MCI Communications](https://ourbigbook.com/go/topic/mci-communications)

##### Smartphone

↑ **Parent:** [Mobile phone](#mobile-phone)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Smartphone)

##### Mobile app

↑ **Parent:** [Mobile phone](#mobile-phone)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Mobile_app)

### Workstation

↑ **Parent:** [Computer form factor](#computer-form-factor)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Workstation)

## Computer manufacturer

↑ **Parent:** [Computer hardware](computer-hardware.md)

This section is about companies that integrate parts and software from various other companies to make up fully working computer systems.

### Dell

↑ **Parent:** [Computer manufacturer](#computer-manufacturer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Dell)

### Lenovo

↑ **Parent:** [Computer manufacturer](#computer-manufacturer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lenovo)

Their websites a bit [shitty](molecular-biology.md#feces), clearly a non cohesive amalgamation of several different groups.

E.g. you have to create several separate accounts, and different regions have completely different accounts and websites.

The [Europe](continent.md#europe) replacement part website for example is clearly made by a third party called [https://flex.com/](https://flex.com/) and has Flex written all over it, and the header of the home page has a slightly broken but very obviously broken CSS. And you can't create an account without a VAT number... and they confirmed by email that they don't sell to non-corporate entities without a VAT number. What a [bullshit](molecular-biology.md#bullshit)!

#### ThinkPad

↑ **Parent:** [Lenovo](#lenovo)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ThinkPad)

This is [Ciro Santilli](ciro-santilli.md)'s favorite laptop brand. He's been on it since the early 2010's after he saw his [then-girlfriend-later-wife](ciro-santilli.md#ciro-santilli-s-wife) using it.

Ciro doesn't know how to explain it, but ThinkPads just feel... right. The screen, the keyboard, the lid, the touchpad are all exactly what Ciro likes.

The only problem with ThinkPad is that it is owned by [Lenovo](#lenovo) which is a [Chinese company](the-most-important-projects-done-by-ciro-santilli.md#ciro-santilli-s-campaign-for-freedom-of-speech-in-china), and that makes Ciro feel bad. But he likes it too much to quit... what to do?

Ciro is also reassured to see that in every enterprise he's been so far as of 2020, ThinkPads are very dominant. And the same when you see internal videos from other big tech enterprises, all those nerds are running... Ubuntu on ThinkPads! And the [ISS](https://en.wikipedia.org/wiki/File:ISS-38_EVA-1_Laptops.jpg).

Those nerds like their ThinkPads so much, that Ciro has seen some acquaintances with crazy old ThinkPad machines, missing keyboard buttons or the like. They just like their machines that much.

ThinkPads are are also designed for repairability, and it is easy to buy replacement parts, and there are OEM part replacement video tutorials: [https://www.youtube.com/watch?v=vseFzFFz8lY](https://www.youtube.com/watch?v=vseFzFFz8lY) No visible [planned obsolescence](cirism.md#planned-obsolescence) here! With the caveat that the official online part stores can be [shit](molecular-biology.md#feces) as mentioned at [Section "Lenovo"](#lenovo).

Further more, in 2020 Lenovo is announced full certification for [Ubuntu](systems-programming.md#ubuntu) [https://www.forbes.com/sites/jasonevangelho/2020/06/03/lenovos-massive-ubuntu-and-red-hat-announcement-levels-up-linux-in-2020/#28a8fd397ae0](https://www.forbes.com/sites/jasonevangelho/2020/06/03/lenovos-massive-ubuntu-and-red-hat-announcement-levels-up-linux-in-2020/#28a8fd397ae0) which _fantastic_ news!

The only thing Ciro never understood is the trackpoint: [https://superuser.com/questions/225059/how-to-get-used-of-trackpoint-on-a-thinkpad](https://superuser.com/questions/225059/how-to-get-used-of-trackpoint-on-a-thinkpad) Why would you use that with such an amazing touchpad? And [vimium](software.md#vimium).

##### ThinkPad series

↑ **Parent:** [ThinkPad](#thinkpad)

[https://www.reddit.com/r/thinkpad/comments/crw08i/series_differences_t_vs_x_vs_p_vs_e_vs_etc/](https://www.reddit.com/r/thinkpad/comments/crw08i/series_differences_t_vs_x_vs_p_vs_e_vs_etc/)

### Raspberry Pi Foundation

↑ **Parent:** [Computer manufacturer](#computer-manufacturer)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Raspberry_Pi_Foundation)

#### Raspberry Pi Foundation project

↑ **Parent:** [Raspberry Pi Foundation](#raspberry-pi-foundation)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Raspberry_Pi_Foundation_project)

##### Raspberry Pi OS

↑ **Parent:** [Raspberry Pi Foundation project](#raspberry-pi-foundation-project)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Raspberry_Pi_OS)

Change password without access:
- [https://raspberrypi.stackexchange.com/questions/24770/change-reset-password-without-monitor-keyboard](https://raspberrypi.stackexchange.com/questions/24770/change-reset-password-without-monitor-keyboard)

Enable SSH on boot:
- `sudo touch /boot/ssh`

##### Raspberry Pi

↑ **Parent:** [Raspberry Pi Foundation project](#raspberry-pi-foundation-project)  
🏷️ **Tags:** [Devboard](electronics.md#microprocessor-development-board)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Raspberry_Pi)

###### Raspberry Pi 1

↑ **Parent:** [Raspberry Pi](#raspberry-pi)

###### Raspberry Pi 2

↑ **Parent:** [Raspberry Pi](#raspberry-pi)

Model B V 1.1.

SoC: BMC2836

[https://www.raspberrypi.org/products/raspberry-pi-2-model-b/](https://www.raspberrypi.org/products/raspberry-pi-2-model-b/)

###### Raspberry Pi 3

↑ **Parent:** [Raspberry Pi](#raspberry-pi)

Model B V 1.2.

SoC: BCM2837

Serial from `cat /proc/cpuinfo`: 00000000c77ddb77

###### Raspberry Pi Pico

↑ **Parent:** [Raspberry Pi](#raspberry-pi)  
🏷️ **Tags:** [Microcontroller devboard](electronics.md#microcontroller-devboard)

Some key specs:
- [SoC](#system-on-a-chip):
  - name: RP2040. Custom designed by [Raspberry Pi Foundation](#raspberry-pi-foundation), likely the first they make themselves rather than using a [Broadcom](#broadcom) chip. But the design still is closed source, likely wouldn't be easy to open source due to the usage of closed proprietary IP like the [ARM](#arm-architecture-family)
  - dual core [ARM Cortex-M0+](#arm-cortex-m0-plus)
  - frequency: 2 kHz to 133 MHz, 125 MHz by default
  - memory: 264KB on-chip [SRAM](#static-random-access-memory)
- GPIO voltage: 3.3V

Datasheet: [https://datasheets.raspberrypi.com/pico/pico-datasheet.pdf](https://datasheets.raspberrypi.com/pico/pico-datasheet.pdf)

![](https://web.archive.org/web/20220808214856im_/https://twilio-cms-prod.s3.amazonaws.com/images/6ofE97USO9rBn4LidgxTgfrAqK0UiI3v524IPNHc7ac3SA.width-800.png)

**[Figure 9](#_667)** [Source](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf).

###### [Raspberry Pi Pico](#raspberry-pi-pico) getting started

↑ **Parent:** [Raspberry Pi Pico](#raspberry-pi-pico)

Getting started on [Ubuntu 25.04](systems-programming.md#ubuntu-25-04): see: [Program Raspberry Pi Pico W with X](#program-raspberry-pi-pico-w-with-x).

Then ignore the other steps from the tutorial, as theese use the picozero package, which is broken with this error: [https://github.com/raspberrypilearning/getting-started-with-the-pico/issues/57](https://github.com/raspberrypilearning/getting-started-with-the-pico/issues/57)
```
AttributeError: module 'pkgutil' has no attribute 'ImpImporter'. Did you mean: 'zipimporter'
```
and uses picozero specific code. Rather, just use our examples from [rpi-pico-w](rpi-pico-w).

###### Flash the Raspberry Pi Pico

↑ **Parent:** [Raspberry Pi Pico getting started](#raspberry-pi-pico-getting-started)

This is a major design flaw, that the only easy default way is that you have to unplug, press bootsel, replug:
- [https://forums.raspberrypi.com/viewtopic.php?t=328795](https://forums.raspberrypi.com/viewtopic.php?t=328795)
- [https://www.reddit.com/r/raspberrypipico/comments/p9kmub/did_you_get_sick_of_unplugging_and_replugging/](https://www.reddit.com/r/raspberrypipico/comments/p9kmub/did_you_get_sick_of_unplugging_and_replugging/)
- [https://raspberrypi.stackexchange.com/questions/149006/how-to-load-binary-into-raspberry-pi-pico-only-with-cli-without-gui](https://raspberrypi.stackexchange.com/questions/149006/how-to-load-binary-into-raspberry-pi-pico-only-with-cli-without-gui)

###### picotool

↑ **Parent:** [Flash the Raspberry Pi Pico](#flash-the-raspberry-pi-pico)

[https://github.com/raspberrypi/picotool](https://github.com/raspberrypi/picotool)

Tested on [Ubuntu 25.04](systems-programming.md#ubuntu-25-04), 


```
sudo apt install libusb-1.0-0-dev
git clone https://github.com/raspberrypi/pico-sdk
git clone https://github.com/raspberrypi/picotool
cd picotool
git checkout de8ae5ac334e1126993f72a5c67949712fd1e1a4
export PICO_SDK_PATH="$(pwd)/../pico-sdk"
mkdir build
cd build
cmake ..
cmake --build . -- -j"$(npro)" VERBOSE=1
```
and the executable is there under `build/picotool` so copy it somewhere in your `PATH` like:
```
cp picotool ~/bin
```
and then trying to use a [Zephyr](systems-programming.md#zephyr-operating-system) example:
```
sudo ~/bin/picotool load -f build/zephyr/zephyr.uf2
```
fails with:
```
No accessible RP2040 devices in BOOTSEL mode were found
```
TODO: how to avoid that? [https://youtu.be/tRXLxrtfU_s?t=207](https://youtu.be/tRXLxrtfU_s?t=207) gives a workaround if you are using the Pico SDK by adding to CMakeLists.txt:
```
pico_enable_stdio_usb(blink 1)
```
but how to do it in [Zephyr](systems-programming.md#zephyr-operating-system)? Video description says:

> make sure that your program initializes the USB code via a call to "stdio\_init\_all()".

but again how to do that from [Zephyr](systems-programming.md#zephyr-operating-system)? It appears that this only works if the code currently running has support for the feature:
- [https://forums.raspberrypi.com/viewtopic.php?t=361359](https://forums.raspberrypi.com/viewtopic.php?t=361359)

<a id="video-never-unplug-your-raspberry-pi-pico-again-by-deltocode"></a>
**[Video 23](#video-never-unplug-your-raspberry-pi-pico-again-by-deltocode). Never unplug your Raspberry Pi Pico again by deltocode.** [Source](https://www.youtube.com/watch?v=tRXLxrtfU_s).

###### Run Zephyr on Raspberry Pi Pico

↑ **Parent:** [Raspberry Pi Pico](#raspberry-pi-pico)  
🏷️ **Tags:** [Run Zephyr on X](systems-programming.md#run-zephyr-on-x)

[Zephyr](systems-programming.md#zephyr-operating-system) docs: [https://docs.zephyrproject.org/latest/boards/raspberrypi/rpi_pico/doc/index.html](https://docs.zephyrproject.org/latest/boards/raspberrypi/rpi_pico/doc/index.html)

Note that the [LED blinker](software.md#led-blinker) example does not work on the [Raspberry Pi Pico W](#raspberry-pi-pico-w), see also: [Run Zephyr on Raspberry Pi Pico W](#run-zephyr-on-raspberry-pi-pico-w).

You can speed up the debug loop a little bit by plugging the Pi with BOOTSEL selected, and then running:
```
west flash --runner uf2
```
This flashes the image, and immediately turns off BOOTSEL mode and runs the program.

However to run again you need to unplug the USB and re-plug with BOOTSEL again so it is still painful.

<a id="video-let-s-run-zephyr-rtos-on-raspberry-pi-pico-ep-1-by-mr-green-s-workshop"></a>
**[Video 24](#video-let-s-run-zephyr-rtos-on-raspberry-pi-pico-ep-1-by-mr-green-s-workshop). Let's run Zephyr RTOS on Raspberry Pi Pico. Ep.1 by Mr. Green's Workshop.** [Source](https://www.youtube.com/watch?v=OyMyY4IwsJE).

###### Run Zephyr on [Raspberry Pi Pico W](#raspberry-pi-pico-w)

↑ **Parent:** [Run Zephyr on Raspberry Pi Pico](#run-zephyr-on-raspberry-pi-pico)

The Zephir [LED blinker](software.md#led-blinker) example does not work on the [Raspberry Pi Pico W](#raspberry-pi-pico-w) because the on-board LED is wired differently. But the hello world works and with:
```
screen /dev/ttyUSB0 115200
```
host shows:
```
*** Booting Zephyr OS build v4.2.0-491-g47b07e5a09ef ***
Hello World! rpi_pico/rp2040
```
Nice!

###### Raspberry Pi Pico variant

↑ **Parent:** [Raspberry Pi Pico](#raspberry-pi-pico)

###### Raspberry Pi Pico 1

↑ **Parent:** [Raspberry Pi Pico variant](#raspberry-pi-pico-variant)

This section is about the original [Raspberry Pi Pico](#raspberry-pi-pico) board. The "1" was added retroactively to the name as more boards were released and "Raspberry Pi Pico" became a generic name for the brand.

###### Raspberry Pi Pico H

↑ **Parent:** [Raspberry Pi Pico variant](#raspberry-pi-pico-variant)

Has [Serial wire debug](systems-programming.md#serial-wire-debug) debug pre-soldered. Why would you ever get one without unless you are a clueless newbie like [Ciro Santilli](ciro-santilli.md)?!?!

It is however possible to solder it yourself on [Raspberry Pi Pico W](#raspberry-pi-pico-w).

###### Raspberry Pi Pico W

↑ **Parent:** [Raspberry Pi Pico variant](#raspberry-pi-pico-variant)

Datasheet: [https://datasheets.raspberrypi.com/picow/pico-w-datasheet.pdf](https://datasheets.raspberrypi.com/picow/pico-w-datasheet.pdf)

Pinout: [https://datasheets.raspberrypi.com/picow/PicoW-A4-Pinout.pdf](https://datasheets.raspberrypi.com/picow/PicoW-A4-Pinout.pdf)

###### Raspberry Pi Pico W UART

↑ **Parent:** [Raspberry Pi Pico W](#raspberry-pi-pico-w)  
🏷️ **Tags:** [UART](computer.md#universal-asynchronous-receiver-transmitter)

You can connect form an [Ubuntu 22.04](systems-programming.md#ubuntu-22-04) host as:
```
screen /dev/ttyACM0 115200
```
When in `screen`, you can Ctrl + C to kill `main.py`, and then execution stops and you are left in a Python shell. From there:
- Ctrl + D: reboots
- Ctrl + A K: kills the [GNU screen](software.md#gnu-screen) window. Execution continues normally
but be aware of: [Raspberry Pi Pico W freezes a few seconds after after screen disconnects from UART](#raspberry-pi-pico-w-freezes-a-few-seconds-after-after-screen-disconnects-from-uart).

Other options:
- [ampy](#ampy) `run` command, which solves [How to run a MicroPython script from a file on the Raspberry Pi Pico W from the command line?](#how-to-run-a-micropython-script-from-a-file-on-the-raspberry-pi-pico-w-from-the-command-line)

###### Program Raspberry Pi Pico W with X

↑ **Parent:** [Raspberry Pi Pico W](#raspberry-pi-pico-w)

###### Program Raspberry Pi Pico W with MicroPython

↑ **Parent:** [Program Raspberry Pi Pico W with X](#program-raspberry-pi-pico-w-with-x)  
🏷️ **Tags:** [MicroPython](systems-programming.md#micropython)

Install firmware: [https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/3](https://projects.raspberrypi.org/en/projects/getting-started-with-the-pico/3)

Then there are two appraoches:
- thonny if you like clicking mouse buttons:
  ```
  pipx install thonny
  ```

  and select the interpreter as the Pico.
- [ampy](#ampy) if you like things to just run from the CLI: [How to run a MicroPython script from a file on the Raspberry Pi Pico W from the command line?](#how-to-run-a-micropython-script-from-a-file-on-the-raspberry-pi-pico-w-from-the-command-line)

###### How to run a MicroPython script from a file on the Raspberry Pi Pico W from the command line?

↑ **Parent:** [Program Raspberry Pi Pico W with MicroPython](#program-raspberry-pi-pico-w-with-micropython)

The first/only way Ciro could find was with [ampy](#ampy): [https://stackoverflow.com/questions/74150782/how-to-run-a-micropython-host-script-file-on-the-raspbery-pi-pico-from-the-host/74150783#74150783](https://stackoverflow.com/questions/74150782/how-to-run-a-micropython-host-script-file-on-the-raspbery-pi-pico-from-the-host/74150783#74150783) That just worked and it worked perfectly!
```
pipx install adafruit-ampy
ampy --port /dev/ttyACM0 run blink.py
```

TODO: possible with [rshell](#rshell)?

###### MicroPython connection tool

↑ **Parent:** [Program Raspberry Pi Pico W with MicroPython](#program-raspberry-pi-pico-w-with-micropython)

###### ampy

↑ **Parent:** [MicroPython connection tool](#micropython-connection-tool)

Source: [https://github.com/scientifichackers/ampy](https://github.com/scientifichackers/ampy)

Install on [Ubuntu 22.04](systems-programming.md#ubuntu-22-04):
```
python3 -m pip install --user adafruit-ampy
```

Bibliography:
- [https://www.digikey.co.uk/en/maker/projects/micropython-basics-load-files-run-code/fb1fcedaf11e4547943abfdd8ad825ce](https://www.digikey.co.uk/en/maker/projects/micropython-basics-load-files-run-code/fb1fcedaf11e4547943abfdd8ad825ce)

###### rshell

↑ **Parent:** [MicroPython connection tool](#micropython-connection-tool)

[https://github.com/dhylands/rshell](https://github.com/dhylands/rshell)

###### How to exit from repl in rshell?

↑ **Parent:** [Rshell](#rshell)

Ctrl + X. Documented by running `help repl` from the main shell.

###### Raspberry Pi Pico W freezes a few seconds after after screen disconnects from UART

↑ **Parent:** [Program Raspberry Pi Pico W with MicroPython](#program-raspberry-pi-pico-w-with-micropython)

- [https://stackoverflow.com/questions/74081960/raspberry-pico-w-micropython-execution-freezes-a-few-seconds-after-disconnecting](https://stackoverflow.com/questions/74081960/raspberry-pico-w-micropython-execution-freezes-a-few-seconds-after-disconnecting)
- [https://github.com/orgs/micropython/discussions/9633](https://github.com/orgs/micropython/discussions/9633)

###### Program Raspberry Pi Pico W with MicroPython code from the command line

↑ **Parent:** [Program Raspberry Pi Pico W with MicroPython](#program-raspberry-pi-pico-w-with-micropython)

[https://stackoverflow.com/questions/66183596/how-can-you-make-a-micropython-program-on-a-raspberry-pi-pico-autorun/74078142#74078142](https://stackoverflow.com/questions/66183596/how-can-you-make-a-micropython-program-on-a-raspberry-pi-pico-autorun/74078142#74078142)

Examples at: [Raspberry Pi Pico W MicroPython example](#raspberry-pi-pico-w-micropython-example).

###### Program the Raspberry Pi Pico W with MicroPython from Thonny

↑ **Parent:** [Program Raspberry Pi Pico W with MicroPython](#program-raspberry-pi-pico-w-with-micropython)

[https://stackoverflow.com/questions/66183596/how-can-you-make-a-micropython-program-on-a-raspberry-pi-pico-autorun/74078142#74078142](https://stackoverflow.com/questions/66183596/how-can-you-make-a-micropython-program-on-a-raspberry-pi-pico-autorun/74078142#74078142)

Examples at: [Raspberry Pi Pico W MicroPython example](#raspberry-pi-pico-w-micropython-example).

###### Raspberry Pi Pico W MicroPython example

↑ **Parent:** [Program Raspberry Pi Pico W with MicroPython](#program-raspberry-pi-pico-w-with-micropython)

An upstream repo at: [https://github.com/raspberrypi/pico-micropython-examples](https://github.com/raspberrypi/pico-micropython-examples)

Some generic Micropython examples most of which work on this board can be found at: [Section "MicroPython example"](systems-programming.md#micropython-example).

Pico W specific examples are under: [rpi-pico-w/upython](rpi-pico-w/upython).

The examples can be run as described at [Program Raspberry Pi Pico W with MicroPython](#program-raspberry-pi-pico-w-with-micropython).

- [rpi-pico-w/upython/led_on.py](rpi-pico-w/upython/led_on.py): turn on-board LED on and leave it on forever. Useful to quickly check that you are still able to update the firmware.
- [rpi-pico-w/upython/led_off.py](rpi-pico-w/upython/led_off.py): turn on-board LED off and leave it off forever
- [rpi-pico-w/upython/pwm.py](rpi-pico-w/upython/pwm.py): [pulse width modulation](electronics.md#pulse-width-modulation). Using the same circuit as the [rpi-pico-w/upython/blink_gpio.py](#_file/rpi-pico-w/upython/blink_gpio.py), you will now see the external LED go from dark to bright continuously  and then back

<h6 id="_file/rpi-pico-w/upython/blink.py">rpi-pico-w/upython/blink.py</h6>

↑ **Parent:** [Raspberry Pi Pico W MicroPython example](#raspberry-pi-pico-w-micropython-example)  
🏷️ **Tags:** [LED blinker](software.md#led-blinker)

Blink on-board [LED](electronics.md#light-emitting-diode). Note that they broke the LED hello world compatibility from non-W to W for God's sake!!!

The [MicroPython](systems-programming.md#micropython) code needs to be changed from the [Raspberry Pi Pico 1](#raspberry-pi-pico-1), [https://forums.raspberrypi.com/viewtopic.php?p=2016234#p2016234](https://forums.raspberrypi.com/viewtopic.php?p=2016234#p2016234) comments:

> Unlike the original Raspberry Pi Pico, the on-board LED on Pico W is not connected to a pin on RP2040, but instead to a GPIO pin on the wireless chip. 

<h6 id="_file/rpi-pico-w/upython/blink_gpio.py">rpi-pico-w/upython/blink_gpio.py</h6>

↑ **Parent:** [Raspberry Pi Pico W MicroPython example](#raspberry-pi-pico-w-micropython-example)  
🏷️ **Tags:** [LED blinker](software.md#led-blinker)

Same as the more generic [micropython/blink\_gpio.py](systems-programming.md#_file/micropython/blink_gpio.py) but with the onboard LED added.

<h6 id="_file/rpi-pico-w/upython/uart.py">rpi-pico-w/upython/uart.py</h6>

↑ **Parent:** [Raspberry Pi Pico W MicroPython example](#raspberry-pi-pico-w-micropython-example)  
🏷️ **Tags:** [LED blinker](software.md#led-blinker)

Any `print()` command ends up on the USB, and is shown on the computer via programs such as [ampy](#ampy) get back.

However, you can also send data over actual UART.

We managed to get it working based on: [https://timhanewich.medium.com/using-uart-between-a-raspberry-pi-pico-and-raspberry-pi-3b-raspbian-71095d1b259f](https://timhanewich.medium.com/using-uart-between-a-raspberry-pi-pico-and-raspberry-pi-3b-raspbian-71095d1b259f) with the help of a [DSD TECH USB to TTL Serial Converter CP2102](ciro-santilli-s-hardware.md#dsd-tech-usb-to-ttl-serial-converter-cp2102) just as shown at: [https://stackoverflow.com/questions/16040128/hook-up-raspberry-pi-via-ethernet-to-laptop-without-router/39086537#39086537](https://stackoverflow.com/questions/16040128/hook-up-raspberry-pi-via-ethernet-to-laptop-without-router/39086537#39086537) for the RPI.

We connect Pin 0 (TX), Pin 1 (RX) and Pin 2 (GND) to the DSD TECH, and the USB to the [Ubuntu 25.04](systems-programming.md#ubuntu-25-04) host laptop.

Then on the host laptop I run:
```
screen /dev/ttyUSB0 9600
```
and a counter shows up there just fine!

<h6 id="_file/rpi-pico-w/upython/adc.py">rpi-pico-w/upython/adc.py</h6>

↑ **Parent:** [Raspberry Pi Pico W MicroPython example](#raspberry-pi-pico-w-micropython-example)  
🏷️ **Tags:** [LED blinker](software.md#led-blinker)

[rpi-pico-w/upython/adc.py](rpi-pico-w/upython/adc.py): [analog-to-digital converter](electronics.md#analog-to-digital-converter).

The program continuously prints to the USB the value of the ADC on GPIO 26 once every 0.2 seconds.

The onboard LED is blinked as a [heartbeat](electronics.md#heartbeat-computing).

The hello world is with a [potentiometer](electronics.md#potentiometer): extremes on GND and VCC pins of the Pi, and middle output on pin GIO26, then as you turn the knob, the uart value goes from about 0 to about 64k.

The 0 side is quite noisy and varies between 0 and 300 for some reason.

In [Ciro's ASCII art circuit diagram notation](electronics.md#ciro-s-ascii-art-circuit-diagram-notation):
```
RPI_PICO_W__gnd__gpio26Adc__3.3V@36
            |    |          |
            |    |          |
            |  +-+          |
            |  |            |
            |  |  +---------+ 
            |  |  |
         P__1__2__3
```

<h6 id="_file/rpi-pico-w/upython/thermistor_fan_control.py">rpi-pico-w/upython/thermistor_fan_control.py</h6>

↑ **Parent:** [Raspberry Pi Pico W MicroPython example](#raspberry-pi-pico-w-micropython-example)  
🏷️ **Tags:** [LED blinker](software.md#led-blinker)

This example attempts to keep temperature to a fixed point by turning on a fan when a [thermistor](electronics.md#thermistor) gets too hot.

You can test it easily if you are not in a place that is too hot by holding the [thermistor](electronics.md#thermistor) with your finger to turn on the fan.

You can use a simple [LED](electronics.md#light-emitting-diode) to represent the fan if you don't have one handy.

In [Ciro's ASCII art circuit diagram notation](electronics.md#ciro-s-ascii-art-circuit-diagram-notation):
```
            +----------FAN-----------+
            |                        |
            |                        |
RPI_PICO_W__gnd__gpio26Adc__3.3V@36__gpio2
            |    |          |
            |    |          |
            |    |          |
            |    +-THERMISTOR
            |    |
            |    |
            R_10-+
```

###### Program Raspberry Pi Pico W with C

↑ **Parent:** [Program Raspberry Pi Pico W with X](#program-raspberry-pi-pico-w-with-x)  
🏷️ **Tags:** [MicroPython](systems-programming.md#micropython)

- [https://www.raspberrypi.com/documentation/microcontrollers/c_sdk.html](https://www.raspberrypi.com/documentation/microcontrollers/c_sdk.html)
- [https://github.com/raspberrypi/pico-sdk](https://github.com/raspberrypi/pico-sdk)
- [https://github.com/raspberrypi/pico-examples](https://github.com/raspberrypi/pico-examples) The key hello world examples are:
  - [https://github.com/raspberrypi/pico-examples/tree/a7ad17156bf60842ee55c8f86cd39e9cd7427c1d/hello_world/usb](https://github.com/raspberrypi/pico-examples/tree/a7ad17156bf60842ee55c8f86cd39e9cd7427c1d/hello_world/usb)
  - [https://github.com/raspberrypi/pico-examples/tree/a7ad17156bf60842ee55c8f86cd39e9cd7427c1d/blink](https://github.com/raspberrypi/pico-examples/tree/a7ad17156bf60842ee55c8f86cd39e9cd7427c1d/blink)

[Ubuntu 22.04](systems-programming.md#ubuntu-22-04) build just worked, nice! Much feels much cleaner than the [Micro Bit](electronics.md#micro-bit) C setup:
```
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi libstdc++-arm-none-eabi-newlib

git clone https://github.com/raspberrypi/pico-sdk
cd pico-sdk
git checkout 2e6142b15b8a75c1227dd3edbe839193b2bf9041
cd ..

git clone https://github.com/raspberrypi/pico-examples
cd pico-examples
git checkout a7ad17156bf60842ee55c8f86cd39e9cd7427c1d
cd ..

export PICO_SDK_PATH="$(pwd)/pico-sdk"
cd pico-exampes
mkdir build
cd build
# Board selection.
# https://www.raspberrypi.com/documentation/microcontrollers/c_sdk.html also says you can give wifi ID and password here for W.
cmake -DPICO_BOARD=pico_w ..
make -j
```

Then we install the programs just like any other [UF2](computer.md#uf2) but plugging it in with BOOTSEL pressed and copying the UF2 over, e.g.:
```
cp pico_w/blink/picow_blink.uf2 /media/$USER/RPI-RP2/
```
Note that there is a separate example for the W and non W LED, for non-W it is:
```
cp blink/blink.uf2 /media/$USER/RPI-RP2/
```

Also tested the UART over USB example:
```
cp hello_world/usb/hello_usb.uf2 /media/$USER/RPI-RP2/
```
You can then see the UART messages with:
```
screen /dev/ttyACM0 115200
```

TODO understand the proper debug setup, and a flash setup that doesn't require us to plug out and replug the thing every two seconds. [https://www.electronicshub.org/programming-raspberry-pi-pico-with-swd/](https://www.electronicshub.org/programming-raspberry-pi-pico-with-swd/) appears to describe it, with SWD to do both debug and flash. To do it, you seem need another board with [GPIO](electronics.md#general-purpose-input-output), e.g. a [Raspberry Pi](#raspberry-pi), the laptop alone is not enough.

## Semiconductor industry

↑ **Parent:** [Computer hardware](computer-hardware.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Semiconductor_industry)

### Semiconductor industry bibliography

↑ **Parent:** [Semiconductor industry](#semiconductor-industry)

#### Crystal Fire: The Birth of the Information Age

↑ **Parent:** [Semiconductor industry bibliography](#semiconductor-industry-bibliography)  
🏷️ **Tags:** [Good book](literature.md#good-book)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Crystal_Fire:_The_Birth_of_the_Information_Age)

### Film about the semiconductor industry

↑ **Parent:** [Semiconductor industry](#semiconductor-industry)  
🏷️ **Tags:** [Business film](film.md#business-film)

#### Halt and Catch Fire (TV series)

↑ **Parent:** [Film about the semiconductor industry](#film-about-the-semiconductor-industry)  
🏷️ **Tags:** [Business film](film.md#business-film)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Halt_and_Catch_Fire_(TV_series))

Season 1 was amazing. The others fell off a bit.

### Semiconductor company

↑ **Parent:** [Semiconductor industry](#semiconductor-industry)  
🏷️ **Tags:** [Company](company.md)

This section is about companies that design [semiconductors](condensed-matter-physics.md#semiconductor).

For companies that manufature semiconductors, see also: [company with a semiconductor fabrication plant](#company-with-a-semiconductor-fabrication-plant).

#### Acorn Computers

↑ **Parent:** [Semiconductor company](#semiconductor-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Acorn_Computers)

#### AMD

↑ **Parent:** [Semiconductor company](#semiconductor-company)  
🏷️ **Tags:** [American company](company.md#american-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AMD)

<a id="video-how-amd-went-from-nearly-bankrupt-to-booming-by-brandon-yen-2021"></a>
**[Video 25](#video-how-amd-went-from-nearly-bankrupt-to-booming-by-brandon-yen-2021). How AMD went from nearly Bankrupt to Booming by Brandon Yen (2021)** [Source](https://www.youtube.com/watch?v=Rtb4mjIACTY). - [https://youtu.be/Rtb4mjIACTY?t=118](https://youtu.be/Rtb4mjIACTY?t=118) Buldozer series CPUs was a disaster
- [https://youtu.be/Rtb4mjIACTY?t=324](https://youtu.be/Rtb4mjIACTY?t=324) got sued for marketing claims on number of cores vs number of [hyperthreads](computer.md#simultaneous-multithreading)
- [https://youtu.be/Rtb4mjIACTY?t=556](https://youtu.be/Rtb4mjIACTY?t=556) Ryzen first gen was rushed and a bit buggy, but it had potential. Gen 2 fixed those.
- [https://youtu.be/Rtb4mjIACTY?t=757](https://youtu.be/Rtb4mjIACTY?t=757) Ryzen Gen 3 surpased single thread performance of Intel. Previously Gen 2 had won multicore.

---

##### AMD product

↑ **Parent:** [AMD](#amd)

###### AMD CPU

↑ **Parent:** [AMD product](#amd-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AMD_CPU)

They have been masters of second sourcing things for a long time! One can ony imagine the complexity of the [Intel](#intel) cross licensing deals.

###### Ryzen

↑ **Parent:** [AMD CPU](#amd-cpu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Ryzen)

This was the CPU architecure that saved AMD in the 2010's, see also: [Video 25. "How AMD went from nearly Bankrupt to Booming by Brandon Yen (2021)"](#video-how-amd-went-from-nearly-bankrupt-to-booming-by-brandon-yen-2021)

###### Ryzen 7

↑ **Parent:** [Ryzen](#ryzen)

[https://en.wikichip.org/wiki/amd/ryzen_7](https://en.wikichip.org/wiki/amd/ryzen_7)

###### Ryzen 7 microarchitecture

↑ **Parent:** [Ryzen 7](#ryzen-7)

Each microarchitecture appears to fully specify all core parameters, it feels likely that they just reuse most of all of the RTL, or even pre-synthesize core blobs.

###### Zen 4

↑ **Parent:** [Ryzen 7 microarchitecture](#ryzen-7-microarchitecture)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Zen_4)

[https://en.wikichip.org/wiki/amd/microarchitectures/zen_4](https://en.wikichip.org/wiki/amd/microarchitectures/zen_4)

###### AMD 7840U

↑ **Parent:** [Zen 4](#zen-4)

Official page: [https://www.amd.com/en/products/processors/laptop/ryzen/7000-series/amd-ryzen-7-7840u.html](https://www.amd.com/en/products/processors/laptop/ryzen/7000-series/amd-ryzen-7-7840u.html)

###### Epyc

↑ **Parent:** [AMD CPU](#amd-cpu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Epyc)

###### AMD GPU

↑ **Parent:** [AMD product](#amd-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AMD_GPU)

###### AMD GPU driver

↑ **Parent:** [AMD GPU](#amd-gpu)

###### AMDGPU

↑ **Parent:** [AMD GPU driver](#amd-gpu-driver)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AMDgpu_(Linux_kernel_module))

Bibliography:
- [https://wiki.archlinux.org/title/AMDGPU](https://wiki.archlinux.org/title/AMDGPU)
- [https://gitlab.freedesktop.org/drm/amd](https://gitlab.freedesktop.org/drm/amd) an issue tracker
- [https://github.com/ROCm/ROCK-Kernel-Driver](https://github.com/ROCm/ROCK-Kernel-Driver) TODO vs the GitLab?

###### RDNA

↑ **Parent:** [AMD GPU](#amd-gpu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/RDNA_(microarchitecture))

###### RDNA 3

↑ **Parent:** [RDNA](#rdna)

###### gfx1103

↑ **Parent:** [RDNA 3](#rdna-3)

Mentioned e.g. at: [https://videocardz.com/newz/amd-begins-rdna3-gfx11-graphics-architecture-enablement-for-llvm-project](https://videocardz.com/newz/amd-begins-rdna3-gfx11-graphics-architecture-enablement-for-llvm-project) as being part of [RDNA 3](#rdna-3).

###### Radeon

↑ **Parent:** [AMD GPU](#amd-gpu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Radeon)

###### AMD Instinct

↑ **Parent:** [AMD GPU](#amd-gpu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AMD_Instinct)

###### ATI Technologies

↑ **Parent:** [AMD GPU](#amd-gpu)  
🏷️ **Tags:** [Canadian company](company.md#canadian-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ATI_Technologies)

##### AMD employee

↑ **Parent:** [AMD](#amd)  
🏷️ **Tags:** [Employee](law.md#employment)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/AMD_employee)

###### Jerry Sanders

↑ **Parent:** [AMD employee](#amd-employee)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Jerry_Sanders_(businessman))

<a id="video-amd-founder-jerry-sanders-interview-2002"></a>
**[Video 26](#video-amd-founder-jerry-sanders-interview-2002). AMD Founder Jerry Sanders Interview (2002)** [Source](https://www.youtube.com/watch?v=HqWWoaA8pIs). Source: [https://exhibits.stanford.edu/silicongenesis/catalog/hr396zc0393](https://exhibits.stanford.edu/silicongenesis/catalog/hr396zc0393). Fun to watch.
- [https://youtu.be/HqWWoaA8pIs?t=779](https://youtu.be/HqWWoaA8pIs?t=779) [Newton Minow](https://en.wikipedia.org/wiki/Newton_N._Minow) mandated [UHF](photon.md#ultra-high-frequency) on all television sets in 1961, and the [oscillator](electronics.md#electronic-oscillator) needed for the tuner was one of the first major non-military products from [Fairchild](#fairchild-semiconductor), the 28918 (?).
- [https://youtu.be/HqWWoaA8pIs?t=1053](https://youtu.be/HqWWoaA8pIs?t=1053) Fairchild had won the first round of a [Minuteman](nuclear-weapon.md#lgm-30-minuteman) contract, but lost the second one due to poor management

---

###### Lisa Su

↑ **Parent:** [AMD employee](#amd-employee)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Lisa_Su)

#### Arm (company)

↑ **Parent:** [Semiconductor company](#semiconductor-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Arm_(company))

<a id="video-arm-30-years-on-episode-one-by-arm-ltd-2022"></a>
**[Video 27](#video-arm-30-years-on-episode-one-by-arm-ltd-2022). Arm 30 Years On: Episode One by Arm Ltd. (2022)** [Source](https://www.youtube.com/watch?v=FCmnWTlDK6M).

<a id="video-arm-30-years-on-episode-two-by-arm-ltd-2022"></a>
**[Video 28](#video-arm-30-years-on-episode-two-by-arm-ltd-2022). Arm 30 Years On: Episode Two by Arm Ltd. (2022)** [Source](https://www.youtube.com/watch?v=w_CiSKUFvcg).

<a id="video-arm-30-years-on-episode-three-by-arm-ltd-2022"></a>
**[Video 29](#video-arm-30-years-on-episode-three-by-arm-ltd-2022). Arm 30 Years On: Episode Three by Arm Ltd. (2022)** [Source](https://www.youtube.com/watch?v=QmHpoi4BVwM). This one is boring US expansion. Other two are worth it.

##### Allen Wu

↑ **Parent:** [Arm (company)](#arm-company)

[https://www.linkedin.com/in/allenxwu](https://www.linkedin.com/in/allenxwu)

This situation is the most bizarre thing ever. The dude was fired in 2020, but he refused to be fired, and because he has the company seal, they can't fire him. He is still going to the office as of 2022. It makes one wonder what are the true political causes for this situation. A big warning sign to all companies tring to setup joint ventures in [China](china.md)!

- 2022 [https://www.reuters.com/technology/arm-china-says-its-ousted-ceo-wu-is-refusing-pack-up-2022-05-05/](https://www.reuters.com/technology/arm-china-says-its-ousted-ceo-wu-is-refusing-pack-up-2022-05-05/)

<a id="video-arm-fired-arm-china’s-ceo-but-he-won’t-go-by-asianometry-2021"></a>
**[Video 30](#video-arm-fired-arm-china’s-ceo-but-he-won’t-go-by-asianometry-2021). ARM Fired ARM China’s CEO But He Won’t Go by Asianometry (2021)** [Source](https://www.youtube.com/watch?v=uLzjZoS-jCs).

##### Arm product

↑ **Parent:** [Arm (company)](#arm-company)

###### Arm Artisan

↑ **Parent:** [Arm product](#arm-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Arm_Artisan)

###### ARM CPU

↑ **Parent:** [Arm product](#arm-product)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ARM_CPU)

###### ARM Cortex-M

↑ **Parent:** [ARM CPU](#arm-cpu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ARM_Cortex-M)

<h6 id="arm-cortex-m0-plus">ARM Cortex-M0+</h6>

↑ **Parent:** [ARM Cortex-M](#arm-cortex-m)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/ARM_Cortex-M0+)

#### Broadcom

↑ **Parent:** [Semiconductor company](#semiconductor-company)  
🏷️ **Tags:** [HP spinoff](electronics.md#hp-spinoff)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Broadcom)

#### Cerebras

↑ **Parent:** [Semiconductor company](#semiconductor-company)  
🏷️ **Tags:** [Fabless semiconductor company](#fabless-semiconductor-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Cerebras)

For some reason they attempt to make a single chip on an entire [wafer](#wafer-electronics)!

They didn't care about [MLperf](machine-learning.md#mlperf) as of 2019: [https://www.zdnet.com/article/cerebras-did-not-spend-one-minute-working-on-mlperf-says-ceo/](https://www.zdnet.com/article/cerebras-did-not-spend-one-minute-working-on-mlperf-says-ceo/)

- 2023: [https://www.eetimes.com/cerebras-sells-100-million-ai-supercomputer-plans-8-more/](https://www.eetimes.com/cerebras-sells-100-million-ai-supercomputer-plans-8-more/) Cerebras Sells $100 Million AI Supercomputer, Plans Eight More

![](https://web.archive.org/web/20230613000748if_/https://www.cerebras.net/wp-content/uploads/2022/03/Chip-comparison-01-uai-1032x1032.jpg)

**[Figure 10](#_839)** [Source](https://www.cerebras.net/product-chip/).

<a id="video-cerebras-architecture-deep-dive-by-sean-lie"></a>
**[Video 31](#video-cerebras-architecture-deep-dive-by-sean-lie). Cerebras Architecture Deep Dive by Sean Lie.** [Source](https://www.youtube.com/watch?v=8i1_Ru5siXc). 2022.

#### Graphcore

↑ **Parent:** [Semiconductor company](#semiconductor-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Graphcore)

#### Intel

↑ **Parent:** [Semiconductor company](#semiconductor-company)  
🏷️ **Tags:** [Company with a semiconductor fabrication plant](#company-with-a-semiconductor-fabrication-plant)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Intel)

##### Intel employee

↑ **Parent:** [Intel](#intel)

###### Intel employee grade

↑ **Parent:** [Intel employee](#intel-employee)

###### Intel fellow

↑ **Parent:** [Intel employee grade](#intel-employee-grade)

##### Intel hardware

↑ **Parent:** [Intel](#intel)

###### Intel CPU

↑ **Parent:** [Intel hardware](#intel-hardware)

###### Intel i7-7820HQ

↑ **Parent:** [Intel CPU](#intel-cpu)

Official page: [https://www.intel.com/content/www/us/en/products/sku/97496/intel-core-i77820hq-processor-8m-cache-up-to-3-90-ghz/specifications.html](https://www.intel.com/content/www/us/en/products/sku/97496/intel-core-i77820hq-processor-8m-cache-up-to-3-90-ghz/specifications.html)

###### Intel GPU

↑ **Parent:** [Intel hardware](#intel-hardware)

###### Intel discrete GPU

↑ **Parent:** [Intel GPU](#intel-gpu)

###### Intel Xe

↑ **Parent:** [Intel discrete GPU](#intel-discrete-gpu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Intel_Xe)

###### Intel Arc

↑ **Parent:** [Intel discrete GPU](#intel-discrete-gpu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Intel_Arc)

<a id="video-worst-we-ve-tested-broken-intel-arc-gpu-drivers-by-gamers-nexus-2022"></a>
**[Video 32](#video-worst-we-ve-tested-broken-intel-arc-gpu-drivers-by-gamers-nexus-2022). Worst We've Tested: Broken Intel Arc GPU Drivers by Gamers Nexus (2022)** [Source](https://www.youtube.com/watch?v=MjYSeT-T5uk).

###### Intel Graphics Technology

↑ **Parent:** [Intel GPU](#intel-gpu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Intel_Graphics_Technology)

##### Intel department

↑ **Parent:** [Intel](#intel)

###### Intel Research

↑ **Parent:** [Intel department](#intel-department)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Intel_Research_Lablets)

"Intel Research Lablets", that's a terrible name.

#### Nvidia

↑ **Parent:** [Semiconductor company](#semiconductor-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nvidia)

Open source [driver](systems-programming.md#driver-software)/hardware interface specification??? E.g. on [Ubuntu](systems-programming.md#ubuntu), a large part of the nastiest UI breaking bugs [Ciro Santilli](ciro-santilli.md) encountered over the years have been GPU related. Do you think that is a coincidence??? E.g. [ubuntu 21.10 does not wake up from suspend](systems-programming.md#ubuntu-21-10-does-not-wake-up-from-suspend).

<a id="video-linus-torvalds-saying-nvidia-fuck-you-2012"></a>
**[Video 33](#video-linus-torvalds-saying-nvidia-fuck-you-2012). Linus Torvalds saying "Nvidia Fuck You" (2012)** [Source](https://www.youtube.com/watch?v=_36yNWw_07g).

<a id="video-how-nvidia-won-graphics-cards-by-asianometry-2021"></a>
**[Video 34](#video-how-nvidia-won-graphics-cards-by-asianometry-2021). How Nvidia Won Graphics Cards by Asianometry (2021)** [Source](https://www.youtube.com/watch?v=TRZqE6H-dww). - [Doom](video-game.md#doom-video-game) was the first [killer app](software.md#killer-application) of [personal computer](#personal-computer) 3D graphics! As opposed to professional rendering e.g. for [CAD](software.md#computer-aided-design) as was supported by [Silicon Graphics](#silicon-graphics)
- [https://youtu.be/TRZqE6H-dww?t=694](https://youtu.be/TRZqE6H-dww?t=694) they bet on [Direct3D](software.md#direct3d)
- [https://youtu.be/TRZqE6H-dww?t=749](https://youtu.be/TRZqE6H-dww?t=749) they wrote their own drivers. At the time, most [drivers](systems-programming.md#driver-software) were written by the [computer manufacturers](#computer-manufacturer). That's insane!

---

<a id="video-how-nvidia-won-ai-by-asianometry-2022"></a>
**[Video 35](#video-how-nvidia-won-ai-by-asianometry-2022). How Nvidia Won AI by Asianometry (2022)** [Source](https://www.youtube.com/watch?v=GuV-HyslPxk&amp;list=WL).

##### Software developed by Nvidia

↑ **Parent:** [Nvidia](#nvidia)  
🏷️ **Tags:** [Command line utility](software.md#command-line-utility)

###### nvidia-smi

↑ **Parent:** [Software developed by Nvidia](#software-developed-by-nvidia)  
🏷️ **Tags:** [Command line utility](software.md#command-line-utility)

##### Nvidia GPU

↑ **Parent:** [Nvidia](#nvidia)

The list: [https://en.wikipedia.org/wiki/List_of_Nvidia_graphics_processing_unit](https://en.wikipedia.org/wiki/List_of_Nvidia_graphics_processing_unit)

###### Nvidia GPU feature

↑ **Parent:** [Nvidia GPU](#nvidia-gpu)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nvidia_GPU_feature)

###### Nvidia tensor core

↑ **Parent:** [Nvidia GPU feature](#nvidia-gpu-feature)

Bibliography:
- [https://developer.nvidia.com/blog/programming-tensor-cores-cuda-9/](https://developer.nvidia.com/blog/programming-tensor-cores-cuda-9/)

###### Nvidia compute GPU

↑ **Parent:** [Nvidia GPU](#nvidia-gpu)  
🏷️ **Tags:** [GPGPU](#general-purpose-computing-on-graphics-processing-units)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nvidia_compute_GPU)

This section is about [Nvidia](#nvidia) GPUs that are focused on compute rather than rendering.

Until 2020 these were branded as [Nvidia Tesla](#nvidia-tesla), but then [Nvidia](#nvidia) dropped that brand due to confusion with the [Tesla Inc.](https://ourbigbook.com/go/topic/tesla-inc) the car maker.[https://wccftech.com/nvidia-drops-tesla-brand-to-avoid-confusion-with-tesla/](https://wccftech.com/nvidia-drops-tesla-brand-to-avoid-confusion-with-tesla/).

###### Nvidia Tesla

↑ **Parent:** [Nvidia compute GPU](#nvidia-compute-gpu)  
🏷️ **Tags:** [GPGPU](#general-purpose-computing-on-graphics-processing-units)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Nvidia_Tesla)

###### List of Nvidia compute GPUs

↑ **Parent:** [Nvidia compute GPU](#nvidia-compute-gpu)

###### Nvidia T4

↑ **Parent:** [List of Nvidia compute GPUs](#list-of-nvidia-compute-gpus)

Official page: [https://www.nvidia.com/en-gb/data-center/tesla-t4/](https://www.nvidia.com/en-gb/data-center/tesla-t4/)

According to [https://wccftech.com/nvidia-drops-tesla-brand-to-avoid-confusion-with-tesla/](https://wccftech.com/nvidia-drops-tesla-brand-to-avoid-confusion-with-tesla/) this was the first card that semi-dropped the "[Nvidia Tesla](#nvidia-tesla)" branding, though it is still visible in several places.

###### Nvidia A10

↑ **Parent:** [List of Nvidia compute GPUs](#list-of-nvidia-compute-gpus)

Official page: [https://www.nvidia.com/en-gb/data-center/products/a10-gpu/](https://www.nvidia.com/en-gb/data-center/products/a10-gpu/)

###### Nvidia A10G

↑ **Parent:** [Nvidia A10](#nvidia-a10)

According to [https://www.baseten.co/blog/nvidia-a10-vs-a10g-for-ml-model-inference/](https://www.baseten.co/blog/nvidia-a10-vs-a10g-for-ml-model-inference/) the [Nvidia A10G](#nvidia-a10g) is a variant of the [Nvidia A10](#nvidia-a10) created specifically for [AWS](#amazon-web-services). As such there isn't much information publicly available about it.

> the A10 prioritizes tensor compute, while the A10G has a higher CUDA core performance

#### Qualcomm

↑ **Parent:** [Semiconductor company](#semiconductor-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Qualcomm)

[Ciro Santilli](ciro-santilli.md) has always had a good impression of these people.

#### Silicon Graphics

↑ **Parent:** [Semiconductor company](#semiconductor-company)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/Silicon_Graphics)

This company is a bit like [Sun Microsystems](software.md#sun-microsystems), you can hear a note of awe in the voice of those who knew it at its peak. This was a bit before [Ciro Santilli](ciro-santilli.md)'s awakening.

Those people created [OpenGL](software.md#opengl) for [God](religion.md#god)'s sake! Venerable.

Both of them and Sun kind of died in the same way, unable to move from the [workstation](#workstation) to the [personal computer](#personal-computer) fast enough, and just got killed by the scale of competitors who did, notably [Nvidia](#nvidia) for graphics cards.

Some/all [Nintendo 64 games](video-game.md#nintendo-64-game) were developed on it, e.g. it is well known that this was the case for [Super Mario 64](video-game.md#super-mario-64).

Also they were a big [UNIX](systems-programming.md#unix) vendor, which is another kudos to the company.

<a id="video-silicon-graphics-promo-1987"></a>
**[Video 36](#video-silicon-graphics-promo-1987). Silicon Graphics Promo (1987)** [Source](https://www.youtube.com/watch?v=Oy-kE0dq1cE). Highlights that this was one of the first widely available options for professional engineers/designers to do real-time 3D rendering for their designs. Presumably before it, you had to do use scripting to CPU render and do any changes incrementally by modifying the script.

### Chinese semiconductor industry

↑ **Parent:** [Semiconductor industry](#semiconductor-industry)  
🏷️ **Tags:** [China](china.md)

<a id="video-china-s-making-x86-processors-by-asianometry-2021"></a>
**[Video 37](#video-china-s-making-x86-processors-by-asianometry-2021). China's Making x86 Processors by Asianometry (2021)** [Source](https://www.youtube.com/watch?v=zd6iZFPiCFQ).

## ↑ Ancestors (5)

1. [Computer](computer.md)
2. [Information technology](technology.md#information-technology)
3. [Area of technology](technology.md#area-of-technology)
4. [Technology](technology.md)
5. [Ciro Santilli's Homepage](README.md)

## ← Incoming links (2)

- [The best articles by Ciro Santilli](articles.md)
- [Turing Award](social-technology.md#turing-award)
