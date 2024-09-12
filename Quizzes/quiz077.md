# Quiz 077

## 1.  Paper Work

![Quiz077C](https://github.com/user-attachments/assets/c7413925-ac40-4908-8815-a18acff02227)


## 2. Solution

```.py
def get_ham_equation(num, P):  # num is k + n
    output = []
    for i in range(num + 1):
        if i & 2 ** (P - 1):
            output.append(i - 1)
    return output
```

## 3. Proof of Work

<img width="305" alt="Quiz077" src="https://github.com/user-attachments/assets/4dc56279-186c-45b8-96c7-6bd9ea96dd08">
