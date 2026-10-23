# What Happens When You Run Code?

This investigation connects variables, memory, the operating system, processes, and language runtimes. The exact details depend on the language, implementation, and operating system; Python examples below describe the common CPython experience unless noted otherwise.

## When you type `x = 10`, where exactly does `10` go?

Python evaluates `10` as an integer object and binds the name `x` to it in the current namespace. The name and object are represented in the memory of the Python process, which the operating system maps into physical RAM as needed. There is no single universal physical address: implementations manage object layout, memory can move or be paged, and an address is not a stable property of the Python value. If no references remain, the runtime can reclaim the object.

The path to investigate is: **Variable → Object → Memory → RAM → Process → OS**. See [variables](../02-variables-and-memory/variables.md), [memory](../02-variables-and-memory/memory.md), [stack and heap](../02-variables-and-memory/stack-and-heap.md), and [garbage collection](../02-variables-and-memory/garbage-collection.md).

## When I type `python app.py`, what happens between pressing Enter and seeing output?

The shell parses the command, finds a Python executable using its configured command lookup (often `PATH`), and asks the operating system to start it. The OS creates a process and loads the interpreter. Python reads and parses `app.py`, compiles it to code objects (commonly bytecode in CPython), and executes the code. The program's output goes to the terminal unless it redirects it elsewhere. Errors may be printed and cause a nonzero exit; the OS then reclaims process resources.

The Python interpreter itself is a native program; its runtime executes Python semantics using CPU instructions. See [how code runs](../01-programming-basics/how-code-runs.md), [compilers](../03-how-programs-run/compiler.md), [interpreters](../03-how-programs-run/interpreter.md), and [processes](../03-how-programs-run/process.md).

## How does a program know that another program has crashed?

Programs do not automatically know that a peer has failed. A parent process can receive an exit status when a child exits; an operating-system supervisor can monitor a process; network services can use health checks, timeouts, and heartbeats. A missing heartbeat can also mean a slow network rather than a definite crash, so distributed systems use timeouts as evidence and design for uncertainty. See [processes](../03-how-programs-run/process.md), [threads](../03-how-programs-run/threads.md), and [servers](../08-cloud-and-deployment/server.md).
