Now let's look at the following regular expressions:

* `(a*b)` - **Modern regular expression - A marked (sub)expression in which zero or more `a` characters are followed by a `b`** character. (Sub)expressions are marked by placing them between `(` and `)`.
* (sub)expressions are marked by placing them between `(` and `)`. (Sub)expressions are marked by placing them between `(`) and `(b)`.
* Reference to the second marked (sub)expression**. When we make a reference to a marked expression we are saying: ``the same, exactly the same as before``.

So:

* `p.p.` - gives true if it finds *pepa*.
* ``(p.p.)1` - does not match *pepa*, and does match *pepepe*, **using old regular expressions**.
* `(p.)\1` - does not match *pepa*, and yes *pepepe*, **using modern regular expressions**.

We could check that:

`printf "pepepepepepepepepepepepepe" | egrep --color 'p.p.'`{{ execute }}

`printf "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe" | egrep --color '(p.)1'`{ execute }}}

`printf "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe "pepe" | grep --color '(p.\1'`{ execute }}}


Now then. If we print the following file:

`printf "aa aba apa aabs abba baab bab"`.

How would you print only `abba` and `baab`?

You could do it with `printf "aa aba aba aabs abba baab bab" | egrep --color "(.)(.)` `{{execute}}