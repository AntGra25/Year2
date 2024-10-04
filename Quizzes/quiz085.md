# Quiz 085

## 1. Trace Table

![Quiz084C](https://github.com/user-attachments/assets/8bb99b28-973a-4739-a1a6-8048ca3b88d8)

## 2. Solution

```.py
def merge_sort(m):
    if len(m) <= 1:
        return m
    n = len(m)//2
    l = merge_sort(m[:n])
    r = merge_sort(m[n:])

    s, i, j = [], 0, 0
    while i < len(l) and j < len(r):
        if l[i] < r[j]:
            s.append(l[i])
            i += 1
        else:
            s.append(r[j])
            j += 1
    return s + l[i:] + r[j:]
```

## 3. Proof of Work

<img width="241" alt="Quiz084" src="https://github.com/user-attachments/assets/35a6b453-7148-454d-8faa-02390ab74b1f">
