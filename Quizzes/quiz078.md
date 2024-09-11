# Quiz 078

## 1. Paper Work

![Quiz078C](https://github.com/user-attachments/assets/b04faa1b-b18d-42a9-a75e-08580ab55cd7)


## 2. Solution

```.py
from quiz075 import get_ham_k
from quiz076 import get_ham_position


def get_ham_template(msg) -> list:
    total_msg = []
    msg_k = get_ham_k(len(msg))
    positions = get_ham_position(msg_k)
    msg_i = 0
    for i in range(msg_k + len(msg)):
        total_msg.append(-1)
        if i not in positions:
            total_msg[i] = msg[msg_i]
            msg_i += 1
    return total_msg


```

## 3. Proof of Work
<img width="253" alt="Quiz078" src="https://github.com/user-attachments/assets/aa34f40c-6481-47eb-90f8-a42a67e331a8">
