# What is the time complexity of the following code :
```c
        int j = 0;
        for(int i = 0; i < n; ++i) {
            while(j < n && arr[i] < arr[j]) {
                j++;
            }
        }
```

# Solution:
This may seem to look like a O(n^2) time complexity but if we analyse more carefully for each interation of i from 0 to n-1 it is clear that condiition j<n is checked and we just perform j++ so the inner loop runs for same number of times as the outer loop

The critical observation here is that j only increments and does not reset for each iteration of i

# Hence O(n)
