## Assignment-2: Goup Management
1. Create the following groups:
   - developers
   - testers
   - admins

2. Verify that the groups were created successfully.

3. Rename the group `testers` to `qa`.

4. Delete the `admins` group.

5. Create a new group called `operations`.

## Solution:
### 1. Create the Groups

Run the following commands to create the three groups:

```bash
sudo groupadd developers
sudo groupadd testers
sudo groupadd admins
```

### 2. Verify That the Groups Were Created

Use the following command to check whether the groups exist:

```bash
getent group developers testers admins
```

**Expected Output:**

```text
developers:x:1001:
testers:x:1002:
admins:x:1003:
```

Note: Group IDs (GIDs) may differ on your system.

### 3. Rename the Group testers to qa

Use the `groupmod` command:

```bash
sudo groupmod -n qa testers
```

Verify the rename:

```bash
getent group qa
```

### 4. Delete the admins Group

Use the `groupdel` command:

```bash
sudo groupdel admins
```

Verify that the group has been deleted:

```bash
getent group admins
```

If the group was successfully deleted, this command will return no output.

### 5. Create a New Group Called operations

Use the `groupadd` command:

```bash
sudo groupadd operations
```

Verify that the group was created:

```bash
getent group operations
```
