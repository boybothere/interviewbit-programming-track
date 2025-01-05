# Time and Space Complexity Analysis

### Code Snippet

```cpp
int a = 0, b = 0;    
for (i = 0; i < N; i++) {
    a = a + rand();  
}
for (j = 0; j < M; j++) {
    b = b + rand();
}

# Solution:

IMPORTANT: Firstly, note that the 2 loops are independent of each other, hence evaluated independently.

## TIME COMPLEXITY:

1. The first loop iterates from `i = 0` to `N-1`, i.e. N iterations.
   Each iteration performs a constant-time operation (`a = a + rand()`). Here, `rand()` is a constant-time operation.

2. The second loop iterates from `j = 0` to `M-1`, i.e. M iterations.
   Each iteration also performs a constant-time operation (`b = b + rand()`).

Combined, the loops run `N + M` times. Therefore, Time Complexity is given by O(N + M).

## SPACE COMPLEXITY:

1. Here, `a`, `b`, `i`, and `j` are scalar variables (i.e., similar to primitive data types which can only hold at most single values).

Therefore, its Space Complexity is given by O(1).

