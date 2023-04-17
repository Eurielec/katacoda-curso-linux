The following examples are also useful:

* `[0-9]` - any digit.

`printf "8 a8 8b8 8, 9,a a9, ab ab3 ab," | egrep --color '[0-9]'`{{ execute }}

* `[0-9,]` - any digit or comma.

`printf "8 a8 8b8 8, 9,a a9, ab ab3 ab," | egrep --color '[0-9,]'`{{ execute }}

* `[^0-9]` - any character except digits.

`printf "8 a8 8b8 8, 9,a a9, ab ab3 ab," | egrep --color '[^0-9]'`{{ execute }}

* `[0-9][^0-9][0-9]` - two digits separated by a non-digit character.

`printf "8a9 a8 8 b8n8,9,a a9, ab ab3 ab," | egrep --color '[0-9][^0-9][0-9]'`{{ execute }}

* `[0-9].*[^0-9].*[0-9]` - two digits separated by some character or characters that *are not all* digits.

`printf "8aaaaaaa9 a8 8 b8n8,9,a a9, ab ab3 ab," | egrep --color '[0-9].*[^0-9].*[0-9]'`{{ execute }}

* `[0-9][^0-9][^0-9]*[0-9]` - two digits separated by some character(s) that is *not any* digit.

`printf "8aaaaaa9 a8 8 b8n8,9,a a9, ab ab3 ab," | egrep --color '[0-9][^0-9][^0-9]*[0-9]'`{{ execute }}