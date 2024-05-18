# Operating Systems - Lab Assignment 4

## Overview
This lab assignment involves implementing various disk-scheduling algorithms and comparing their performance in terms of total head movement.

## Objective
The objective is to implement the following disk-scheduling algorithms:
- FCFS (First-Come, First-Served)
- SSTF (Shortest Seek Time First)
- SCAN
- C-SCAN (Circular SCAN)
- LOOK
- C-LOOK (Circular LOOK)

The program will generate 1000 random cylinder requests and service them according to each algorithm, reporting the total head movement.

### Implementation
1. Generate 1000 random cylinder requests within the range of 0 to 4999.
2. Read the initial head position from the command line.
3. Implement each disk-scheduling algorithm to calculate the total head movement:
   - FCFS: Service requests in the order they arrive.
   - SSTF: Service the closest request next.
   - SCAN: Move towards the end of the disk, servicing requests, and then reverse direction.
   - C-SCAN: Similar to SCAN, but return to the beginning without servicing requests in between.
   - LOOK: Similar to SCAN, but only go as far as the last request in each direction.
   - C-LOOK: Similar to LOOK, but return to the first request after the last without servicing in between.
4. Calculate and print the total head movement for each algorithm.

## Conclusion
This lab provided hands-on experience with implementing and comparing different disk-scheduling algorithms. By completing these tasks, we have gained a deeper understanding of the performance trade-offs and efficiencies of various scheduling techniques used in operating systems.
