The `locate` tool searches a database of local files and directories. As you can see, the result of this command returns the absolute `path` of the files or directories that match the string that accompanies the command.

Let's see a couple of examples:

* `locate howToComunicate.txt`{{execute}} Will return the path of the file asCommunicate.txt
*  `locate *.txt`{{execute}} Return all paths to all files that are text notes or .txt.

You can also use the pipe system explained above:
* `locate *.txt | grep c` {{execute}} In this case it will return the paths of the .txt files having the pattern c (containing the letter c)
Maybe with the previous example you do not see special value in the use of pipes, but if you have to search for example all the information about zip and that is inside the bin directory is a very useful tool because with the simple instruction `locate zip | grep bin`{{execute}} we will get the path to access them



It is important to note that the database used by `locate` is created and updated with the `updatedb` program and most Linux distributions run this process once a day, but like everything in Linux it can be run manually but only if you have root permissions with `sudo updatedb`{{execute}}