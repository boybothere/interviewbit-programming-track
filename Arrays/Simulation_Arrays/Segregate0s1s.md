# Segregate 0s and 1s in an array
Using the Dutch National Flag algorithm for sorting 2 distinct kind of features

Zeroes.....Unknown Elements.......Ones 

0 to low-1 | low to high | high + 1 to n-1

```c
vector<int> Solution::solve(vector<int> &nums) {
    int low=0,n=nums.size(),high=n-1;
    while(low<=high){
        if(nums[low]==0){
            low++;
        }else{
            swap(nums[low],nums[high]);
            high--;
        }
    }
    return nums;
}

```
## Time Complexity: O(n)

## Space Complexity: O(1)
