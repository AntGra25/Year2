# Quiz 078

## 1. Solution

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

## 2. Proof of Work
