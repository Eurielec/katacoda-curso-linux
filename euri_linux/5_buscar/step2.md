The `find` tool, on the other hand, is extremely useful for finding files in a specific directory. What this statement does is to go through the directory tree starting from one or more directories indicated (or the default one).

The different ways to use this command are the following:

* `find`{{execute}} will list all the files in the current directory and its subdirectories and as an extension if we sentence `find `{execute}} it will do the same but in directory 'two'.
* `find -name xxx` will only list files with the pattern xxx in their name, we can do for example `find -name howtoCommunicate.txt`{{execute}} and we see that it lists the files that have howtoCommunicate.txt as their name. An interesting function is the use of *iname* instead of *name*, as the former is case insensitive, finding a result for `find -name howtocommunicate.txt`{{execute}} will not return a result, but `find -iname howtocommunicate.txt`{{execute}} will.
* `find -type x` is a very useful option as it allows us to filter the results by file type: `find -type d`{{execute}} will return directories, `find -type |` will return symbolic links and `find -type f` will show all current files.
* Obviously we can also do a combination of all the above instructions like: `find /two -name how* -type f`{{execute}}.