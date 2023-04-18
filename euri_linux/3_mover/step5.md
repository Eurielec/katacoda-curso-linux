**Hard links and soft links**

To explain this section, let's go to another folder with `cd /root/two/books`{{ execute }}

`ln` is used to create **hard links** and (with the -s parameter) **soft links** (*soft links* or *symlinks*). These two types of links are very useful on UNIX systems.

Let's create a **hard link** to `howToText.txt` called `howToFlirt.txt`. We will do it like this:

`ln howToText.txt howToFlirt.txt`

Using `ls`{{ execute }} you can see that a second file has been created that is the same as the first. However, a closer look at both files shows that this is not quite true.

`ls -li howToText.txt howToFlirt.txt`{{ execute }}

The `-i` option of `ls` shows in the first column the inode number, which is unique for each object. This field is the same in both files, which means that there is only one object but with two filenames associated to it.

On the other hand, there are **soft links**, or symbolic links. Symbolic links are created with the -s option:

`ln -s asCommunicate.txt asExpress.txt`{{ execute }}

What is a symbolic link about?

`ls -li asCommunicate.txt asExpress.txt`{{ execute }}

We notice that `asExpress.txt` is not a normal file, as it clearly points to `asCommunicate.txt` and has different inode numbering.

Symbolic links** do not take up extra space on the filesystem (unless their name is very long). They are very useful as they can easily be modified to point to different files. An easy way to reach long paths from your home directory using a shortcut is to create a symbolic link.

Unlike hard links, **soft links** can point to files on other filesystems (or partitions). These may or may not be available at the moment, or may not even exist. In the case where a link points to a currently unavailable or non-existent file, you get a broken, dead, or orphaned link (*broken*, *orphaned*, *dead*, or *dangling link*).

Exercise - Create a symbolic link in home to go to the `/root/two/anotherDirectory` directory more quickly.

Hard links are very useful as they save disk space, but you should be cautious about using them. The main reason is that if you delete file1 or file2 from the example in the previous section, the inode pointing to the object on disk (and its corresponding filename) will be preserved, which can lead to undesirable consequences if the file is recreated with the same name.

What happens if you delete a *hard link*, do they both get deleted, what happens if you modify one, what about symbolic links, and what about the *hard link*?