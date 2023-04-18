A funny thing

Let's move now to our *home*. `cd`{{ execute }}

The `echo` command prints out what we enter. For example `echo HOLA World o0`{{ execute }}.

But a funny thing happens if we run `echo *`{{{ execute }}}.

There's something strange here. If echo repeats the parameters we expect it to write an asterisk (\*). Why does this happen?

The key is that the *command interpreter* has intervened. The command interpreter has replaced the asterisk with the ordered (ascii-coded) list of object names that do not begin with a full stop. The command interpreter then called the echo program by passing that list of names as parameters.