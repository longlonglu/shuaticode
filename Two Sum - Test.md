<img src=" " width="60%" height="auto"/>

## 思路
1. This is An `Test`
<img src="https://raw.githubusercontent.com/longlonglu/shuatiimage1/main/20.png " width="60%" height="auto"/>

___

`Time complexity: O(n^2)`

`Space complexity: O(n^3)`

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        hash_map = {}
        
        for i in range(len(nums)):
            sub = target - nums[i]
            if (sub in hash_map):
                return [i, hash_map[sub]]
            hash_map[nums[i]] = i 
```