[LCP 06. 拿硬币 - 力扣（LeetCode）](https://leetcode.cn/problems/na-ying-bi/description/?envType=daily-question&envId=2023-09-15)
# 思路
1. 每个堆只有奇数堆的最后一个拿1个，其余次都按2个拿
```python
class Solution:
    def minCount(self, coins: List[int]) -> int:
        res = 0
        for x in coins:
            res += math.ceil(x  / 2)
        return res
```
