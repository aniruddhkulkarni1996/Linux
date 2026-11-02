## Assignment-3: Add Users to Groups
1. Create the following users:
   - john
   - alice
   - bob

2. Add john and alice to the `developers` group.

3. Add bob to the `qa` group.

4. Add bob to the `developers` group without removing his existing group memberships.

5. Verify the group memberships of all three users.

6. Remove alice from the `developers` group.

7. Verify that alice is no longer a member of the `developers` group.

## Solution:
## Step 1: Create the Users

Execute the following commands to create the three users.

```bash
sudo useradd -m john
sudo useradd -m alice
sudo useradd -m bob
```

**Explanation:**
- `useradd` creates a new Linux user.
- `-m` creates a home directory for the user.

## Step 2: Create the Groups

Create the `developers` and `qa` groups.

```bash
sudo groupadd developers
sudo groupadd qa
```

**Explanation:**
- `groupadd` creates a new Linux group.

Note: If these groups already exist, you do not need to create them again.

## Step 3: Add John and Alice to the Developers Group

Execute:

```bash
sudo usermod -aG developers john
sudo usermod -aG developers alice
```

**Explanation:**
- `usermod` modifies an existing user account.
- `-a` appends the user to existing supplementary groups.
- `-G` specifies supplementary groups.
- `developers` is the group to which the users are added.

## Step 4: Add Bob to the QA Group

Execute:

```bash
sudo usermod -aG qa bob
```

**Explanation:**

This command adds bob to the `qa` group.

## Step 5: Add Bob to Developers Without Removing Existing Groups

Execute:

```bash
sudo usermod -aG developers bob
```

**Explanation:**

The `-aG` option adds bob to the developers group while preserving his existing supplementary group memberships.

**Important:** Do not use `-G` without `-a` because it can replace the user's existing supplementary group memberships.

Bob should now belong to both:
- qa
- developers

## Step 6: Verify Group Memberships of All Three Users

Execute the following commands:

```bash
id john
id alice
id bob
```

Alternatively, use:

```bash
groups john
groups alice
groups bob
```

**Expected supplementary group memberships:**

| User | Groups |
|------|--------|
| john | developers |
| alice | developers |
| bob | qa, developers |

Note: Each user also has a primary group, which may have the same name as the username.

## Step 7: Remove Alice from the Developers Group

Execute:

```bash
sudo gpasswd -d alice developers
```

**Explanation:**
- `gpasswd` manages group membership.
- `-d` removes a user from a group.
- `alice` is the user to remove.
- `developers` is the group.

This removes alice from the developers group without deleting her user account.

## Step 8: Verify Alice Is No Longer in the Developers Group

Execute:

```bash
id alice
```

Or:

```bash
groups alice
```

To check specifically whether alice belongs to developers, execute:

```bash
id -nG alice
```

The output should not contain `developers`.
