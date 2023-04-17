When executing commands, by default we have three file streams (or descriptors): **standard input** (standard input, standard in or stdin), **standard output** (standard output, standard out or stdout) and **standard error output** (standard error or stderr). Usually stdin is the keyboard and stdout and stderr are displayed on the terminal.

* 0` Standard input (stdin)
* `1` Standard output (stdout)
* `2` Standard error output (stderr)

If you want to redirect stderr to another file, use its file descriptor (2), and the greater than sign (" > "), followed by the name of the file to which stderr will be dumped:

`ls -l /bin/bash /kaka > output 2> error`{{ execute }}

Two files have appeared, `output` and `error`. What is each?

You can use the notation 2>&1 to dump stderr into the same file as stdout.

`ls -l /bin/bash /kaka > stdout 2>&1`{{ execute }}

Bash implements a simplified notation of the above statement:

`ls -l /bin/bash /kaka >& output`{{ execute }}