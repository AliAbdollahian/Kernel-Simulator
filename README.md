# Kernel Simulator

This project implements a Kernel Simulator for simulating OS-level process scheduling and analyzing the performance of different scheduling algorithms. The simulator supports process state transitions and logs each transition to an output file.

## Features
- Simulates OS kernel-level process state transitions.
- Tracks states: New, Ready, Running, Waiting, and Terminated.
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

## Running the Program

1. Open Terminal and navigate to the program's directory.
2. Run the program with a CSV file:
   ```bash
   ./my_program input_test1.csv
3. Ensure the CSV file is in the same directory or provide its full path.
4. The program will create an output.csv file in the same directory.
