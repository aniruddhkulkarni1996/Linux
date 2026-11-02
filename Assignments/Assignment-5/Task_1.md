## Assignment-1: Basic User Management
1. Create a user named `devuser1`.

2. Create three users:
   - `developer1`
   - `developer2`
   - `developer3`

3. Verify that all three users were successfully created.

4. Delete the user `developer3`.

5. Create a user named `tester1`.

6. Change the username `tester1` to `qauser1`.

7. Delete the user `qauser1`.

8. Create a user named `admin1`.

9. Verify the UID (User ID) and primary group of `admin1`.

## Solution:
## 1. Create a user named devuser1

**Command:**

```bash
sudo useradd devuser1
```

**Verify:**

```bash
id devuser1
```

---

## 2. Create three users

Create developer1:

```bash
sudo useradd developer1
```

Create developer2:

```bash
sudo useradd developer2
```

Create developer3:

```bash
sudo useradd developer3
```

---

## 3. Verify that all three users were created

**Command:**

```bash
id developer1
id developer2
id developer3
```

---

## 4. Delete developer3

**Command:**

```bash
sudo userdel developer3
```

**Verify deletion:**

```bash
id developer3
```

Expected output:

```text
id: ‘developer3’: no such user
```

---

## 5. Create a user named tester1

**Command:**

```bash
sudo useradd tester1
```

**Verify:**

```bash
id tester1
```

---

## 6. Change the username tester1 to qauser1

**Command:**

```bash
sudo usermod -l qauser1 tester1
```

**Verify username change:**

```bash
id qauser1
```

Check whether the old username exists:

```bash
id tester1
```

Expected output:

```text
id: ‘tester1’: no such user
```

---

## 7. Delete qauser1

**Command:**

```bash
sudo userdel qauser1
```

**Verify deletion:**

```bash
id qauser1
```

Expected output:

```text
id: ‘qauser1’: no such user
```

---

## 8. Create a user named admin1

**Command:**

```bash
sudo useradd admin1
```

---

## 9. Verify the UID and primary group of admin1

**Check UID:**

```bash
id -u admin1
```

**Check primary group ID:**

```bash
id -g admin1
```

**Check primary group name:**

```bash
id -gn admin1
```
