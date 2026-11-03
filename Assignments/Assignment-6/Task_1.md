## Assignment-1: Hard Links & Soft Links
1. Create a file named `training.txt` containing the text "Linux Training".
2. Create a hard link called `training_hard.txt`.
3. Create a soft link called `training_soft.txt`.
4. Verify both links using `ls -li`.
5. Modify `training.txt` and check both links.
6. Delete `training.txt`
7. Check what happens to the hard link and soft link.
8. Find the inode number of the hard link.

### Questions
1. What is the difference between hard link and soft link?
2. Why does the hard link still work after deleting the original?
3. Why does the soft link become broken after deleting the original?

## Solution:
<img width="1710" height="1013" alt="Screenshot 2026-11-03 at 10 22 49 AM" src="https://github.com/user-attachments/assets/cff41c10-f822-4d04-8d30-65f09cf51170" />

### Answers
1.
| Hard Link | Soft Link |
|---|---|
| Points directly to the same inode as the original file. | Points to the pathname of the original file. |
| Shares the same inode number. | Has a different inode number. |
| Works even after deleting the original filename. | Becomes broken if the target file is deleted or moved. |
| Cannot normally be created for directories. | Can link to files and directories. |
| Cannot cross different filesystems. | Can cross different filesystems. |

2. 
A hard link points directly to the file's inode rather than its filename.

When the original file is deleted, only its directory entry is removed. The actual data remains on the disk as long as at least one hard link exists.

Therefore, `training_hard.txt` continues to work even after deleting `training.txt`

3. 
A soft link stores the pathname of the original file rather than directly accessing its inode.

When `training.txt` is deleted, the soft link still points to the pathname `training.txt`, but that file no longer exists.

Therefore, the soft link becomes a broken link.
