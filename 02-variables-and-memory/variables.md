# Variables and Values

A variable is a name a program uses to refer to data. The exact relationship between a name and a value depends on the language: in Python, a name is bound to an object rather than being a labeled box containing the value.

## Curiosity questions and answers

### 11. What happens internally when you write `x = 10`?

Python evaluates the integer literal `10`, obtains an integer object, and binds the name `x` to that object in the current scope. Assignment does not mean that a physical box named `x` is necessarily created; the runtime maintains name bindings and object references.

### 12. Where is `10` stored?

The integer is represented as a Python object in the process's memory. Its physical location is managed by the Python implementation and operating system; Python code should not assume a fixed address or a particular memory layout.

### 13. Where is `x` stored?

`x` is a name in a namespace, such as a module's global namespace or a function's local namespace. That namespace maps names to objects or references. The runtime chooses how to represent and store it.

### 14. Is `x` actually the value `10`?

In Python, `x` is a name bound to an integer object whose value is 10. It is useful to think of the name as a label or reference, not as the object itself. This distinction becomes important when multiple names refer to the same mutable object.

### 15. What happens when you assign `x = 10` and then `x = 20`?

The second assignment rebinds `x` to the integer object representing 20. It does not mutate the integer 10; integers are immutable in Python. If no names or other references still reach the old object, it can eventually be reclaimed.

### 16. What happens to `10` after `x = 20`?

The integer object for 10 remains available if anything else refers to it. If it has no remaining references, Python can reclaim it; exact timing and memory reuse depend on the implementation. Python may also reuse some immutable objects internally, so identity and memory addresses should not be inferred from small examples.

### 17. What happens when you write `a = b = c = 100`?

Python evaluates the right-hand expression and assigns the resulting object to each target name. All three names refer to the resulting value; the statement does not promise three separate physical copies.

### 18. Are `a`, `b` and `c` three copies of `100`?

They are three names bound to the value produced for `100`. Python integers are immutable, so sharing the same integer object has no observable effect through ordinary mutation. For mutable values, shared references matter: changing an object through one name can be seen through another name that refers to it.

### 19. What happens to variables when a function finishes?

A function's local namespace stops being active when the call returns, so its local names are no longer usable by the caller. Objects those names referenced remain alive if another reference exists—for example, a returned value, a global name, or a closure. Otherwise they become eligible for reclamation.
