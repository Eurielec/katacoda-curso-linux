**Substitutions with `vi` or `sed`**.

Regular expressions scan the lines from left to right. Among the leftmost sequences, they select the longest one. For example, in one line we have alababa and we want to replace the characters between an `a` and a `b` inclusive by an `X` . There are five possible sequences. Later we impose that there is no b in the middle of the sequence to be substituted. There are three possible sequences.

`echo 'alababa' > ersed`{{ execute }}

`sed -e 's/a.*b/X/' ersed`{{ execute }}

`sed -e 's/a[^b]*b/X/' ersed`{{ execute }}


---

You can put references to marked subexpressions in the second part (second parameter) of a substitution.

`echo 'a8b a6c b8b a98b' > solomon`{{ execute }}

`sed -e 's/a\([0-9]*)b/A\1B/g' solomon`{{ execute }} substitutes the sequence: an `a` character, followed by digits (or none), followed by a `b` character with an `A` character, followed by those same digits followed by a `B` character (as many times as it finds it).

Now let's write another file to see another behaviour of `sed`:

`echo 'stafania' > christopher`{{ execute }}

`sed -e 's/\([aeiou][aeiou]/\1/g' christopher`{ execute }}

The above command duplicates the first pair of (consecutive) vowels it finds in each line.

We can run the following command a few times and something very funny will happen `sed -e 's/\([aeiou][aeiou][aeiou]/1/g' christopher >> christopher`{ execute }}