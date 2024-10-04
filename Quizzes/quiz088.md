# Quiz088

## 1. Paper Work

## 2. Solution

```.py
from quiz087 import Queue


class Stack:
    def __init__(self):
        self.data = Queue()

    def push(self, value):
        self.data.enqueue(value)

    def pop(self):
        value = None
        temp = Queue()
        while not self.data.isEmpty():
            temp.enqueue(value)
            value = self.data.dequeue()
        self.data = temp
        return value
```

## 3. Proof of Work

### Testing code

```.py
test = Stack()
for elem in ["yellow", "red", "black"]:
    test.push(elem)
out = []
for i in range(4):
    out.append(test.pop())
print(out)
```

### Testing result
