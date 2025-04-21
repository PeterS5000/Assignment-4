Memory Management Simulator

📋 Description

This C program simulates a segmentation-based memory management system using the first-fit strategy. It maintains a 200KB memory block and supports process creation, swapping (in/out), and termination.

🧠 Features

Segment-based memory tracking

Linked list for managing holes

First-fit allocation for each segment

Dynamic segment tables

Full trace printing for segment operations

🛠️ How to Compile

Use gcc to compile the main.c file:

gcc main.c -o memory_simulator

▶️ How to Run

Once compiled, run the executable:

./memory_simulator

The program will simulate a fixed sequence of memory operations. Each operation will:

Load new processes

Swap processes in or out

Terminate processes

You’ll see printed segment tables and a final list of holes.

📥 Sample Input (Built-in)

(1, new), (2, new), (1, out), (3, new), (4, new),
(2, out), (1, in), (3, terminated), (2, in), (5, new),
(6, new), (7, new), (5, out), (4, terminated), (8, new)

🧪 Custom Test

To add your own custom test sequence:

Modify main() to replace or add new process definitions and calls to add_process, unload_process, terminate_process, etc.

