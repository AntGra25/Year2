# Quiz 086

## 1. Paper Work

## 2. Solution

```.py
s = [3, 7, 7, 7, 5, 5, 1]
queue = Queue()

loop for i=1 to 8
  count = 0
  loop for j=0 to len(s)+1
    if i==s[j]
      count += 1
    end if
  end loop
  queue.enqueue(count)
end loop
```

```.py
count = Array(max(s))
for i=0 to len(s)-1
  count[s[i]-1] += 1
end loop
```
