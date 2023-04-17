The command interpreter is normally responsible for establishing the connection between standard input and output to files or other processes. This change of the source and destination of reads and writes is called redirection. The user tells the shell which redirects he wants by means of conventions.

* `< fich1` makes the standard input `fich1`.
* `> fich2` makes the standard output `fich2`. If the file `file2` exists, its previous contents are lost. If the file does not exist, it is created.
* ` `>> fich2` causes the standard output to be `fich2` . If file `file2` exists, its contents are not lost. It is then written. If the file does not exist, it is created.
`<< sentinel` makes the standard input the lines below, terminating on finding *sentinel *sentinel *sentinel* *sentinel* *sentinel* *sentinel* *sentinel* *sentinel* *sentinel* *sentinel* *sentinel* *sentinel*.
* `com1 | com2` causes the standard output of `com1` to be carried to the standard input of `com2`. This is known as **pipe**.