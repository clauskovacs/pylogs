# pylogs

A python class to manage (creating, pushing, etc.) logfiles.

## Folder Structure

This project has the following folder structure
```
.
└── pylogs.py
```
The file **pylogs.py** contains a class which manages the logfiles. Creating of logfiles as well as pushing into logs (short one-line messages as well as information dumps is supported).

## Usage

Import the files via *import pylogs* in your python program.

Each logfile is initialised using a class object via, e.g.:
```
logging = pylogs.logs("logs/", "testlog")
```

Pushing into the log can either be done by appending to an existing log instance via
```
logging.append_to_log("logmessage1")
logging.append_to_log("logmessage2")
logging.append_to_log("logmessage3")
```
which appends the given logmessage into the logfile (preceeded by the current date).

A textblob (larger textinformation) can be pushed to a (single) logfile using:
```
logging.dump_to_log(textblobstring, "header")
```
This creates the logfile which consists of a header (time, date and the given header) followed by the textblobstring.
