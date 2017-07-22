# py1.0

This repository contains a Python 1.0 for those who can't find
[this download page](http://legacy.python.org/download/releases/src/)
and rename the `getline()` function to something else in
[Objects/fileobject.c](Objects/fileobject.c). Most of the content in
this repository comes from `python1.0.1.tar.gz` on the page linked above.

## Compiling

I don't know what dependencies you need. [Create an
issue](https://github.com/8Banana/py1.0/issues/new) if you need help,
and we'll update this README accordingly.

Assuming that you managed to magically install all dependencies, here's
what you need to run:

    $ git clone https://github.com/8Banana/py1.0
    $ cd py1.0
    py1.0$ ./configure && make

Then you can run `./python`. There's no readline support, so you won't
get any nice autocompletion or history of commands, but it works.

For some reason, `Lib` is not on `sys.path` by default, but that's easy to fix:

```python
>>> import string
Traceback (innermost last):
  File "<stdin>", line 1
ImportError: No module named string
>>> import sys
>>> sys.path.append('Lib')
>>> import string
>>> string
<module 'string'>
```

## See also

[README.original](README.original) used to be a file called `README`.
