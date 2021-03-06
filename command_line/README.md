# Sample scripts using the vtrace API

> **NOTE:** To run these scritps you need the latest version of vdb from:
> [http://visi.kenshoto.com/releases/](http://visi.kenshoto.com/releases/)
> 
> Untar the latest version and update the VDB_ROOT in the scripts to make them work.

## simpleAPI
> List of functions to use as reference on how to accomplish specific tasks.

## simpleAttach
> Script that attaches to a given PID and continues execution of the program.

## simpleDisasm
> Script that converts a string of hex data to assembly output.

## simpleFollowChild
> Script that follows a child process created from CreateProcessA in windows.  Will breakpoint on the first instruction executing in the child process.

## simpleFunctionList
> Script that outputs all the functions in a dll.

## simpleIAT
> Prints out the import table for the given executable.

## simpleIAT_NX
> Extension of simpleIAT script.  Scripts will set the IAT of a binary to unreadable causing a signal to be thrown on each external library reference and call.  The signal is then caught by a custom notifier class that will log them into a list in the order they were called, and continue the program.  Once process ends it will print out the list of called functions.
> The difference between the two scripts is that simpleIAT_NX_vdb is meant to be started within an already running vdb instance, simpleIAT_NX can be run from a commandline directly.

## simpleNotifier
> Script that implements a notifier class to output data when specific signals are caught.

## simpleOEP
> Script that parses the PE headers and calculates Original Entry Point (OEP).

## simpleReg
> Script that prints out the current values of some registers.

## simpleRet
> Calculates the return address of a function upon entering into the function.

## simpleRun
> Script showing how to start a program with the debugger attached and continue execution.

## simpleSnapshot
> Takes a snapshot of memory after a process is run to OEP.  Saves the snapshot to a file called zTest.snap.

## simpleStalker
> Uses the stalker functionality within vtrace.

## simpleStalker_ChildProc
> Uses the stalker functionality to stalk a child process.  Combination of the simpleFollowChild and simpleStalker scripts.
