The `grep` command searches for a pattern in a file. It could be used with `grep FruitPurchaseList`{{ execute }}

Also, if you don't put any file into the `grep` command, it will search for the pattern by standard input. You can use the command with the following *pipe*

`cat sstv | grep MHz`{{ execute }}

And with the use of the very useful *pipe*, we can count the number of results of what we are looking for with `wc`.

`cat sstv | grep MHz | wc`{{ execute }}

There is a command to sort the contents of a file and pass it through standard input, this is `sort`. Instead `uniq -c` writes how many times each line is repeated consecutively.

Using pipes we could do the following:

`sort votes | uniq -c`{{ execute }}

Another useful way to use *pipes* is with the `history` command, which prints out the command history. If you have forgotten how you used a command in the past, you can look it up with `grep`.

`history | grep cat`{{ execute }}

If you have command output that is very large, you can redirect it to the `less` program which will display it in a more orderly fashion:

`ls -l | less`

Then, we have some of the filters we have seen, such as `head` or `tail`, which we can use with the *pipes.

`cat food | head -7`{{ execute }}

Exercise -> How do you get only *milk* and *tomato* in the standard output?