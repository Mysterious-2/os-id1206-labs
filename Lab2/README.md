# Operating Systems - Lab Assignment 2

## Overview
This lab assignment consists of two parts aimed at understanding multithreading with mutexes and implementing the Reader-Writer problem using shared memory and semaphores.

## Part 1: Multithreading with Mutexes

### Objective
The objective is to create three threads that increment a shared buffer. Each thread prints its thread ID, process ID, and the buffer’s current value, then increments the buffer by one. The process is protected by a mutex to ensure mutual exclusion.

### Implementation
1. Create and initialize three threads.
2. Use a mutex to protect the critical section where the buffer is incremented.
3. Each thread increments the buffer 15 times.
4. The main thread waits for all threads to finish and prints the total changes made by each thread.

## Part 2: Reader-Writer Problem

### Objective
The objective is to implement the Reader-Writer problem with two readers and one writer process. The writer updates a shared buffer, and the readers read from it. Proper synchronization is ensured using semaphores.

### Implementation
1. Initialize shared memory and semaphores.
2. Create two reader processes and one writer process.
3. The writer increments the shared variable until it reaches a maximum value, ensuring mutual exclusion using semaphores.
4. The readers read the shared variable, ensuring mutual exclusion using semaphores.
5. Proper synchronization is maintained to avoid race conditions.
6. The program terminates when the writer reaches the maximum value.

## Conclusion
This lab provided hands-on experience with multithreading, mutexes, shared memory, and semaphores. By completing these tasks, we have deepened our understanding of synchronization mechanisms and the Reader-Writer problem in Unix-like operating systems.
