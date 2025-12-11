# TaskList — Doubly Linked List To-Do Manager (C++)

**Overview / Summary**

This project implements a fully functional `TaskList` ADT using a **doubly linked list**, demonstrating advanced C++ concepts:

- Manual **dynamic memory management** with raw pointers
- Full **Rule of Three**: destructor, copy constructor, and assignment operator
- **Deep copy semantics** ensuring independent lists
- **Pointer-safe traversal and modification**
- Index-based access, search, insertion, and removal
- **Test-driven development** with comprehensive assert-based validation

This system models a professional-quality, pointer-driven data structure suitable for productivity apps or task management systems.

---

## TaskList Module

Handles all list-related functionality for managing tasks (strings).

**Implemented capabilities:**

- Adds tasks to the end of the list (`addBack`)
- Removes the front task (`removeFront`)
- Checks if the list is empty (`empty`)
- Retrieves the number of tasks (`size`)
- Indexed retrieval of tasks (`get`)
- Search for tasks by value (`find`)
- Clears the list (`clear`)
- Prints all tasks to `cerr` (`printAll`)
- Full deep-copy and assignment support for value semantics

These functions provide robust, safe, and deterministic behavior for all task list operations.

**Memory & Safety Features:**

- Doubly linked nodes with `prev`/`next` pointers
- Maintains `head`, `tail`, and size for efficient operations
- `getNode(int pos)` helper ensures safe index traversal
- `copyList()` and `freeList()` for correct memory management
- No memory leaks; deep copies prevent shared ownership errors
- Edge-case handling for empty or single-element lists

---

## Testing

The `main.cpp` file includes a thorough set of **assert()** tests verifying:

- Behavior on empty list (size, removal, retrieval)
- Single-element lifecycle (add, get, find, remove)
- Multi-element behavior (add multiple tasks, get all, find existing and missing tasks)
- Sequential removals update size correctly
- Copy constructor produces an independent deep copy
- Assignment operator supports deep copy semantics and self-assignment safety
- Clearing the list frees memory and allows reuse
- Edge-case index handling for `get()` and `find()`

All tests pass and demonstrate expected outputs

