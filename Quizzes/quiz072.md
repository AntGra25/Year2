# Quiz 072

## 1. Solution

```.py
DATA = ['Ankara', 'Turkey', 'Tokyo', 'Japan', 'Lisbon', 'Portugal']

size = 0
DATA.resetNext()
WHILE DATA.hasNext()
  DATA.getNext()
  size += 1
END LOOP

CITY = Array(size/2)
CAPITAL = Array(size/2)
count = 0
DATA.resetNext()
WHILE DATA.hasNext()
  CITY[count] = DATA.getNext()
  CAPITAL[count] = DATA.getNext()
  count += 1
```
