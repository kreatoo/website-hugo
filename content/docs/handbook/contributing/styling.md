---
title: "Code styling"
draft: false
---

This page describes the coding style that is preferred on Kreato Linux projects. If you are looking to contribute, please consider the points here.

This page was heavily inspired by Linux kernel coding standards, in terms of how it is laid out.

# Indentation
Most of Kreato Linux code is written in Nim, so indentation is very important. Indents should be 2 characters most of the time. 4 characters are also accepted, but not more.

Example;

```nim
proc testProc(test: string): int =
    ## Test proc.
    if test == "hello":
        echo test    
```

# Comments
We believe code should be readable without requiring comments. If you still require comments, it is then allowed. `proc`s that are for a command (example: install() on kpkg/commands/installcmd.nim) have to have comments with double hashtag (`##`), explaining what they do in a single line. This comment will be visible on the help page of the main command (eg. `kpkg --help`). Comments should be as short as possible.

Example;

```nim
proc testCommand() =
    ## Says hello world.
    echo "Hello, World!"
```

# Variables
**DO NOT** use short variables. Variables should explain what they are for. If it is too long to explain, you should explain it with a comment. Variables, like procs, should use camelCase.

Example;

```nim
var t: int # Wrong
var time: int # Correct

# Wrong
var d = "/tmp/destdir"

# Correct
var destDir = "/tmp/destdir"
```

# Naming
Kreato Linux uses camelCase by default. Try to stick to camelCase. Paths do not have to use camelCase but it would be a nice addition.

Example;

```nim
var destdir = "/tmp/destdir" # wrong
var destDir = "/tmp/destDir" # correct
```

Naming shouldnt be *too* long (eg. `destDir` instead of `aVariableThatOutputsDestDir`).

# Procedures
Procedures should be simple, in both naming and job. If it is a general function, it should use exceptions and retturn a value.

Examples;

```nim
proc testProc(a, b: int): int =
    # Combines a and b. 
    return a + b

proc testExceptionProc (test: string): string =
    # Checks if test is "Hello", returns OSError otherwise.
    if test != "Hello":
        raise newException(OSError, "Test is not Hello")
    else:
        return test
```
