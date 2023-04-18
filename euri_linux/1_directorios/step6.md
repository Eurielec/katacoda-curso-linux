The *"path "* is the Anglo-Saxon term used to describe the path to a target file or directory. There are two ways to identify path:
* Absolute path: Starts at the root directory and follows the directory tree branch by branch until it reaches the target directory or file. Absolute paths always start with /. For example `cd /root/dos/anotherDirectory`{{ execute }}
* Relative path: Starts in the current working directory. Relative paths never start with /. For example `cd ~/dos/anotherDirectory`{{ execute }}

Multiple slashes (`/` or *slash*) are allowed between directories and the file, the system ignores the excess. In short, `////usr//bin` is valid because the system interprets it as `/usr/bin`. E.g.: `cd //root////dos///anotherDirectory`{{ execute }}

It is often more convenient to use relative paths as they require less typing. Their main advantage is that the following shortcuts are available:

* `.` Current directory
* `..` Directory father of the current
* `∼` Home (`/home/tu_usuario`)
* `∼usuario33` usuario33's home (`/home/usuario33`)

**Ejercicio** ->

Go to `/root/two/anotherDirectory`. Try going to `/root/three/helmet`.

In principle there are 3 ways. Using an absolute path and using relative path with `~` or `../../`. Is there any other way?
