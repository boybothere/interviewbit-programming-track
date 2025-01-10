# Move Zeroes
# Intuition
We aim at arriving at the solution that is moving any zeros in the array to the end while shifting the non zero elements to the front of the array maintaining their relative sequence
# Approach
The method used here is that I have traversed the array until I have found the index of the first zero whose value is held by i then looping from j = i+1 to n-1, I can perform the following:
1. If i find a non zero element I will swap it with value at index i since I know that it is a zero at index i so for every non zero element we encounter we swap so in a sequential manner
2. Also j is always moving since it has to be used for comparing, i is incremented only if swapping is performed
That's the beauty of this logic, using pen and paper it can be visualized better

## Code
```c
vector<int> Solution::solve(vector<int> &arr) {
    int n = arr.size();
    int i=0;
    while(i<n && arr[i]!=0) {
        i++;
    }
    for(int j=i+1;j<n;j++){
        if(arr[j]!=0){
            swap(arr[i],arr[j]);
            i++;
        }
    }
    return arr;
}

```

## Time Complexity: O(n)
## Space Complexity: O(1)
