## Assignment-2: Monitor RAM in Real Time
Use free and watch to monitor memory.

free -h

watch free -h

watch -n 5 free -h

## Solution:
<img width="937" height="222" alt="image" src="https://github.com/user-attachments/assets/3d8ab782-7024-4dd9-8ca3-58beb36ba062" />

```
Tasks:

Monitor RAM for 2 minutes.
--> Monitored.

Record RAM utilization every 30 seconds.
--> Varied from 540 MB to 543 MB.

Record total, used, free, buff/cache, and available.
--> 7.4 GB, 543 MB, 6.86 GB, 210 MB, 6.96 GB respectively.

Question: Why can free memory be very low while available memory is still high?
Answer: Because Linux uses all the spare RAM for disk caching and buffers to speed up the system performance.
Free memory is the RAM which is completely empty and unused whereas the Available memory is the estimate of RAM that is ready for use by new or existing processes without triggering swap space.
```
