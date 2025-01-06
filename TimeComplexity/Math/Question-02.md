# What is time complexity of following code :
```c
        int count = 0;
        for (int i = N; i > 0; i /= 2) {
            for (int j = 0; j < i; j++) {
                count += 1;
            }
        }
```
# Solution:
The outer loop's value of i is halved each time so given it iterates N times firstly, it will reduce to N/2 then N/4, N/8 and so on having time complexity O(logn)

The inner loop runs till " i " that is current value of i of outer loop for each iteration so it runs for N then N/2, then N/4 iterations and so on

# So total iterations will N + N/2 + N/4 +... = N(1 + 1/2 + 1/4 + ...) Therefore O(N)
