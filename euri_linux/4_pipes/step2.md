Redirection of standard input

If you type the command `cat` *just*, it redirects standard input to standard output. Try it

`cat`{{ execute }}

To exit, we can press *Ctrl-D*. It is important to note the following:
* *Ctrl-D* sends the *EOF* signal to the standard input. And the `cat` program interprets it to exit.
* *Ctrl-C* Abort the application.
* *Ctrl-Z* takes it to the *background*.

With the behaviour of the `cat` command we can see the following:

`cat < shoppingList`{{ execute }}

As we can see, we can see the content of the file `shoppingList` using a redirect (normally it will not use this way).

Now we will see the following behaviour:

`cat << END`{{ execute }}

Try typing some things through the standard input, and now try typing *END*. What happens?