## Assignment-5: File Permissions
1. Set the permissions of `app.conf` to:
   ```
   rw-r-----
   ```

2. Set the permissions of `app.log` to:
   ```
   rw-r--r--
   ```

3. Set the permissions of `deploy.sh` to:
   ```
   rwxr-x---
   ```

4. Verify the permissions using:
   ```
   ls -l
   ```

Convert the following symbolic permissions into numeric permissions:

1. `rwxr-x---`
2. `rw-r-----`
3. `rwxrwxr-x`
4. `r--r--r--`

Convert the following numeric permissions into symbolic permissions:

1. `755`
2. `644`
3. `750`
4. `700`

## Solution:
**Step 1: Set permissions for app.conf**

```bash
chmod 640 app.conf
```

**Step 2: Set permissions for app.log**

```bash
chmod 644 app.log
```

**Step 3: Set permissions for deploy.sh**

```bash
chmod 750 deploy.sh
```

**Step 4: Verify the permissions**

```bash
ls -l
```

**Expected Output:**

```text
-rw-r-----  app.conf
-rw-r--r--  app.log
-rwxr-x---  deploy.sh
```

---

**1. rwxr-x---**

- Owner: rwx = 4 + 2 + 1 = 7
- Group: r-x = 4 + 0 + 1 = 5
- Others: --- = 0

Answer: `750`

**2. rw-r-----**

- Owner: rw- = 4 + 2 = 6
- Group: r-- = 4
- Others: --- = 0

Answer: `640`

**3. rwxrwxr-x**

- Owner: rwx = 7
- Group: rwx = 7
- Others: r-x = 5

Answer: `775`

**4. r--r--r--**

- Owner: r-- = 4
- Group: r-- = 4
- Others: r-- = 4

Answer: `444`

---

**1. 755**

- Owner: 7 = rwx
- Group: 5 = r-x
- Others: 5 = r-x

Answer: `rwxr-xr-x`

**2. 644**

- Owner: 6 = rw-
- Group: 4 = r--
- Others: 4 = r--

Answer: `rw-r--r--`

**3. 750**

- Owner: 7 = rwx
- Group: 5 = r-x
- Others: 0 = ---

Answer: `rwxr-x---`

**4. 700**

- Owner: 7 = rwx
- Group: 0 = ---
- Others: 0 = ---

Answer: `rwx------`
