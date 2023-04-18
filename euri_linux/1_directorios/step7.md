The `cd` command remembers its last position, and allows you to return to it by using `cd -`. To remember previous directories we have `pushd`. This command not only moves you to the desired directory (as `cd` would do), but also stores the previous directory in a stack. To return to the last directory on the stack, `popd` is available. The directory stack can be displayed using the `dirs` command.

You can go to `/root/tres/pedal` with `pushd /root/tres/pedal`{{ execute }}, then move to `/root/uno` with `pushd /root/uno`{{ execute }}.

Now you can list your directory queue with `dirs`{{{ execute }}}

And go back to where you were with `popd`{{ execute }}

Exercise-

Move around the filesystem with `pushd` and `popd`.