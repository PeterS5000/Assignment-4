Memory Management Simulator
===========================

Project Overview
----------------
This C program simulates a computer system with 200KB of memory using a segmentation-based memory 
management system. It follows the First-Fit strategy to allocate memory for segments and maintains 
a dynamic list of holes in memory.

Each process can have one of the following statuses:
- new         : Load into memory for the first time.
- in          : Swap the process back into memory.
- out         : Swap the process out (segments removed, table kept).
- terminated  : Remove the process completely (segment table deleted).

Features
--------
- First-Fit strategy for memory allocation
- Dynamic hole tracking using a linked list
- Segment tables maintained per process
- Proper memory deallocation and hole merging
- Output includes segment table updates, hole status, and memory content

Compilation Instructions
------------------------
To compile the program, use:

    gcc memory_management.c -o memory_management

How to Run
----------
After compiling, run the executable:

    ./memory_management

The program will simulate both:
1. The full input sequence provided in the assignment
2. A second custom input sequence of your choice

Input Scenarios
---------------
1. Given Input Sequence:
    (1, new), (2, new), (1, out), (3, new), (4, new),
    (2, out), (1, in), (3, terminated), (2, in), 
    (5, new), (6, new), (7, new), (5, out), 
    (4, terminated), (8, new)

    Segment details:
    - Process 1: (1, 5KB), (2, 10KB), (3, 3KB), (4, 2KB)
    - Process 2: (1, 15KB), (2, 10KB), (3, 5KB)
    - Process 3: (1, 5KB), (2, 5KB), (3, 5KB)
    - Process 4: (1, 4KB), (2, 4KB)
    - Process 5: (1, 15KB), (2, 10KB)
    - Process 6: (1, 3KB), (2, 6KB), (3, 0KB)
    - Process 7: (1, 5KB)
    - Process 8: (1, 5KB), (2, 9KB), (3, 5KB)

2. Custom Input Sequence:
    (10, new), (11, new), (10, out), 
    (12, new), (11, terminated), (10, in)

Output
------
- Segment table is printed after each process operation
- Custom messages for swapped out or terminated processes
- Final state of holes in memory printed after all operations

Submission Contents
-------------------
- Handwritten solution to Part A (scanned or photographed)
- Source code file: memory_management.c
- Screenshots of:
    - Given input scenario output
    - Custom input scenario output
- README.txt (this file)

Questions
---------
If you have any questions, feel free to ask!
