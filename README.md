# Stack
## Overview

This repository contains two implementations of a Stack:
1. **Stack Implementation Using Array**
2. **Stack Implementation Using C++ STL (Standard Template Library)**

A stack is a linear data structure that follows the Last-In-First-Out (LIFO) principle, meaning the element inserted last will be the first to be removed. Stacks are commonly used in recursive algorithms, expression evaluation, memory management, and more.

## Advantages of Stacks:
- **Simple and Intuitive:** Stacks are conceptually easy to understand and implement, based on the LIFO (Last-In-First-Out) principle. This simplicity makes them ideal for handling temporary data and performing operations where order matters.
- **Efficient Memory Usage:** Stacks manage memory efficiently in situations where temporary storage is needed, such as in recursive function calls or expression evaluation.
- **Supports Recursive Algorithms:** Many recursive algorithms rely on stacks to store intermediate states or results. For example, recursive depth-first search (DFS) in graphs or recursive tree traversals are implemented using stacks.
- **Useful in Memory Management:** Operating systems and compilers often use a stack to keep track of function calls (known as the call stack). Each time a function is called, its local variables and return address are pushed onto the stack, and they are popped when the function returns.
- **Constant Time Operations (O(1)):** Both the push (insertion) and pop (deletion) operations can be done in constant time, making stacks very efficient when used for problems requiring sequential access to the most recent element.

## Disadvantages of Stacks:
- **Limited Access:** Stacks follow the LIFO principle, meaning you can only access or modify the element at the top. This restricts flexibility if access to elements in the middle or bottom of the stack is needed.
- **Fixed Size in Array Implementation:** In an array-based stack, the size must be predefined. If the stack grows beyond the array size, resizing or reallocation is required, which can lead to inefficiencies. Alternatively, the stack might overflow if not enough memory is allocated initially.
- **No Random Access:** Unlike arrays, stacks do not support random access to elements, which can be a drawback in cases where non-sequential access is required.
- **Overflow and Underflow:** In array-based stack implementations, stack overflow occurs when more elements are pushed than the predefined size allows. Stack underflow happens when pop operations are attempted on an empty stack.

## Stack Implementations

### 1. Stack Implementation Using Array

**Description:**

In this implementation, a stack is manually managed using an array. We use a pointer called `top` to keep track of the index of the last element inserted into the stack. The stack supports the following operations:
- `Push`: Adds an element to the top of the stack.
- `Pop`: Removes the top element from the stack.
- `Peek`: Returns the top element without removing it.
- `isFull` and `isEmpty`: Checks if the stack is full or empty.

**Algorithm:**

1. **Push Operation:**
   - Check if the stack is full by checking if `top == size - 1`.
   - If not full, increment `top` and insert the new element at `arr[top]`.

2. **Pop Operation:**
   - Check if the stack is empty by checking if `top == -1`.
   - If not empty, remove the element at `arr[top]` and decrement `top`.

3. **Peek Operation:**
   - Check if the stack is empty.
   - If not empty, return the element at `arr[top]`.

4. **isFull/isEmpty Operation:**
   - `isFull`: Returns true if `top == size - 1`.
   - `isEmpty`: Returns true if `top == -1`.

**Time Complexity:**
- Push: O(1)
- Pop: O(1)
- Peek: O(1)

### 2. Stack Implementation Using C++ STL

**Description:**

The C++ Standard Template Library (STL) provides a built-in `stack` class, which makes implementing a stack much simpler and safer. This implementation handles all memory management internally, offering easy-to-use functions to manipulate the stack. The `stack` class supports the following operations:
- `push`: Adds an element to the top of the stack.
- `pop`: Removes the top element.
- `top`: Returns the top element.
- `empty`: Checks if the stack is empty.

**Algorithm:**

1. **Push Operation (push):**
   - Use `st.push(value)` to insert an element at the top of the stack.

2. **Pop Operation (pop):**
   - Use `st.pop()` to remove the top element from the stack.

3. **Access Top Element (top):**
   - Use `st.top()` to retrieve the element at the top of the stack without removing it.

4. **Check If Stack is Empty:**
   - Use `st.empty()` to check if the stack has no elements.

**Time Complexity:**
- Push: O(1)
- Pop: O(1)
- Top: O(1)
