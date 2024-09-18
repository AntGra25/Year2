# Quiz 083

## 1. Trace Table

![Quiz083C](https://github.com/user-attachments/assets/5bcdb606-47cd-4244-bb37-734d6c8acce7)

## 2. Solution

```.py
def N(X):
    if len(X) == 1:
        return X[0]
    if len(X) == 0:
        return 0

    M = len(X) // 2
    L = N(X[:M])
    R = N(X[M:])
    return L + R
```

## 3. Proof of Work

<img width="209" alt="Quiz083" src="https://github.com/user-attachments/assets/f970c9b4-cd61-422f-84cf-532f8f5cf700">
