It is not a good idea to send any file to the screen carelessly. Some files can be sent to the screen without worrying. All their characters are printable. Other files should not be sent directly to the screen. They have non-printable characters.

If a file with non-printable characters is sent to the screen, it may happen that what you see does not correspond to the content, the screen may be left in such a way that everything that follows is unreadable, or it may be locked. None of this is irreversible, but it is quite annoying.

`cat /bin/ls`{{ execute }}

With the `file` command we can see what type of file it is without having to open it.

Now we run `file *`{{ execute }}

The shell takes the `file *` line and substitutes `*` for all items in the directory.

The file command attempts to determine the type of the objects whose names appear as parameters. Most of the time the names are file names. It starts by looking to see if the file has non-printable characters.

When the file has non-printable characters, it studies its first two or four octets. If those first octets take recognised values, `file` indicates the associated object type.