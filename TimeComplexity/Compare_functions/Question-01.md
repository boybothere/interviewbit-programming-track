In a competition, four different functions are observed. All the functions use a single for loop and within the for loop, same set of statements are executed.

Consider the following for loops:
```c
  A) for(i = 0; i < n; i++)
 
  B) for(i = 0; i < n; i += 2)
 
  C) for(i = 1; i < n; i *= 2)
 
  D) for(i = n; i > -1; i /= 2)
```
If n is the size of input(positive), which function is the most efficient? In other words, which loop completes the fastest
Solution: Here it is clear that multipying the looping variable by 2 is most efficient and prone to completing the loop faster than the other 3.
Loop 1: Time Complexity :0(n) same as Loop 2

Given then Loop 3 and Loop 4 both have logarithmic time complexities bu Loop 3 executes faster since it is increasing exponentially by powers of 2 while Loop 4 divides by 2 causing it to be slower than Loop 3.
