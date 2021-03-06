 [剑指 Offer 03. 数组中重复的数字](https://leetcode-cn.com/problems/shu-zu-zhong-zhong-fu-de-shu-zi-lcof/)
找出数组中重复的数字。

在一个长度为 n 的数组 nums 里的所有数字都在 0～n-1 的范围内。数组中某些数字是重复的，但不知道有几个数字重复了，也不知道每个数字重复了几次。请找出数组中任意一个重复的数字。

**示例 1：**

```
输入：
[2, 3, 1, 0, 2, 5, 3]
输出：2 或 3 
```

```python
# Python版本
class Solution:
    def findRepeatNumber(self, nums: List[int]) -> int:
        dic = set()
        for num in nums: # 遍历数组，
            if num in dic: return num # 在集合直接返回  如果找所有的，用个list存放
            dic.add(num)
        return -1
```

##### 复杂性分析

###### 时间复杂度：O(n)。

遍历数组一遍。使用哈希集合（HashSet），添加元素的时间复杂度为O(1)，故总的时间复杂度是 O(n)。

###### 空间复杂度：O(n)。不重复的每个元素都可能存入集合，因此占用 O(n) 额外空间。

