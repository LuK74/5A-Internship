# Diary

## Week 4
### Overview
Fixed the issue with the new kernels (5.15,5.16,5.17), also tried several micro artificial benchmark in order to analyze AMD governor setup behaviour.

### Done
- Fixed issue with new kernels (error in configuration file)
- Update reboot kernel script in order to be able to boot with the new AMD P-State driver (Kernel 5.17 only)
- Benchmark dacapo done with Kernel 5.9 (with cpu usage), few observations needs to be investigated
  - AMD run at high frequency most of the time
  - Some benchmark run at a lower frequency with NEST (which doesn't happen on Intel machines) but they still have better performances
  - Seems like schedutil and performance give the same results (AMD specifics or error in benchmarking method ?)
- Artificial benchmark done, cpu governor setup understood
- Started writing of a recap document for each observation linked to AMD machines
- Benchmark configure (only a few) done with all new kernels, few observations needs to be investigated
  - Performance decrease since Kernel 5.16
  - No difference between amd-pstate driver and regular acpi-controller driver
- Modification on ocaml scripts done
- Artificial benchmarks upgraded and given with a few scripts
- Installation and learning of new tools "stepper" and "count_occurency"
- Presentation of Arachne paper done

### TODO
- Run dacapo benchmark with new kernels
- Study observations done last week
- Prepare phoronix benchmark for neowise machines
- Complete recap document

## Week 3
### Overview
Eurosys'22 week.

## Week 2
### Overview
After running and analyzing the first benchmarks ran with the AMD Zen 2 machines we conclude that there were some strange things in those results :
- CPU Power usage measures inaccurate
- CPU Frequency seems to be running very highly most of the time
And so I tried to investigate those issues. In the meantime I also worked on an update of NEST for the Linux Kernel 5.15, 5.16 and 5.17.

### Done
- CPU Power usage measurement fixed (script compiling those measurements needed an update for handling AMD machines results which are different from the Intel ones)
- CPU Frequency still investigated but it seems that the frequency measurement is correct (we can see that the frequency is reduced when we're running a high number of process, like expected, or at least like we can in an Intel machine)
- Update of NEST for the Linux Kernel 5.15, 5.16 and 5.17 done
- Read and analyzed the following paper for a presentation : "Arachne: Core-Aware Thread Management"
- Mastered and update of some tools (trace-cmd, dat2graph, read_csvs)
- Ran some personal benchmarks which didn't give anything special conclusion except for :
  - The frequency reduction when there is a high number of process
  - Special behaviour when setting two different cpu governors on 2 hyperthreads from the same core

### TODO
- Deploy images with the new kernels (currently, there is an issue which need to be investigated)
- Study the "special behaviour" encountered when setting two different cpu governors on 2 hyperthreads from the same core
- Prepare the presentation of the "Arachne: Core-Aware Thread Management" paper
- Rerun NEST initial benchmarks with CPU power measurement fix and modification on cpu frequency graph drawer script (reduce frequency steps)

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
