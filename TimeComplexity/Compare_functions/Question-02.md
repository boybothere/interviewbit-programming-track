# Which of the following is not bounded by O(n^2)?
```c
1. (15^10) * n + 12099
2. n^1.98
3. n^3 / (sqrt(n))
4. (2^20) * n
```
Solution: Now when they say is bounded by O(n^2) I take it as some time complexity less than O(n^2) 
So basically its growth rate can be less than equal to that of O(n^2) and not greater than

In option 1, we can simplify thatterm to O(n)) as per asymptotic notations

In option 2, it is clearly less than n^2, so no issues

In option 3, we get $\frac{n^3}{\sqrt{n}} = n^{3 - \frac{1}{2}} = n^{2.5}$ which is clearly greater than O($n^2$) hence that's our answer

While option 4 is same as O(n)
