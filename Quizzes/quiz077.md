# Quiz 077

## 1.  Paper Work

![Quiz077C](https://github.com/user-attachments/assets/c7413925-ac40-4908-8815-a18acff02227)


## 2. Solution

```.py
def ham_parity(num, P):  # num is k + n
    output = []
    for i in range(num + 1):
        if i & 2 ** (P - 1):
            output.append(i)
    return output
```

## 3. Proof of Work

<img width="253" alt="Quiz077" src="https://github.com/user-attachments/assets/c5f97982-1e76-41b6-84eb-2b188dc034ce">
