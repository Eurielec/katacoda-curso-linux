We are going to go through some of the most used regular expressions one by one.  We will focus on the following for now:

* `.` - any character, except line shift (ascii 10 decimal).
* `?` - Zero or a reference to the previous character. **This is a modern regular expression**.
* `*` - Represents any string of characters.

As these are modern regular expressions, we will use `egrep`, the evolution of `grep`. From now on we will use the `-egrep` option to paint the results, `--colour`.

We can see the differences in each regular expression with the following examples:

`printf "colour colour" | egrep --colour 'colou?r'`{ execute }}

`printf "colour colour colour colour" | egrep --colour 'colou*r'`{{ execute }}

`printf "colour colour colour" | egrep --colour 'colo.r'`{ execute }} `printf "colour colour colour" | egrep --colour 'colo.r'`{ execute }}

`printf "colour colour colour" | egrep --colour 'colou.r'`{ execute }}

The differences between `?` and `.` can be a little confusing. We can see it better with the following example:

`printf "error "error" | egrep --colour 'er?or'`{ execute }}

`printf "error "error" | egrep --color 'er*or'`{ execute }}