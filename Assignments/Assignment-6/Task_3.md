## Assignment-3: Real-World Log Analysis
Create a file named `access.log` with the following content:

```text
192.168.1.10 - - [12/Sep/2026:10:15:20] "GET /index.html" 200 1200
192.168.1.20 - - [12/Sep/2026:10:16:10] "GET /login" 200 800
192.168.1.10 - - [12/Sep/2026:10:17:30] "POST /login" 401 500
192.168.1.30 - - [12/Sep/2026:10:18:40] "GET /products" 200 2400
192.168.1.20 - - [12/Sep/2026:10:19:50] "GET /admin" 403 600
192.168.1.40 - - [12/Sep/2026:10:20:15] "GET /products" 200 2200
192.168.1.10 - - [12/Sep/2026:10:21:25] "POST /login" 401 500
192.168.1.50 - - [12/Sep/2026:10:22:35] "GET /index.html" 200 1300
192.168.1.20 - - [12/Sep/2026:10:23:45] "GET /admin" 403 600
192.168.1.60 - - [12/Sep/2026:10:24:55] "GET /products" 500 300
```

Using `awk`, `cut`, `sed`, `grep` and basic Linux commands, perform the following tasks:

1. Display all IP addresses.
2. Display unique IP addresses.
3. Count requests from each IP.
4. Find the IP generating the most requests.
5. Display all HTTP status codes.
6. Count how many requests returned 200.
7. Count how many requests returned 401.
8. Count how many requests returned 403.
9. Count how many requests returned 500.
10. Display only failed requests.
11. Display all requests to /admin.
12. Find the number of /products requests.
13. Calculate the total response size.
14. Find the largest response size.
15. Find the IP addresses generating 401 responses.
16. Find IPs generating 403 responses.
17. Replace /admin with /secure-admin using sed.
18. Replace HTTP 500 with ERROR.
19. Replace HTTP 200 with SUCCESS.
20. Generate an access log report in below format.
```text
===== ACCESS LOG REPORT =====

Total Requests : 10
Successful     : 5
Unauthorized   : 2
Forbidden      : 2
Server Errors  : 1
```

## Solution:
<img width="1710" height="1041" alt="Screenshot 2026-11-03 at 11 11 58 AM" src="https://github.com/user-attachments/assets/0c3a5562-c623-48b5-80f8-cdc434d70a4e" />

<img width="1710" height="754" alt="Screenshot 2026-11-03 at 11 26 42 AM" src="https://github.com/user-attachments/assets/c221575f-345c-452a-ba54-d9c740688f26" />

<img width="1710" height="592" alt="Screenshot 2026-11-03 at 11 27 22 AM" src="https://github.com/user-attachments/assets/dcab1b06-2d4d-40ed-98e8-b361460a8e9d" />

<img width="1710" height="664" alt="Screenshot 2026-11-03 at 11 37 41 AM" src="https://github.com/user-attachments/assets/a5c74759-6ff0-4cd7-959a-66915e79f9b9" />

### Important AWK Field Reference

For this access.log format:

| Field | Meaning |
|---|---|
| $1 | IP address |
| $2 | - |
| $3 | - |
| $4 | Date and time |
| $5 | Request method |
| $6 | Requested URL |
| $7 | HTTP status code |
| $8 | Response size |

### Conclusion

In this assignment, we learned how to analyze web server access logs using basic Linux commands.

We used:
- awk for extracting fields, counting requests, and generating reports.
- grep for searching specific requests.
- sed for replacing text.
- sort for sorting IP addresses and request counts.
- cat for creating and displaying files.

These commands are useful for Linux administration, server monitoring, and basic log analysis.
