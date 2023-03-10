# Find All Numbers Disappeared in an Array

### Solution:

```
class Solution {
public:
    vector<int> findDisappearedNumbers(vector<int>& nums) {
        int n = nums.size();
        int i = 0;
        while(i<n){
            if(nums[i] == i+1 || nums[nums[i] - 1] == nums[i])
                i++;
            else
                swap(nums[i], nums[nums[i]-1]);
        }
        vector<int> result;
        for(int j = 0; j < nums.size(); j++){
            if (nums[j] != j+1)
                result.push_back(j+1);
        }
        return result;
    }
};
```

#### Learnings:

1. How to check the position and number in that position are equal in the ascending order of natural numbers?\
   \
   we need:  position space (1 indexed):  \[1, 2, 3, 4, 5] , nums vector(0 indexed) = \[1, 2, 3, 4, 5]

```
if ( nums[nums[i] - 1] == nums[i])
```
