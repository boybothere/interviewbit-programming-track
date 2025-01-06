What is the time complexity of the following code :
# Code
```c
int i, j, k = 0;
for (i = n/2; i <= n; i++) {
    for (j = 2; j <= n; j = j * 2) {
         k = k + n/2;
    }
}
```
# Solution:
The outer loops runs for n/2 times given by n-n/2

While the inner loops runs from 2 till j>n and j is multiplied by 2 portraying logarithmic number of iterations for each value of the outer loop

# Therefore, Outer loop : O(n)

# Inner loop : O(logn)

# Since they are nested we compute the time complexity as O(n*logn)
