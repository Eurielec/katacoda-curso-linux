**sed (stream editor)**.

The `sed` program is a non-interactive editor or stream editor. It allows basic transformations of an input stream (a file or an input from a pipe).

The format (for substitutions) is as follows:

`sed [options] 's/REGEXP/replace/flag' [file]`.

Some commands:
* `s` substitution
* `d` deletion
* `i`, `a`, add before/after the affected line
* `c` replace the affected line

Some options:
* `-e` command: add command
* `-i` edits the in-place file
* `-n` suppresses output

Some flags:
* `g:` applies changes globally (by default, only the first occurrence on each line is changed) * `-p` prints affected lines, even with `-p` option.
* `p` prints the affected lines, even with the `-n` option.
* `w file`: writes the lines with substitutions to the specified file.


**It is important to note that you need to use old regular expressions**.

A small example of how to use `sed`:

`printf "abajhbab" | sed -e "s/\(.\)"`{ execute }}