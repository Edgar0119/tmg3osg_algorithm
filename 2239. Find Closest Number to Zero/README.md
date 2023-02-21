# [2239. Find Closest Number to Zero](https://leetcode.com/problems/find-closest-number-to-zero)


## Description

<p>Given an integer array <code>nums</code> of size <code>n</code>, return <em>the number with the value <strong>closest</strong> to </em><code>0</code><em> in </em><code>nums</code>. If there are multiple answers, return <em>the number with the <strong>largest</strong> value</em>.</p>
<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<pre>
<strong>Input:</strong> nums = [-4,-2,1,4,8]
<strong>Output:</strong> 1
<strong>Explanation:</strong>
The distance from -4 to 0 is |-4| = 4.
The distance from -2 to 0 is |-2| = 2.
The distance from 1 to 0 is |1| = 1.
The distance from 4 to 0 is |4| = 4.
The distance from 8 to 0 is |8| = 8.
Thus, the closest number to 0 in the array is 1.
</pre>

<p><strong class="example">Example 2:</strong></p>

<pre>
<strong>Input:</strong> nums = [2,-1,1]
<strong>Output:</strong> 1
<strong>Explanation:</strong> 1 and -1 are both the closest numbers to 0, so 1 being larger is returned.
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>1 &lt;= n &lt;= 1000</code></li>
	<li><code>-10<sup>5</sup> &lt;= nums[i] &lt;= 10<sup>5</sup></code></li>
</ul>

## Solutions

<!-- tabs:start -->

### **Python3**

```python
class Solution:
    def findClosestNumber(self, nums: List[int]) -> int:
        min_num = nums[0]
        for i in nums:
            tmp = abs(i)
            if tmp < abs(min_num):
                min_num = i
            elif tmp == abs(min_num):
                if i > min_num:
                    min_num = i
        return min_num
```
