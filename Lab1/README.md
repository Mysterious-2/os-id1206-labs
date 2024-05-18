# Operating Systems - Lab Assignment 1

## Overview
This lab assignment consists of two parts aimed at understanding inter-process communication using pipes and message queues in a Unix-like operating system. The tasks involve creating child processes, using `fork`, `exec`, `wait`, and communicating between processes using `pipe` and `msgsnd/msgrcv` system calls.

## Part 1: Using `fork`, `exec`, `wait`, and `pipe`

### Objective
The objective is to implement a program that replicates the command `ls / | wc -l`. The program creates a child process that lists the files in the root directory and pipes this output to the parent process. The parent process then counts the number of lines.

### Implementation
1. Create a pipe for inter-process communication.
2. Use `fork` to create a child process.
3. In the child process:
   - Close the read end of the pipe.
   - Duplicate the write end of the pipe to standard output (`STDOUT_FILENO`).
   - Execute `ls /` using `execlp`.
4. In the parent process:
   - Close the write end of the pipe.
   - Duplicate the read end of the pipe to standard input (`STDIN_FILENO`).
   - Wait for the child process to finish.
   - Execute `wc -l` using `execlp`.

## Part 2: Using Message Queues

### Objective
The objective is to implement two processes where one reads the content of a file and passes it to the other through a message queue. The receiving process then counts and prints the number of words in the file content.

### Implementation
1. Create a message queue using `msgget`.
2. Use `fork` to create a child process.
3. In the parent process:
   - Receive the message from the message queue using `msgrcv`.
   - Print the received message.
   - Count and print the number of words in the message.
   - Destroy the message queue using `msgctl`.
4. In the child process:
   - Open and read the file content into a message buffer.
   - Set the message type and send the message using `msgsnd`.

## Conclusion
This lab provided hands-on experience with creating and managing processes using `fork`, executing commands using `exec`, synchronizing processes with `wait`, and communicating between processes using pipes and message queues. By completing these tasks, we have deepened our understanding of inter-process communication mechanisms in Unix-like operating systems.

