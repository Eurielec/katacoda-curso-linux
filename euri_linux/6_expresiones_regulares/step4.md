Now we will look at the following regular expressions. Remember that in *step 1* are the most important regular expressions.

* `[aeiou]` - any lowercase vowel.

`printf "ae a b ab j e io o" | egrep --color '[aeiou]'`{{ execute }}

* `[^aeiou]` - any character except lowercase vowels.

`printf "ae a b ab j e io o" | egrep --colour '[^aeiou]'`{{ execute }}

* `[aeiou^]` and `[a^eiou]` - any lower case vowel or the circumflex accent `^`.

`printf "ae a b ^^ ab j e io o ^" | egrep --color '[a^eiiou]'`{{ execute }}

* `[a-z]{4,6}` - Between 4 and 6 consecutive lower case letters. Put between `{` and `}` the minimum and maximum number of times the above can be repeated. With old regular expressions it would be `[a-z]\{4,6}` - Between 4 and 6 consecutive lowercase letters. The minimum and maximum number of times the above can be repeated is put between `{{` and `{}}`.

`printf "aaaa aaaa aaaa aaaa aaaa aaaa aaaa aaaaaaaaaaaaaaa" | egrep --color '[a-z]{4,6}'`{ execute }}

* `[a-z]{4,6}' - 7 consecutive lowercase letters.

`printf "aaaa aaaa aaaa aaaa aaaa aaaa aaaa aaaaaaaaaaaaaaa" | egrep --color '[a-z]{7}'`{ execute }}

* `[a-zA-Z0-9]*` - a (perhaps empty) sequence of letters and digits. It is similar to a pascal language identifier.

`printf "b8 bB8a a90 a|5 ab6 # a7b a77b b77c bb aa 7b abc8 8@9 - @" | egrep --color '[a-zA-Z0-9]*'`{{ execute }}

* `[a-zA-Z][a-zA-Z0-9]*` - A letter followed by zero or more letters or digits. This is the form of Pascal language identifiers.

`printf "b8 bB8a a90 a|5 ab6 # a7b a77b b77c bb aa 7b abc8 8@9 - @" | egrep --color '[a-zA-Z][a-zA-Z0-9]*'*'`{{ execute }}