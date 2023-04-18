To list the contents of a directory, the `ls`{{ execute }} command is used, which will display the files present in the current directory.
files present in the current directory.

To list the contents of a specific path, we pass it as an argument `ls /root/two/books`{{ execute }}.

The command `ls`, has different options:
* with `ls -l`{{ execute }} we list the files showing their size, permissions and owner.
* with `ls -a`{{ execute}} List all files, including hidden files. Files starting with a "." (e.g. .bashrc, .config) are hidden files and are useful when you have files that you want to be in a certain place but don't want them to show up normally. Generally this is done to improve the readability of directory items.
* With `ls -r`{{ execute }} Lists the files in reverse order to the normal order. If nothing is specified, the order is always alphabetical. With the -t option the listing order is the date of last modification.
