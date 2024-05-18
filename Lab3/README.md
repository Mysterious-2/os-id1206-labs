# Operating Systems - Lab Assignment 3

## Overview
This lab assignment involves translating logical to physical addresses using a TLB (Translation Lookaside Buffer) and a page table. The program reads logical addresses, translates them, and outputs the corresponding physical addresses and byte values.

## Objective
The objective is to read a file containing logical addresses, use a TLB and page table to translate each address to its corresponding physical address, handle page faults by reading from a backing store, and calculate the page fault rate and TLB hit rate.

### Implementation
1. Read logical addresses from `addresses.txt`.
2. Use bit-masking and bit-shifting to extract the page number and offset.
3. Check the TLB for the page number. If a TLB hit occurs, retrieve the frame number from the TLB.
4. If a TLB miss occurs, check the page table. If the page table entry is invalid, handle the page fault by reading from the backing store.
5. Update the TLB using a FIFO replacement strategy.
6. Calculate and print the physical address and byte value for each logical address.
7. Calculate and print the page fault rate and TLB hit rate.

## Conclusion
This lab provided practical experience with address translation, TLB and page table management, and handling page faults. By completing these tasks, we have enhanced our understanding of virtual memory management in operating systems.
