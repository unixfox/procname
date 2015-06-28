This python library lets you easily rename your python programs in top and ps output.

## Usage ##

>>> import procname

>>> procname.getprocname()

'python'

# Lets check this. Press Ctrl+Z

user@comp:~/procname$ ps

> PID TTY          TIME CMD

13016 pts/2    00:00:00 bash

13128 pts/2    00:00:00 python     <--  it's python

13133 pts/2    00:00:00 ps


user@comp:~/procname$ fg

# Lets rename:

>>> procname.setprocname('My super name')

# Lets check.  Press Ctrl+Z

[1](1.md)+  Stopped                 python

user@comp:~/procname$ ps

> PID TTY          TIME CMD

13016 pts/2    00:00:00 bash

13128 pts/2    00:00:00 My super name    <--  it's here

13231 pts/2    00:00:00 ps


user@comp:~/procname$ fg

>>>

# Lets get current name

>>> procname.getprocname()

'My super name'

>>>


## Installation ##

Download source code and unpack it.

Install python-devel package to you system.

Edit file Makefile - set correct location of header files.

Then type 'make'. If all ok, you'll get a file procname.so. Use it :)


## Limitation ##

Currently Linux-only.