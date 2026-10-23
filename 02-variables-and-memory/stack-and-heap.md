# Stack and Heap

“Stack” and “heap” describe common ways runtimes organize memory; they are useful models, not identical rules in every language or implementation.

## Curiosity questions and answers

### 26. What is a stack?

A call stack tracks active function calls. Each call has a frame for information such as local state, return location, and arguments, though the exact contents vary by runtime. Returning from a function removes its frame. Deep or unbounded recursion can exhaust stack space.

### 27. What is a heap?

The heap is an area commonly used for dynamically allocated objects whose lifetimes do not fit neatly into a single function call. In Python, objects are generally managed by the runtime and many live in a heap, while local names and execution frames have their own implementation details. Programmers should rely on language lifetime rules, not assume a specific physical arrangement.
