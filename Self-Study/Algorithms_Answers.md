```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```

a) The time complexity for this would be On(n^3) because although it's not the traditional
nested for loop, it still loops n^3 which is the same run time as the triple nested for loop.

```
b)  sum = 0

    for i in range(n):
      i += 1
      for j in range(i + 1, n):
        j += 1
        for k in range(j + 1, n):
          k += 1
          for l in range(k + 1, 10 + k):
            l += 1
            sum += 1
```

b) The time complexity here would be O(n^3) because it's a triple nested for loop that all go 
up to n except the last loop which at only one iteration would be n since k is continuously 
incrementing until it reaches n. 


```
c)  def bunnieEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

c) Time complexity here would be O(n) because it's a linear recursive call and constants can be ignored. 



## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also
that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get
broken if dropped off a floor less than floor _f_. Devise a strategy to
determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the
runtime complexity of your solution.


2) Here we can take the midpoint story of the n-story building and drop one egg to see if it breaks. 
If it does, we can take the next LOWER midpoint story of the building until the egg being dropped 
doesn't break. This process will be repeated until we pin point f. The reverse can also happen. We 
may continuously take the HIGHER midpoint story of the building until the egg breaks pin pointing f.
The time complexity for this is O(logn). This algorithm works like Binary Search.  