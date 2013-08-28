screenfetch-c
=============

### Current Version: 0.5 Alpha (compiled, not complete)

screenfetch-c is an attempt to rewrite screenFetch, a popular shell 
script that displays system information and an ASCII logo, in the C 
language.
Like the original screenFetch, screenfetch-c will be capable of 
compiling and running on Windows (via Cygwin), all Linux distros, the 
four major *BSD distros, and OS X.

### Current Status:
Right now, the majority of detection functions are complete.
However, some of the larger ones (detect_distro(), detect_wm(), 
detect_pkgs()) are lacking Linux/BSD sections due to a lack of a testing 
environment.
screenfetch-c has been successfully compiled and run on Cygwin and OS X, 
with most information being displayed correctly.
However, more testing needs to be done.
Current phase: completion of BSD/Linux sections, as well as addition of colors to outputted stats.

### Compiling screenfetch-c:
Because screenfetch-c has no dependencies outside of the standard library/POSIX API, 
it is very easy to compile and run:

```
gcc screenfetch-c.c -o screenfetch -std=c99
./screenfetch [options]
```

Just be sure that screenfetch-c.h is in the same directory, as it contains all of 
screenfetch-c.c's prototypes and macros.

_Note:_ For some reason, compiling screenfetch-c on Lubuntu results in a bunch of implicit warnings,
despite unistd.h and all required functions being present.
If this occurs for you, just add the '-w' flag to your compilation command to suppress the warnings.

### Examples:

![alt tag] (http://puu.sh/4bxE9.png)
![alt tag] (http://puu.sh/4bxFQ.png)
![alt tag] (http://puu.sh/4cGCt.png)
![alt tag] (http://puu.sh/4cK61.png)

