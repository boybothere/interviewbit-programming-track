# Time and Space Complexity Analysis
## Code:
```c
int a = 0, b = 0; 
for (i = 0; i < N; i++) {      // Loop1 
    for (j = 0; j < N; j++) {  // Loop2 
        a = a + j; 
    } 
} 
for (k = 0; k < N; k++) {      // Loop3 
    b = b + k; 
} 
```

# Solution:
Here we should note that Loop1 and Loop2 are nested and not independent of each other, while Loop3 is independent of the rest.

## TIME COMPLEXITY: 
1. Loop1 iterates from 0 to N-1 i.e N times and increments by 1
2. Similarly Loop2 iterates from 0 to N-1 i.e N times 
   So combined the inner loop (Loop2) iterates N times for each value of i of Loop1 which ranges from 0 to N-1
   Therefore we get a time complexity of O(N²)
3. Next, Loop3 obviously iterates independently for N times hence has a time complexity of O(N)
4. In Big-O notation, we focus on the dominant term (the one with the highest growth rate) while ignoring smaller terms and constants. Here "O(N) is smaller than O(N²)" illustrated below for better clarity and understanding.

For a detailed visualization of different time complexities, check out this [Big-O Cheat Sheet](https://www.freecodecamp.org/news/big-o-cheat-sheet-time-complexity-chart/).

Therefore after analyzing these 3 loops we jump to the conclusion that we get a time complexity of O(N²) for the following piece of code.

## SPACE COMPLEXITY:
1. Talking about the space consumed we have scalar variables (a, b, i, j) while operations performed in the loops are also of constant time.
   Therefore we get a space complexity of O(1)
