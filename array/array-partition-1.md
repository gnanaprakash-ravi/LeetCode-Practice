---
description: Easy
---

# Array Partition 1

#### Solution

```
class Solution {
public:
    int arrayPairSum(vector<int>& nums) {
        sort(nums.begin(), nums.end());
        int n = nums.size();
        int ms = 0;
        for(int i = 0; i < n; i+=2)
            ms += nums[i];
        return ms;
    }
};
```
