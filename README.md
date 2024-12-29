# Project Overview

This project implements a Kernel Simulator to simulate OS-level process scheduling and analyze the performance of different scheduling algorithms. The simulator supports process state transitions and logs each transition to an output file. Assignment 2 expands on [Assignment 1](https://github.com/AliAbdollahian/Kernel-Simulator/tree/main/cpu%20scheduling%20simulator), where basic process scheduling was implemented. In Assignment 2, we introduced and compared three scheduling algorithms and extended the system's memory management capabilities.

## Key Changes from [Assignment 1](https://github.com/AliAbdollahian/Kernel-Simulator/tree/main/cpu%20scheduling%20simulator) to Assignment 2

1. **Scheduling Algorithms:**
   - [Assignment 1](https://github.com/AliAbdollahian/Kernel-Simulator/tree/main/cpu%20scheduling%20simulator) used a basic **First-Come-First-Serve (FCFS)** algorithm.
   - Assignment 2 introduced and compared:
     - **FCFS:** Executes processes in the order they arrive.
     - **Priority Scheduling:** Executes based on process priority (higher priority first).
     - **Round Robin (RR):** Allocates a fixed time slice to each process in a cyclic order.

   We measured and compared performance metrics like average turnaround time, wait time, and throughput.

2. **Memory Management Simulations:**
   - [Assignment 1](https://github.com/AliAbdollahian/Kernel-Simulator/tree/main/cpu%20scheduling%20simulator) did not include memory management.
   - Assignment 2 added memory management simulations with different **memory partition configurations**, exploring how partition size affects memory usage, fragmentation, and process performance.

3. **Performance Metrics:**
   - New metrics introduced in Assignment 2:
     - **Average turnaround time** and **wait time**.
     - **Throughput**, measuring processes completed per unit time.
     - **Memory usage efficiency**, focusing on partition sizes and fragmentation.

4. **Analysis and Conclusion:**
   - **Scheduling:** FCFS was most efficient in turnaround and wait times, while Round Robin (RR) performed the worst, especially with higher I/O frequencies.
   - **Memory Management:** Smaller partitions caused fragmentation and increased wait times for larger processes, while larger partitions improved throughput but needed careful management.

## Conclusion

This update in Assignment 2 builds on the work from [Assignment 1](https://github.com/AliAbdollahian/Kernel-Simulator/tree/main/cpu%20scheduling%20simulator) by adding memory management simulations and comparing RR, Priority, and FCFS algorithms. The analysis helps understand operating system functions and their impact on performance. For detailed results and analysis, refer to the [report](https://github.com/AliAbdollahian/Kernel-Simulator/blob/main/SYSC4001-A2.pdf).

## Running the Program

1. Open Terminal and navigate to the program's directory.
2. Run the program with a CSV file:
   ```bash
   ./my_program input_test1.csv
