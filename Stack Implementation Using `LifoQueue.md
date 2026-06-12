# Stack Implementation Using `LifoQueue` (Max Size 7) 🔄

This Python program demonstrates a stack implemented using the `LifoQueue` class from the `queue` module. It allows up to 7 elements, checks if the stack is full, and then prints the elements in reverse (LIFO) order.

## 🎯 Aim

To create a Python program that:
- Implements a stack using `LifoQueue` with a maximum size of 7
- Adds user-inputted values to the stack
- Checks whether the stack is full
- Prints the stack elements in reverse order (LIFO)

## 📋 Algorithm

1. Import the `LifoQueue` class from the `queue` module.
2. Create a stack with a maximum size of 7.
3. Read the number of elements (`n`) to be added to the stack.
4. Loop `n` times:
   - Read a value from the user.
   - Use `put()` to push it onto the stack if it's not full.
5. Use `full()` to check if the stack is full and print the result.
6. Use `get()` repeatedly to pop and print elements in reverse order.

## Program:
```python
from queue import LifoQueue

stack = LifoQueue(maxsize=7)

n = int(input("Enter number of elements: "))

for i in range(n):
    x = input("Enter value: ")
    if not stack.full():
        stack.put(x)

print("Stack Full:", stack.full())

print("Stack Elements (LIFO Order):")
while not stack.empty():
    print(stack.get())
```

## Output:
<img width="516" height="434" alt="image" src="https://github.com/user-attachments/assets/e4d8a23b-f100-4808-a8b0-103b4570f5ac" />


## Result:
Thus,the program is executed successfully.
