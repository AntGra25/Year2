# Quiz074

## 1. Paper Work

![Quiz074C](https://github.com/user-attachments/assets/7feb5711-030d-4214-8716-803661ba300e)


## 2. Solution
```.py
def error_check2(msg):
    if len(msg) % 3 != 0:
        output = 'Invalid input'
    else:
        out_msg = ""
        len_m = len(msg) // 3
        for i in range(0, len_m):
            m1 = msg[i]
            m2 = msg[i + len_m]
            m3 = msg[i + 2 * len_m]
            if m1 == m2 or m1 == m3:
                out_msg += m1
            else:
                if m1 == '0':
                    out_msg += '1'
                else:
                    out_msg += '0'
        if msg == out_msg*3:
            output = f'No errors detected. Message: {out_msg}'
        else:
            output = f'Error detected. Corrected message: {out_msg}'
    return output


test = '100110111011'
print(error_check2(test))

```

## 3. Proof of Work
<img width="248" alt="Quiz074" src="https://github.com/user-attachments/assets/ca249a2e-4c35-4ee3-acac-b185c9c05b28">
