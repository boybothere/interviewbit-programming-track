# Problem Statement
You are given an integer array A.

You have to find the number of occurences of each number.

Return an array containing only the occurences with the smallest value's occurence first.

For example, A = [4, 3, 3], you have to return an array [2, 1], where 2 is the number of occurences for element 3, 
and 1 is the number of occurences for element 4. But, 2 comes first because 3 is smaller than 4.



Problem Constraints
1 <= |A| <= 105
1 <= Ai <= 109

# Solution
```c
vector<int> Solution::findOccurences(vector<int> &A) {
    map<int,int> m;
    vector<int> ans;
    for(int i=0;i<A.size();i++){
        m[A[i]]++;
    }
    for(auto it:m){
        ans.push_back(it.second);
    }
    return ans;
}
```


Here we have declared a vector ans to return the occurences of each element, since it is mentioned in non decreasing order we use map in C++

We iterate through the array and keep on incrementing each elements occurrences then we iterate through the map using iterator it and then push it.second i.e number of occurences

# Note In code auto it is short way of writing map<int,int>:: iterator it
