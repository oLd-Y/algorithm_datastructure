---
tags: 
source: LeetCode
type: daily
canvas: 
state: complete
---

[LCP 06. 拿硬币 - 力扣（LeetCode）](https://leetcode.cn/problems/na-ying-bi/description/?envType=daily-question&envId=2023-09-15)
# 方法1：
## 思路
1. 每个堆只有奇数堆的最后一次拿1个，其余次都按2个拿

## Code
```python
class Solution:
    def minCount(self, coins: List[int]) -> int:
        res = 0
        for x in coins:
            res += math.ceil(x  / 2)
        return res
```

## 复杂度

1. 时间复杂度：$O(n)$
2. 空间复杂度：$O(1)$

