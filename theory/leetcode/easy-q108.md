# Easy 108
------------------------------
## Convert Sorted Array to Binary Search Tree

Given an array where elements are sorted in **ascending order**, convert it to a **height balanced BST**.

A **height-balanced** binary tree is a binary tree in which the depth of the two subtrees of every node never differs by more than one.

Constraints:
* $1 <= nums.length <= 10^4$
* $-10^4 <= nums[i] <= 10^4$
* nums is sorted in a strictly increasing order.

https://leetcode.com/problems/convert-sorted-array-to-binary-search-tree/

------------------------------
### Notes:



### My First Answer:
```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right

class Solution:
    def sortedArrayToBST(self, nums: List[int]) -> Optional[TreeNode]:
        if len(nums) == 0:
            return None
        if len(nums) == 1:
            return TreeNode(val=nums[0])
        i = int(len(nums) / 2)
        cur = TreeNode(nums[i])
        cur.left = self.sortedArrayToBST(nums[:i])
        cur.right = self.sortedArrayToBST(nums[i + 1:])
        
        return cur
```
##### interpret
1. Recursively building the tree by giving left a half of list and right a half of list






