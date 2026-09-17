## Assignment-3: CPU Monitoring Using top
Run:

top

top -d 5

top -n 3

top -b -n 3

top -c

<img width="990" height="695" alt="image" src="https://github.com/user-attachments/assets/b9342115-d246-427e-a563-0589dd92786f" />

Answer the following questions:
```
What is the total CPU utilization?
--> 0.0

Which process is consuming the most CPU?
--> systemd (PID 1)

Which process is consuming the most memory?
--> snapd (PID 232)

What is the meaning of %us, %sy, %id, %wa?
--> %us - Time spent on user space processes (such as python scripts or java processes)
    %sy - Time spent on system / kernel processes (such as driver operations or memory management)
    %id - Time spent doing nothing while waiting for tasks to process
    %wa - Time spent while waiting for disk or network i/o operations to complete

What is the difference between top -n 3 and top -d 5?
--> top -n 3 runs the top command for 3 iterations and exits back to the terminal prompt
    top -d 5 starts the top command with 5 second update delay instead of default 3 seconds

Why would top -b be useful in scripts?
--> Using top in standard interactive mode withing a script will fail of hang because top expects an interactive terminal.
    top -b command runs the top command in batch mode specifically designed for scripts / automation.
    This disables the interactive mode and sends raw text output directly to stdout, making it useful for logging or piping to a file
    Eg: top -b -n 3 > log.txt
        top -b -n 1 | grep "Cpu(s)" | awk '{pring $2}'
```
