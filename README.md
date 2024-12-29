# Project Overview

This project implements a Kernel Simulator for simulating OS-level process scheduling and analyzing the performance of different scheduling algorithms. The simulator supports process state transitions and logs each transition to an output file. Assignment 2 expands on the foundation from [Assignment 1](https://github.com/AliAbdollahian/Kernel-Simulator/tree/main/cpu%20scheduling%20simulator), where the basic simulation of process scheduling was implemented. In Assignment 2, we introduced and compared three different scheduling algorithms and extended the system's capabilities to manage memory effectively.

## Key Changes from Assignment 1 to Assignment 2

1. **Introduction of Multiple Scheduling Algorithms:**
   - In Assignment 1, the simulation only used a basic **First-Come-First-Serve (FCFS)** algorithm to schedule processes.
   - In Assignment 2, we implemented and compared three scheduling algorithms:
     - **FCFS:** The classic approach where the first process in the queue is executed first.
     - **Priority Scheduling:** Processes are executed based on their priority (with higher priority processes being executed first).
     - **Round Robin (RR):** Each process is given a fixed time slice, rotating between processes.

   These schedulers were tested with a variety of workloads, and key performance metrics like average turnaround time, average wait time, and throughput were measured and compared.

2. **Memory Management Simulations:**
   - Assignment 1 did not include memory management.
   - Assignment 2 added simulations involving different **memory partition configurations**, exploring how memory size and allocation impact process execution.
   - We used the **FCFS** algorithm to allocate processes to memory partitions, analyzing the effects of partition size on memory usage, internal fragmentation, and system performance.

3. **Performance Metrics:**
   - New metrics were introduced in Assignment 2 to assess the performance of the schedulers and memory management system:
     - **Average turnaround time** and **wait time** for processes.
     - **Throughput** of the system, measured by the number of processes completed per unit of time.
     - **Memory usage efficiency**, focusing on partition sizes, internal fragmentation, and the impact of partition configuration on process waiting times.

4. **Analysis and Conclusion:**
   - **Process Scheduling:** FCFS proved to be the most efficient in terms of turnaround and wait times, while Round Robin (RR) performed the worst, especially with higher I/O frequencies.
   - **Memory Management:** The impact of partition sizes on memory efficiency was explored. Smaller partitions led to internal fragmentation and longer wait times for larger processes, while larger partitions improved system throughput but required careful management.

## Conclusion

This update showcases the progress made in Assignment 2 by introducing more complex algorithms and memory management simulations, compared to the foundational work done in Assignment 1. The additional analysis of performance and memory usage offers a deeper understanding of operating system functions.

## Running the Program

1. Open Terminal and navigate to the program's directory.
2. Run the program with a CSV file:
   ```bash
   ./my_program input_test1.csv
3. Ensure the CSV file is in the same directory or provide its full path.
4. The program will create an output.csv file in the same directory.
