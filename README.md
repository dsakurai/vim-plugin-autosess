autosess
========

== Description

Start Vim without file arguments to automatically load previous session for current directory. This make easier work with complex projects - just start `vim`.

Set the session name in the environment variable `VIM_AUTOSESS_NAME`.
It is assumed that the session name is some directory.
You can therefore use direnv to set the session name automatically:

Example `.envrc` file

~~~
export VIM_AUTOSESS_NAME="$PWD"
~~~

When you quit from Vim, if there are more than one open tab/window, session will be automatically saved. This let you edit single files in same directory without breaking your saved session. (Quickfix and vimdiff's windows are ignored.)

If you quit from Vim with no open files, session will be deleted. This let you start usual empty Vim in this directory next time.

Download .zip/.vmb from http://www.vim.org/scripts/script.php?script_id=3883
