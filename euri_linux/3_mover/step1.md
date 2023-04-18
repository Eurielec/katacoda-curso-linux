`touch` is used to set or update the access and/or edit dates of a file. By default it resets the access and edit dates to the current date.

It is also possible to create an empty file using `touch`:

`touch myfile`{{ execute }}

This is usually done in order to create a container to be filled later.

The `touch` option provides multiple options, but here is the one of interest: The `-t` option allows you to modify the date and time the file is accessed and edited. The date format is the following [[SS]YY]MMDDhhmm[.ss]

`touch -t 05200800 myfile`{{execute}}

You can see the date of the file with `ls -la`{{ execute }}.