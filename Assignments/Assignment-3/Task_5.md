## Assignment-5: Process Investigation
Choose any running process, run the below commands and answer the questions that follow.
- ps -p <PID>
- ps -ef | grep <process>
- ps -T -p <PID>

## Solution:
<img width="1217" height="422" alt="image" src="https://github.com/user-attachments/assets/d9785e2b-e171-438d-a19b-afddedf1fe0f" />

```
What is the PID?
--> 3338

Who owns the process?
--> root

When was the process started?
--> 6:00 am UTC

What command started the process?
--> /usr/sbin/nginx -g daemon on; master_process on;

How many threads does it have?
--> 1

What are the thread IDs?
--> 3338

What is the difference between a process and a thread?
--> A process is an independent executing program with its own dedicated memory, while a thread is the smallest unit of execution within a process that shares memory and resources with other threads in that same process.
    We can think of process as an entire office building and threads as individual employees working inside that building.
```
