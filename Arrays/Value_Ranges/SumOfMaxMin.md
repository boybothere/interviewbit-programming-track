# Problem Description

Given an array A of size N. You need to find the sum of Maximum and Minimum element in the given array.

NOTE: You should make minimum number of comparisons.

Problem Constraints
1 <= N <= 105

-109 <= A[i] <= 109

Input Format
First and only argument is an integer array A of size N.

Output Format
Return an integer denoting the sum Maximum and Minimum element in the given array.

# Solution

```c
int Solution::solve(vector<int> &A) {
    auto maxi=max_element(A.begin(), A.end());
    auto mini=min_element(A.begin(), A.end());
    return *maxi+*mini;
}

```

Here we use 2 iterators maxi and mini inorder to point to the maximum and minimum elements in the array respectively

Since these are iterators we need to dereference them using * inorder to get the values they are pointing to

And then according to the problem statement we just return the sum

## Time Complexity: O(n)
## Space Complexity: O(1)


