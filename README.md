# Internship

## Student
Lucas Chaloyard (11904079)
UGA Mail : lucas.chaloyard@etu.univ-grenoble-alpes.fr
INRIA Mail : lucas.chaloyard@inria.fr

## Subject
Understanding scheduling overheads and their performance impact in KVM
Whisper team, Inria Paris, 2 rue Simone IFF, 75102 Paris
March 21, 2022 - September 22, 2022

Today, virtualization is commonly used in production environments to support application execution.
In a virtual environment, an underlying hypervisor provides uniform access to the underlying hardware features, allowing the user to install any operating system (known as the guest operating system) that fits the needs of their application.  This approach offers safety, predictability, and flexibility. Nevertheless, it may also incur inefficiencies.
Indeed, the guest operating system may make poor decisions, because its view of the hardware and the overall system load is limited to the information provided by the hypervisor.

The goal of this internship is to examine the consequences of this gap between the guest operating and the machine in the context of process scheduling.
Building on the expertise in Linux kernel process scheduling in the Whisper team, We will design and carry out experiments to precisely understand the challenges facing the process scheduler in a virtualized environment and the impact of these challenges on application performance.
In this, we will study the behavior of a wide range of applications found in the Phoronix benchmark suite, on a wide range of multicore servers, found in both the Whisper team and the Grid 5000 platform.

The internship will be supervised by Julia Lawall (DR1, Inria-Paris), in collaboration with Himadri Pandya (PhD student, Inria-Paris) and Jean-Pierre Lozi (researcher, Oracle).

Some relevant papers:

Vo Quoc Bao Bui, Djob Mvondo, Boris Teabe, Kevin Jiokeng, Patrick Lavoisier Wapet, Alain Tchana, Gaël Thomas, Daniel Hagimont, Gilles Muller, Noel De Palma:
When eXtended Para - Virtualization (XPV) Meets NUMA. EuroSys 2019: 7:1-7:15

Li Liu, Haoliang Wang, An Wang, Mengbai Xiao, Yue Cheng, Songqing Chen:
Mind the Gap: Broken Promises of CPU Reservations in Containerized Multi-tenant Clouds. SoCC 2021: 243-257

Djob Mvondo, Antonio Barbalace, Alain Tchana, Gilles Muller:
Tell me when you are sleepy and what may wake you up! SoCC 2021: 562-569

Redha Gouicem, Damien Carver, Jean-Pierre Lozi, Julien Sopena, Baptiste Lepers, Willy Zwaenepoel, Nicolas Palix, Julia Lawall, Gilles Muller:
Fewer Cores, More Hertz: Leveraging High-Frequency Cores in the OS Scheduler for Improved Application Performance. USENIX Annual Technical Conference 2020: 435-448
