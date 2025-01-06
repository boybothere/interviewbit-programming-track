# What is the time complexity of the following code :
## Code:

```c

  int a = 0, i = N;
  while (i > 0) {
      a += i;
      i /= 2;
  }
```
# Solution: 
In the above problem we have initializations which take up constant time, the loop runs till i>0 i.e from N to 1

Next, a+=i -> constant time operation

and i/=2 also being a constant time operation helps us devise the code's time complexity

Suppose N=8

1st iteration, i = 8/2 = 4

2nd iteration, i = 4/2 = 2

3rd iteration, i = 2/2 = 1

4th iteration, i = 1/2 = 0

Loop terminates

It doesn't iterate N times rather log2(N), in this case log2(8) = log2(2^3) = 3 so nea rabout we get the number of iterations

# Hence time complexity is given by O(log2(N))


