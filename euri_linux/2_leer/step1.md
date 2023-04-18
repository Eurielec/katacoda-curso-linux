Linux provides commands capable of displaying the contents of a file, creating a file or an empty file, altering the timestamp of a file, and deleting or renaming a file or directory. These commands, useful in data and file management, are what make it possible to make data available in a certain location. This section details everything related to file management.

Utilities available for viewing files:
* `cat` Prints the entire file on screen, used for short files as it does not provide vertical scrolling.
* `tac` Same as cat except that it inverts the file line by line.
* `less` Is a document viewing program, used for large files as it provides scrolling, and search functions. Note: `/` is used to search forward for a pattern and `?` is used to search backward for a pattern.
* ``tail` Prints the last 10 lines of a file, by default. You can alter the number of lines displayed with, for example, `-n3` or `-3` to display only 3 lines.
* `head` The opposite of tail, by default prints the first 10 lines.