**To see part of the content**

Sometimes we are only interested in seeing the first few lines of a file and we don't need to do `more` followed by `q` which will show us the first 22 lines.

`head -8 clothing_workshop.txt`{{ execute }}

`head -3 clothing_workshop.txt` shows the first 3 lines of the named file. `head` defaults to 10 lines.

On the other hand `tail -6 clothing_workshop.txt`{{ execute }} shows the last 6 lines of the named file. `tail` defaults to 10 lines.
