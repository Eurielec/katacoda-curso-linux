Command `tee` command

`who | tee tmp | wc -l | cat - tmp`{{ execute }}

Four commands work in a chain. The output of one command serves as input to the next.
* `who` describes the sessions on the system.
* `tee tmp` takes two copies of the characters it reads. One copy goes to standard output, the other to the `tmp` file.
* `wc -l` counts incoming lines.
* `cat - tmp` concatenates what it reads from the standard input ( - ) with the `tmp` file.

The `tee` command is used to make two copies of a piece of information, one for immediate processing.

Another example:

`cat votes | grep "null" | tee file2.txt | wc -l`{{ execute }}