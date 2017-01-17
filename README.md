# CSE410 Lab 1
Bit and Pointer puzzles
## Desc
CSE 410 WI17
Junfei Zhang

find details [there](https://courses.cs.washington.edu/courses/cse410/17wi/lab-1.html)

## Debug
We have included two tools to help you check the correctness of your work.

dlc is a modified version of an ANSI C compiler from the MIT CILK group that you can use to check for compliance with the coding rules for each puzzle. The typical usage is:

```
$ ./dlc bits.c
```

Note: dlc will always output the following warning, which can be ignored:

```
/usr/include/stdc-predef.h:1: Warning: Non-includable file <command-line> included from includable file /usr/include/stdc-predef.h.
```

The program runs silently unless it detects a problem, such as an illegal operator, too many operators, or non-straightline code in the integer puzzles. Running with the -e switch:
```
$ ./dlc -e bits.c
```
causes dlc to print counts of the number of operators used by each function. Type ./dlc -help for a list of command line options.

btest is a program that checks the functional correctness of the code in bits.c. To build and use it, type the following two commands:
```
$ make
$ ./btest
```
Notice that you must rebuild btest each time you modify your bits.c file. (You rebuild it by typing make.) You'll find it helpful to work through the functions one at a time, testing each one as you go. You can use the -f flag to instruct btest to test only a single function:
```
$ ./btest -f bitXor
```
You can feed it specific function arguments using the option flags -1, -2, and -3:
```
$ ./btest -f bitXor -1 7 -2 0xf
```
Check the file README for documentation on running the btest program.

We may test your solution on inputs that btest does not check by default and we will check to see if your solutions follow the coding rules.