## Assignment-4: File Ownership
1. Create a directory named `project`.
2. Create three files inside the directory:
   - `project/app.conf`
   - `project/app.log`
   - `project/deploy.sh`
3. Change the owner of `app.conf` to `john`.
4. Change the owner and group of `app.log` to:
   - Owner: `alice`
   - Group: `developers`
5. Change the group ownership of `deploy.sh` to `developers`.
6. Verify the ownership and group of all three files.

## Solution:
## Step 1: Create the directory

Command:

```bash
mkdir -p project
```

Explanation:

- `mkdir` creates a directory.
- `-p` creates the directory if it does not already exist.

## Step 2: Create three files

Commands:

```bash
touch project/app.conf project/app.log project/deploy.sh
```

## Step 3: Change the owner of app.conf to john

Command:

```bash
sudo chown john project/app.conf
```

Explanation:

- `chown` changes file ownership.
- `john` is the new owner.
- `project/app.conf` is the file.

## Step 4: Change the owner and group of app.log

Command:

```bash
sudo chown alice:developers project/app.log
```

Explanation:

- `alice` is the new owner.
- `developers` is the new group.
- Both ownership and group are changed using `chown`.

## Step 5: Change the group ownership of deploy.sh

Command:

```bash
sudo chgrp developers project/deploy.sh
```

Explanation:

- `chgrp` changes the group ownership of a file.
- `developers` is the new group.

## Step 6: Verify ownership and group of all files

Command:

```bash
ls -l project
```

This displays the file permissions, owner, group, file size, and modification date.
