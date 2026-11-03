## Assignment-2: Cut
Create a file named `employees.txt` with the following data:
```
101,Chenna,DevOps,85000
102,Rahul,Testing,65000
103,Priya,Development,90000
104,Amit,DevOps,95000
105,Sneha,Support,55000
```

1. Display only employee IDs.
2. Display only employee names.
3. Display only department names.
4. Display only salaries.
5. Display name + department.
6. Display name + salary.
7. Display the first 2 fields.
8. Display the last field.
9. Display employee names and salaries separated by -.
10. Display as shown below format:
```
Chenna earns 85000
Rahul earns 65000
...
...
```
11. Print employees whose salary is greater than 80000.
12. Print employees working in DevOps.
13. Count the number of employees.
14. Calculate the total salary.
15. Calculate the average salary.

## Solution:
<img width="1710" height="1013" alt="Screenshot 2026-11-03 at 10 39 22 AM" src="https://github.com/user-attachments/assets/6cd2ec67-c72a-4bec-8e23-46de92d80e40" />

<img width="1710" height="559" alt="Screenshot 2026-11-03 at 10 45 20 AM" src="https://github.com/user-attachments/assets/4f3cac04-56d9-44a3-ae13-4a4d866ee52e" />

### Important Linux Commands Used

| Command | Purpose | Example |
|---|---|---|
| `cat` | Create and display files | `cat employees.txt` |
| `cut` | Extract specific fields from a file | `cut -d',' -f1 employees.txt` |
| `awk` | Process, filter, and manipulate file data | `awk -F',' '{print $2}' employees.txt` |
| `grep` | Search for matching text in a file | `grep "DevOps" employees.txt` |
| `wc -l` | Count the number of lines in a file | `wc -l employees.txt` |
| `-d` | Specify the delimiter in the cut command | `cut -d',' -f1 employees.txt` |
| `-f` | Specify the field number in the cut command | `cut -d',' -f2 employees.txt` |
| `-F` | Specify the field separator in awk | `awk -F',' '{print $1}' employees.txt` |
| `$0` | Represents the entire line in awk | `awk '{print $0}' employees.txt` |
| `$1` | Represents the first field in awk | `awk -F',' '{print $1}' employees.txt` |
| `$2` | Represents the second field in awk | `awk -F',' '{print $2}' employees.txt` |
| `$3` | Represents the third field in awk | `awk -F',' '{print $3}' employees.txt` |
| `$4` | Represents the fourth field in awk | `awk -F',' '{print $4}' employees.txt` |
| `$NF` | Represents the last field in awk | `awk -F',' '{print $NF}' employees.txt` |

---

### Additional Important awk Concepts

| Syntax | Purpose |
|---|---|
| `BEGIN` | Executes before processing input records |
| `END` | Executes after processing all input records |
| `sum += $4` | Adds the fourth field to the sum |
| `count++` | Increments the counter by 1 |
| `$4 > 80000` | Checks whether salary is greater than 80000 |
| `$3 == "DevOps"` | Checks whether department is DevOps |
| `print` | Displays the output |

---
