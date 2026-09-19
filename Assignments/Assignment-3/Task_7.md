## Assignment-7: Measure Command Execution Time
- Compare "time sleep 2" and "time sleep 5" commands
- time ls
- time find /var -type f

Answer:
- What is real time?
- What is user time?
- What is sys time?

## Solution:
<img width="1170" height="687" alt="image" src="https://github.com/user-attachments/assets/93a7b40f-d47f-422a-bfbb-dd1d81882c3c" />
<img width="717" height="695" alt="image" src="https://github.com/user-attachments/assets/ae99683c-554f-45a0-a72c-e29cf182e14b" />

```
When you run a command using time in linux, you get 3 distinct metrics representing different aspects of execution performance.
1. Real Time: The total time elapsed from the moment you hit Enter to the moment the command finishes.
              It includes execution time, time spent waiting for CPU access, and time spent waiting for disk or network I/O operations.
2. User Time: The total CPU time spent strictly executing user-space code inside your application.
              It excludes any time spent inside the Linux kernel or waiting for external resources.
3. Sys Time: The total CPU time spent strictly executing kernel-space code on behalf of your application.
             This occurs when your program makes system calls such as allocating memory, reading/writing to a file, or opening network connections.
```
