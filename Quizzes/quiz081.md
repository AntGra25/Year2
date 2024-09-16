# Quiz 081

## 1. Trace Table

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


print(P('AB', 1))

```

## 3. Proof of Work

