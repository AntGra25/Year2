# Quiz 080

## 1. Trace Table

![Quiz080C](https://github.com/user-attachments/assets/f06fbef2-a540-4c53-9761-89ecb1adde1b)


## 2. Solution

```.py
def F(N):
    if len(N) == 1:
        return N[0]
    else:
        M = F(N[1:])
        if N[0] > M:
            return N[0]
        else:
            return M
```

## 3. Proof of Work

<img width="215" alt="Quiz080" src="https://github.com/user-attachments/assets/0b8d7372-c571-4279-b055-4f4b7259df80">
