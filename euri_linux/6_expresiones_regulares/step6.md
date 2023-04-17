We have the following regular expressions, which it is good to highlight again:
* `.*` - any character strip (including empty or null length strip).
* `..*` - any character strip (with at least one character).

We can now look at the following examples.

* ``([0-9]\1`) - A two-digit capicua number.

`printf "989 9 898 22 33 678" | egrep --colour '([0-9])\1'`{ execute }}

* `(.)\1` - two equal *consecutive* characters.



* ``(.\).*\1` - two characters repeated.



* `(...*)1` - two sequences repeated consecutively



* `(..*).* "- two repeated sequences



How would you search for a 5-digit capicua number?
How would you do it with 5 capicua letters?