---
title: leetcode-array
date: 2022-01-05 18:48:37
tags:
- leetcode
categories:
- [Coding]
---



### 二分法

#### 寻找第一个大于等于目标值的数

- 默认升序
- 如果没有找到，假象值会导致索引越界（因为升序，所以在长度以外）
- frt 靠近 lst，向下取整可以避免数组越界

```python
frt, lst = 0, len(nums)
while frt < lst:
    mid = frt + (lst - frt) // 2
    if target > nums[mid]:
        frt = mid + 1
    else:
        lst = mid
    return frt
```

#### 寻找最后一个小于等于目标值的数

- 默认升序
- 如果没有找到，假象值会导致索引越界（因为升序，所以在索引-1的位置）
- lst靠近 frt，向上取整可以避免数组越界

```python
frt, lst = -1, len(nums) - 1
while frt < lst:
    mid = frt + (lst - frt + 1) // 2
    if target >= nums[mid]:
        frt = mid
    else:
        lst = mid - 1
    return lst
```

### 练习模板

#### [35. 搜索插入位置](https://leetcode-cn.com/problems/search-insert-position/)

#### [34. 在排序数组中查找元素的第一个和最后一个位置](https://leetcode-cn.com/problems/find-first-and-last-position-of-element-in-sorted-array/)



