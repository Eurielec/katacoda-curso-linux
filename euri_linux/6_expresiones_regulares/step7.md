If we want to use the power of regular expressions with `ls` for example it would look like this:

`ls | egrep '^a.txt'`{{ execute }} Search for files named `a.txt`. The `^` character indicates the start of the line.
`ls | egrep '^(a)(.)\1.txt'`{ execute }} Search for files named `a` followed by a character and then `a.txt`. For example `aba.txt`.

Create some files with different names (using the `touch` command), and check the use of the regular expressions seen above.

Psss... It doesn't end there

With regular expressions we could delete files that have a pattern in their name, using pipes. To remove them would be with:

`ls | egrep '^a.txt' | xargs -d "d" rm`{{ execute }}

Check its use