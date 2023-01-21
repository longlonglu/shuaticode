
## 思路
1. This is an easy question
2. Having a `HashMap` to store all visited `num`
3. Once we notice the `HashMap` contains `target` - `num`
4. We then know we find the answer.

___

`Time complexity: O(n)`
`Space complexity: O(n)`

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