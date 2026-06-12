# 🔄 Types of Queue-Circular Queue in Python

This project demonstrates the implementation of a **Circular Queue** in Python. The queue accepts 3 user values, performs enqueue and dequeue operations, and displays the removed values.

---

## 🎯 Aim

To develop a Python program that implements a Circular Queue:
- Accepts 3 values from the user
- Removes the 3 values from the queue
- Displays the removed values

---

## 🧠 Algorithm

1. **Initialize** a circular queue of fixed size (e.g., 5).
2. **Define the following functions**:
   - `enqueue()`: Inserts an element into the queue.
   - `dequeue()`: Removes an element from the queue.
   - `display()`: Shows the queue contents.
3. Accept 3 values from the user using the `enqueue()` method.
4. Remove 3 values using the `dequeue()` method.
5. Print the removed values.

---

## 💻 Program:
```python
size = 5
queue = [None] * size
front = rear = -1

def enqueue(value):
    global front, rear
    if (rear + 1) % size == front:
        print("Queue is Full")
        return

    if front == -1:
        front = rear = 0
    else:
        rear = (rear + 1) % size

    queue[rear] = value

def dequeue():
    global front, rear

    if front == -1:
        print("Queue is Empty")
        return None

    value = queue[front]

    if front == rear:
        front = rear = -1
    else:
        front = (front + 1) % size

    return value

for i in range(3):
    enqueue(input("Enter value: "))

print("Removed Values:")
for i in range(3):
    print(dequeue())
```

### Output:
<img width="466" height="288" alt="image" src="https://github.com/user-attachments/assets/539e7c8f-55d4-41d5-83ac-5e97ce794ca1" />


## Result:
Thus,the program is executed successfully.
