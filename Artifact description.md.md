### Hardware platform
- Intel Xeon Gold 6240 CPU of 2.60GHz;
- 252GB DDR4 memory;
- 4$times$ 128GB Optane DCPMM;

### Software
- Ubuntu 18.04 with Linux kernel 5.4.0-135-generic;
- Pacman (https://github.com/thustorage/pacman, commit 8fdf212) used as our baseline.
- We configure Optane DCPMM with full AppDirectNotInterleaved mode, create EXT4 file system with 4KB block size, and access through a DAX file system mapped to a pre-defined address space.

### The type of experiments

We mainly focus on performance, i.e., the key-value access throughput between the state-of-the-art baseline and the proposed log-structured key-value store system. We conduct detailed experiments including the overall performance comparison, the numbers of garbage collection, the amount of memory accesses. We also break down the contributions of the several proposed individual optimizations.