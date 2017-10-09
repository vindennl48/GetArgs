# GetArgs
Argument Parser for Python

This module is used to simplify the need to deal with arguments passed to
your __Python__ programs.  Instead of needing to write a separate function or
member to deal with terminal arguments every program, you can 
```python
from GetArgs import getargs
```

##How To Use
To set up __GetArgs__, you must initialize the flags that you want to use.
```python
myargs = getargs(['-h','--help','-s','-r','-up','username', 'password'])
args = myargs.getargs()
```

`args` is a Dictionary of the flags set in the terminal.  To find if a flag was 
used in the terminal:
```python
if '-h-' in args or '--help' in args:
    foo()
if '-up' in args:
    usrnm = args['username']
    pword = args['password']
```

__GetArgs__ will also raise an exception for any flags set that are not in the
list specified in the class init.

## Dependencies
 - Python 3.x
