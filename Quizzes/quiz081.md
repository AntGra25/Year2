# Quiz 081

## 1. Trace Table

![Quiz081C](https://github.com/user-attachments/assets/b70a5e86-cb11-49de-93a6-f9f8efe18433)

## 2. Solution

```.py
def swap(S: str, i1, i2):
    S = list(S)
    temp = S[i1]
    S[i1] = S[i2]
    S[i2] = temp
    return ''.join(S)


def P(S, k):
    if k == len(S):
        return [S]
    else:
        out = []
        for i in range(len(S)):
            T = swap(S, k, i)
            out.extend(P(T, k + 1))
        return out
```

## 3. Proof of Work

<img width="224" alt="Quiz081" src="https://github.com/user-attachments/assets/e32ba297-42e5-4cc9-b2a9-f5f5ebffdadd">
