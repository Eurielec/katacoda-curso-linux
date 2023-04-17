Execute the following command:

`cat > letter`{{ execute }}

As we have seen, when the `cat` command has no parameters it copies the standard input to the standard output.

But in this case it is redirecting the standard input to the `letter` file.

Now let's repeat the command, `cat > letter`{{ execute }}

We will see that the file has been overwritten by the previous statement, and what we previously had in `letter` has disappeared.

`(date ; who) > whoandWhen`{{ execute }} redirects the output of the `date` and `who` commands to the `whoandWhen` file.

The redirection affects both commands because they are enclosed in parentheses. The output of `who` follows the output of `date`.

`(date ; who) >> whoandWhen`{{ execute }} redirects the output of the `date` and `who` commands to the `whoandWhen` file by writing after what was there. So we have two dates and two session lists.

Putting together everything we've learned about redirects:

`cat << END > input`{{ execute }}

Can you join the contents of two files into one file, just by using redirects (with the `cat` command without any parameters).