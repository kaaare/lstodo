# lstodo

`lstodo [-flr] [file1 file2 ...]`

List `# TODO:` comments from files or directories, optionally with line numbers and file names.

### Example
```
br@kyrandia~$ lstodo mojoapp.pl
# TODO: Add `modified` timestamp column to `comment` table.
# TODO: Write more tests for malformed requests.
# TODO: Change database user's password.
br@kyrandia~$ █
```

Also works on windows (no grep).

Supports only pound sign comment syntax (php/perl/sql/tcl/bash/python plus plus etc).

### Usage
`lstodo`
List TODOs from all files in the current directory.

`lstodo -f`
Include file names when listing TODOs.

`lstodo -l`
Include line numbers when listing TODOs.

`lstodo -r`
List TODOs from all files in the current directory and subdirectories recursively.

`lstodo file1 file2 ...`
List TODOs from file1 and file 2 and ...


### Notes about Windows

To get an experience identical to linux:

* Add a `.pl` extension to the file; `lstodo.pl`.
* Make sure `.pl` files are opened with your perl interpreter.
* Put the file in a directory in your `PATH` environment variable.
* Add `;.PL` to the `PATHEXT` environment variable.

It can now be used like on linux, typing just `lstodo` instead of `perl lstodo.pl`.
