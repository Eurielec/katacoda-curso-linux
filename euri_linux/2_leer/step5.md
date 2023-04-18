**To view medium or large files**

If we send a large file to the screen, the lines fly, they pass before our eyes without us being able to read them. Even if they go slowly, we may want to look carefully at a formula, a sentence (judicial? computer?), ...

We want that until we say: - more - the output of characters on the screen stops and no information is lost at the top of the screen. That "more" gives the name to the command that will help us: `more`.

`more cripto_gpg.md`{{ execute }}

When we type a whitespace, `more` presents almost a new screen. Typing carriage return moves the text forward one line. Typing *slashes* (/) moves the cursor down to the last line. The next characters we type appear on the last line. When we give carriage return, `more` searches for the sequence indicated in the text not presented. The screen displays the searched character string on one of its first lines. A whitespace or carriage return at the end of the file ends the session with the `more` command. Another way to end the session is to type `q` (for quit).

The `less` is a command that supports all the possibilities of `more` and accepts other moves as well. In order not to force the user to learn new letter-move associations, `less` takes the moves from the vi editor and obeys them.

`less cripto_gpg.md`{{ execute }}
