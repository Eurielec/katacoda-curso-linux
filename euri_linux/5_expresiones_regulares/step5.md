Los siguientes ejemplos también son útiles:

* `[0-9]` - cualquier cifra.

`printf "8 a8 8b8 8, 9,a a9, ab ab3 ab," | egrep --color '[0-9]'`{{ execute }}

* `[0-9,]` - cualquier cifra o la coma.

`printf "8 a8 8b8 8, 9,a a9, ab ab3 ab," | egrep --color '[0-9,]'`{{ execute }}

* `[^0-9]` - cualquier carácter excepto las cifras.

`printf "8 a8 8b8 8, 9,a a9, ab ab3 ab," | egrep --color '[^0-9]'`{{ execute }}

* `[0-9][^0-9][0-9]` - dos cifras separadas por un carácter que no es cifra.

`printf "8a9 a8 8  b8n8,9,a a9, ab ab3 ab," | egrep --color '[0-9][^0-9][0-9]'`{{ execute }}

* `[0-9].*[^0-9].*[0-9]` - dos cifras separadas por algún o algunos caracteres que *no son todos* cifras.

`printf "8aaaa9 a8 8  b8n8,9,a a9, ab ab3 ab," | egrep --color '[0-9].*[^0-9].*[0-9]'`{{ execute }}

* `[0-9][^0-9][^0-9]*[0-9]` - dos cifras separadas por algún o algunos caracteres que *no es ninguno* cifra.

`printf "8aaaa9 a8 8  b8n8,9,a a9, ab ab3 ab," | egrep --color '[0-9][^0-9][^0-9]*[0-9]'`{{ execute }}
