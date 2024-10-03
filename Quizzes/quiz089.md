# Quiz089

## 1. Paper Work

## 2. Solution

```.py
from quiz087 import Stack


class Collection:
    def __init__(self, data: tuple):
        self.data = data
        self.count = 0

    def hasNext(self):
        if self.count < len(self.data):
            return True
        return False

    def getNext(self):
        self.count += 1
        return self.data[self.count-1]

    def resetNext(self):
        self.count = 0


RPN = Collection((5, 2, '+', 25, 16, '-', '*', 3, '/'))
stack = Stack()
while RPN.hasNext():
    value = RPN.getNext()
    while value not in ['+', '-', '*', '/']:
        stack.push(value)
        value = RPN.getNext()
    op2 = stack.pop()
    op1 = stack.pop()
    if value == '+':
        new_val = op1 + op2
        stack.push(new_val)
    if value == '-':
        new_val = op1 - op2
        stack.push(new_val)
    if value == '*':
        new_val = op1 * op2
        stack.push(new_val)
    if value == '/':
        new_val = op1 / op2
        stack.push(new_val)
result = stack.pop()
print(f"The result is: {result}")

```

## 3. Proof of Work

