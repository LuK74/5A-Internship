# Diary

## Week 1
### Overview
Firstly, I have to work on AMD machines on Grid'5000 (neowise from the Lyon site) and redoing the NEST paper experience on them.
NEST paper mostly is about Intel Machines, some experiences have been run but it is interesting to study more what happens on those machines.
AMD (Zen 2) machines differs from Intel one due to the chiplet architecture, Intel machines have one L3 caches shared between all the cores whereas AMD machines have several L3 caches shared between a small set of cores. This difference might influence the scheduling of tasks. 

### Done
- Master tools (grid5000, scripts, linux kernel configuration and makefile)
- Read NEST paper : OS Scheduling with Nest: Keeping Tasks Close Together on Warm Cores (https://hal.archives-ouvertes.fr/hal-03612592/)
- Read papers and documentation about AMD Zen 2 architecture
- Run a few benchmarks from the NEST experience on the AMD machines and studied the results
- Design a personal benchmark to run specific experiences to study AMD Zen 2 features

### TODO
- Run personal benchmark and study their results
- Study and try to run with a v5.17.1 Linux Kernel (there might be some interesting AMD options)
- Find the issue about CPU power measurement and fix it
- Run dacapo bencharmk and phoronix benchmarks
