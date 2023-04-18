Now let's go to the `/root/dos/books` path where we will have different files.

`cd /root/dos/books`{{ execute }}

If we list all the files in `/root/dos/books` with `ls`{{ execute }} we will see that it contains some files and a directory.

If we list them with `ls -la`{{ execute }} we will see that we have *hidden* files.

Look at the differences between each file, what is each thing?

The characters at the beginning of each line (e.g. "drwxr-xr-r") tell us what permissions each file has (the letter "d").
(the letter "d" indicates that it is a directory). Let's analyse this part: if all
permissions were available to all users, we would have something like this:

`-rwxrwxrwx`.

The "r" character means read permission, "w" means write permission, "x" means execute permission.
"x" for execution. The first three characters indicate the permissions of the owner; the next three characters indicate the permissions of the group; the following three characters indicate the permissions of the group.
The next three, the permissions of the group; the last three, the permissions of the other users. The fifth field shows the size of the object measured in characters. The sixth, seventh and eighth fields give the date and time the file was last modified.

Some versions of ls display the last modification date in detail when prompted with the `--full-time` option.

`ls -l --full-time`{{ execute }}

**What are the directories `.` and `..`?**