#
# Looks for a directive in the form: #! C:\Python30\python.exe
# The directive must start with #! and contain ".exe".
# This will be assumed to be the correct python interpreter to
# use to run the script ON WINDOWS. If no interpreter is
# found then the script will be run with 'python.exe'.
# ie: whatever one is found on the path.
# For example, in a script which is saved as utf-8 and which
# runs on Linux and Windows and uses the Python 2.6 interpreter...
#
#    #!/usr/bin/python
#    #!C:\Python26\python.exe
#    # -*- coding: utf-8 -*-
#
# When run on Linux, Linux uses the /usr/bin/python. When run
# on Windows using winpylaunch.py it uses C:\Python26\python.exe.
#
# To set up the association add this to the registry...
#
#    HKEY_CLASSES_ROOT\Python.File\shell\open\command
#    (Default) REG_SZ = "C:\Python30\python.exe" S:\usr\bin\winpylaunch.py "%1" %*
#
# NOTE: winpylaunch.py itself works with either 2.6 and 3.0. Once
# this entry has been added python files can be run on the
# commandline and the use of winpylaunch.py will be transparent.
#
