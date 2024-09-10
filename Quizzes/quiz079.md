# Quiz 079

## 1. Solution

```.py
from quiz075 import get_ham_k
from quiz077 import get_ham_equation
from quiz078 import get_ham_template


def calculate_ham_P(msg):
    out_msg = get_ham_template(msg)
    k = get_ham_k(len(msg))
    equations = []
    for i in range(k):
        equations.append(get_ham_equation(k + len(msg), i + 1))
    for equation in equations:
        parity_bit = equation[0]
        bit_sum = 0
        for bit in equation[1:]:
            bit_sum += int(out_msg[bit])
        if bit_sum % 2 == 0:
            out_msg[parity_bit] = '0'
        else:
            out_msg[parity_bit] = '1'

    output = ''
    for i in out_msg:
        output += i
    return output

```

## 2. Proof of Work
<img width="263" alt="Quiz079" src="https://github.com/user-attachments/assets/0f985208-6a5e-432b-a248-914512666f00">
