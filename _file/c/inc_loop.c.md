<h1 id="_file/c/inc_loop.c">c/inc_loop.c</h1>

↑ **Parent:** [CPU microbenchmark](../../cpu-microbenchmark.md)

[Ubuntu 25.04](../../ubuntu-25-04.md) GCC 14.2 -O0 x86\_64 produces a horrendous:
```
11c8:       48 83 45 f0 01          addq   $0x1,-0x10(%rbp)
11cd:       48 8b 45 f0             mov    -0x10(%rbp),%rax
11d1:       48 3b 45 e8             cmp    -0x18(%rbp),%rax
11d5:       72 f1                   jb     11c8 <main+0x7f>
```
To do about 1s on [P14s](../../ciro-santilli-s-hardware/lenovo-thinkpad-p14s-gen4-amd.md) we need 2.5 billion instructions:
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

## ↑ Ancestors (9)

1. [CPU microbenchmark](../../cpu-microbenchmark.md)
2. [Microarchitectural benchmark](../../microarchitectural-benchmark.md)
3. [Microarchitecture](../../microarchitecture.md)
4. [Computer hardware](../../computer-hardware-split.md)
5. [Computer](../../computer-split.md)
6. [Information technology](../../information-technology.md)
7. [Area of technology](../../area-of-technology.md)
8. [Technology](../../technology-split.md)
9. [Ciro Santilli's Homepage](../../split.md)
