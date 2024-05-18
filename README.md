# os-id1206-labs
This repository contains the lab assignments for the Operating Systems course (ID1206) at KTH. Each lab focuses on different core concepts of operating systems, including process management, threading, memory management, and file systems.

## Lab Assignments

### [Lab 1](Lab1)
- **Part 1:** Implement process creation and communication using `fork`, `exec`, and `pipe`.
- **Part 2:** Implement inter-process communication using message queues.

### [Lab 2](Lab2)
- **Part 1:** Implement multithreading with mutexes to control access to a shared buffer.
- **Part 2:** Solve the Reader-Writer problem using semaphores and shared memory.

### [Lab 3](Lab3)
- Implement a memory management simulator to translate logical addresses to physical addresses using a TLB and page table.

### [Lab 4](Lab4)
- **Question 1:** Implement various disk-scheduling algorithms.

## Getting Started

Each lab directory contains:
- A `src` folder with the source code files.
- A `README.md` file with specific instructions and explanations for the lab.
- The original lab assignment PDF.

## How to Run

For each lab, navigate to the respective `src` directory and compile the code using `gcc`. For example, to run the program for Lab 1 Part 1:

```sh
cd Lab1/src
gcc -o part1 part1.c
./part1
