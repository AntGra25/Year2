# Quiz087

## 1. Paper Work

## 2. Solution

```.py
class Container:
    def __init__(self):
        self.data = [None]

    def get(self):
        return self.data[0]

    def set(self, x):
        self.data[0] = x


class Queue:
    def __init__(self):
        self.queue = []

    def enqueue(self, item):
        c = Container()
        c.set(item)
        self.queue.append(c)

    def isEmpty(self):
        if len(self.queue) == 0:
            return True
        return False

    def dequeue(self):
        if self.isEmpty():
            return None
        out = self.queue[0].get()
        self.queue = self.queue[1:]
        return out
```

## 3. Proof of Work

### Testing code

```.py
import random

q = Queue()
test_list = []

for i in range(10):
    num = random.randint(1, 100)
    q.enqueue(num)
    test_list.append(num)
print(test_list)

for i in range(10):
    print(q.dequeue())
print(q.isEmpty())
```

### Testing result
