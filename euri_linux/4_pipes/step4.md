The Linux console philosophy is to have many small programs (commands) that cooperate with each other to produce a complex result, to the detriment of a single very complex program with many options and modes of operation. Pipes were created to simplify collaboration between these applications; they make it possible to bridge the standard output of one program to the standard input of another.

Pipes are indicated by a vertical bar (" `|` ") between commands:

`command1 | command2 | command3`.

The above instruction represents a pipeline and allows the action of multiple commands to be combined into one. This is extraordinarily efficient because both command1 and command2 do not have to wait for the previous program in the pipeline to finish its execution to start processing the data they receive via *stdin*. In other words, the programs run in parallel and this speeds up processing on multi-core/multi-processor platforms. In addition the processing is done on the fly, there is no need to store the result of each pipeline program in a temporary file, this saves disk space and reduces disk read/write operations, which is usually the bottleneck of the computer.