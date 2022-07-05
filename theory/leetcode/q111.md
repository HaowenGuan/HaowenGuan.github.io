# Easy Q111

------------------------------
## Minimum Depth of Binary Tree

Given a binary tree, find its minimum depth.

The minimum depth is the number of nodes along the shortest path from the root node down to the nearest leaf node.

Note: A leaf is a node with no children.

Constraints:
* The number of nodes in the tree is in the range [0, 105].
* $-1000 <= Node.val <= 1000$

https://leetcode.com/problems/minimum-depth-of-binary-tree/

------------------------------
### Notes:
Edge cases:
* root is None, return 0
* Only one root, return 1

Mistake I made:
* Forgot the condition of the shortest path has to end at **leaf node**.

Some insights:
1. Philosophically, without traverse through (in general) all nodes, we can't find the shortest path.
2. By the above intuition, this problem's best solution **is always bound by O(n).**

### My first Answer:
```Python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right

class Solution:
    def minDepth(self, root: Optional[TreeNode]) -> int:
        if not root:
            return 0
        l_d = self.minDepth(root.left)
        r_d = self.minDepth(root.right)
        if l_d == 0 and r_d == 0:
            return 1
        if l_d == 0 or r_d == 0:
            return max(l_d, r_d) + 1
        return min(l_d, r_d) + 1
```
### Interpret
1. Recursively traverse through all node, pop the depth from bottom to top.
2. Time complexity: is always O(n). Its garenteed to traverse all nodes.
3. Space complexity: is O(n), worst case will stack n recursions at a same time.


### Best Answer:
```Python
class Solution:
    def minDepth(self, root: Optional[TreeNode]) -> int:
        if not root:
            return 0
        if root.left is None:
            return self.minDepth(root.right) + 1
        if root.right is None:
            return self.minDepth(root.left) + 1
        
        return min(self.minDepth(root.left), self.minDepth(root.right)) + 1
```
### Interpret
1. Basic logic is the same
2. Avoid some redundant function call by if statement






