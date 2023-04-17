Regular expressions are a language for describing strings of characters.

They first came into use with ed, a line-oriented editor. Later they were included in other commands. Following good programming methodology, they were not in the code of each command, but in a library of functions, and their behaviour was the same for different commands.

At a certain point, the functionality of regular expressions was rethought and a variant emerged. I will call these dialects *old regular expressions* and *modern regular expressions*. Both dialects share a set of rules.

**Common part

Valid for `grep`, `vi`, `sed`, `ed`, `more`, `egrep` and `awk`.

* c` - A non-special character is valid by itself. A character can be special in modern regular expressions, and non-special in older regular expressions, e.g. `|`.
* `.` - any character except line shift (ascii 10 decimal).
* `?` - Zero or a reference to the previous character.
* `*` - Represents any character string.
* ``` - ``` **Cancels** the meaning of special characters. This character, the inverse ( ```` ), is also a special character.
* ``^` - **Start of line**, something before the first character of a line.
* `$` - **Line end**, something after the last character of a line.
* `[abz]` - **Alternate characters**. `a` or `b` or `z`. In general, any of the characters in square brackets.
* `[i-n01]` - **Alternative**. Allows character ranges to be specified. In this case it specifies any lower case letter from `i` to `n`, or the digit `0`, or the digit `1`.
* `[^a-zA-Z]` - **Any character except the quoted characters and the line shift**. The character `^` immediately following `[`[` indicates complement of the named characters with respect to the character set without the line shift. The `^` character in another bracketed position represents itself.
* a*` - **Zero or more repetitions of a**. The asterisk indicates zero or more repetitions of the immediately preceding.

**Old regular expressions

Valid for `grep`, `vi`, `sed`, `ed`, and `more`.

* ``(a*b\)` - **A tagged (sub)expression in which zero or more `a` characters are followed by a `b`** character. (Sub)expressions are marked by placing them between `(`) and `(b)`.
* Reference to the second marked (sub)expression**. When we make a reference to a marked expression we are saying: '*the same, exactly the same as before'.
* ``` - **Beginning of a word, something before the first character of a word**. A word is a sequence of one or more letters, digits and underscores. (More like *C*, or *awk* language identifiers than words to me). Each word shall include as many characters as possible.

* `[a-z][a-z][a-z]` - Represents any three lowercase letters.
* ``[a-z][a-z][a-z][a-z]` -
