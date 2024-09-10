# Quiz075

## 1. Solution
```.py
from matplotlib import pyplot as plt


def hamming_efficiency(msg_n):
    k = 1
    while not 2**k >= k + msg_n + 1:
        k += 1
    return msg_n/(k + msg_n)


x = []
y = []
for i in range(1, 1001):
    x.append(i)
    y.append(hamming_efficiency(i))

plt.plot(x, y)
plt.show()


```

## 2. Proof of Work

<img width="475" alt="Quiz075" src="https://github.com/user-attachments/assets/4308d85c-9b84-4d64-b22e-1faf895058f6">
