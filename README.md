# Kernel Simulator

This project implements a Kernel Simulator for simulating OS-level process scheduling and analyzing the performance of different scheduling algorithms. The simulator supports process state transitions and logs each transition to an output file. It will also serve as the foundation for further development in Assignment 2.

## Features
- Simulates OS kernel-level process state transitions.
- Tracks states: New, Ready, Running, Waiting, and Terminated.
- Handles processes with I/O events and preemption.
- Logs transitions with detailed time-stamped entries.

## Input Format
The simulator accepts a CSV file as input, containing the following fields:

| Field          | Description                                                   |
|----------------|---------------------------------------------------------------|
| `Pid`          | Unique identifier for the process                             |
| `ArrivalTime`  | Time at which the process enters the system (ms)              |
| `TotalCPUTime` | Total CPU time required (excluding I/O time)                  |
| `IOFrequency`  | Frequency of I/O requests (in ms)                             |
| `IODuration`   | Duration of each I/O operation (in ms)                        |

### Example Input (CSV Format)


## Output
The simulator generates an output log file (`output.csv`) capturing every state transition:

| Field         | Description                           |
|---------------|---------------------------------------|
| `Time`        | Simulation time (ms)                 |
| `Pid`         | Process ID                           |
| `OldState`    | State before the transition          |
| `NewState`    | State after the transition           |

### Example Output

## Project Structure
### Files
1. **`main.c`**: Entry point for the simulator.
2. **`my_structs.h`**: Defines the PCB and queue structures.
3. **`my_functions.h`**: Function prototypes for simulator operations.
4. **`my_functions.c`**: Function implementations for CSV parsing, queue operations, logging, and state transitions.

### Key Functions
- **`readCSV`**: Reads and parses the input file to initialize processes.
- **`alloc_queue`**: Allocates memory for a queue.
- **`enqueue` / `dequeue`**: Handles queue operations.
- **`logTransition`**: Logs state transitions to the output file.
- **`runSimulation`**: Core simulation logic.

## Compilation
Compile the project using GCC:
```bash
gcc -o kernel_simulator main.c my_functions.c -std=c99

./kernel_simulator <test_file.csv>
