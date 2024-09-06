# Quiz073

## 1. Solution
```.py
def error_check(binary):
    error = False
    first = binary[0]
    count = 0
    for num in binary[1:]:
        if num == '1':
            count += 1
    if count % 2 == int(first):
        error = True
    return error


num = '10010'  # edit this string to try different binary numbers
if error_check(num):
    print('Error detected')
else:
    print('No error detected')

```


## 2. Proof of Work

<img width="425" alt="Quiz073" src="https://github.com/user-attachments/assets/9dc19fd0-d10f-43d9-8df8-ba7faf04ebbd">
