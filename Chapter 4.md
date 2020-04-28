# Copy of Kreig's Notes

# 4.1 What is Ownership?

## Stack

- LIFO, hence push and pop.
- Fixed known size for all data.
- Pointers placed here.
- This memory access is faster.
- think *"stack of plates*"

## Heap

- For unknown size data.
- Request x size and OS finds big enough f in heap and returns pointer.
- Sounds like Classic MacOS memory management lol
- ... standard scoping chatter
- `String` ≠ string literal
- ah cool copypasta of the example provides a compiler directive e.g. `#![allow(unused_variables)]`
- Ah! ***Scoping*** is how Rust manages memory. Not garbage collection.
- When a variable is re-assigned it receives a new pointer on the stack pointing to the same location as the original variable on the heap. A bit like an `Object.assign {}`
- The old pointer and assignation becomes *invalid*!
- So this is called a *move*. Not like a deep clone in js.
- For this there's an actual `.clone()` method.
- But this is all only for complex types. Integers do not follow these rules as they are always on the stack.
- Tuples are a good way to more cleanly pass variables into and out of functions due to ownership.

# 4.2 References and Borrowing