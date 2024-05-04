Binary tree search is a search algorithm that finds a target value in a binary search tree (BST). A BST is a data structure that organizes data in a binary tree where:

* Each node has a value and can have at most two child nodes: a left child and a right child.
* The values in the left child are less than the value in the parent node.
* The values in the right child are greater than the value in the parent node.

**Algorithm:**

To perform a binary tree search, we start at the root node and compare the target value to the value in the current node. There are three possible outcomes:

1. **Target value is equal to the current node's value:** We have found the target value and can return it.
2. **Target value is less than the current node's value:** The target value must be in the left subtree, so we move to the left child and repeat the process.
3. **Target value is greater than the current node's value:** The target value must be in the right subtree, so we move to the right child and repeat the process.

We continue this recursive process until we either find the target value or reach a leaf node where the target value cannot be located.

**Steps:**

1. Initialize a pointer to the root node of the BST.
2. While the pointer is not null:
    * If the target value is equal to the value in the current node, return the current node.
    * If the target value is less than the value in the current node, move the pointer to the left child.
    * If the target value is greater than the value in the current node, move the pointer to the right child.
3. If the pointer is null, the target value is not in the tree.

**Example:**

Suppose we have a BST with the following values:

```
        10
      /    \
     5      15
    / \    /  \
   2   7  12   18
```

To search for the value 12, we start at the root node (10) and compare 12 to 10. Since 12 is greater, we move to the right child (15). We compare 12 to 15 and find that it is less, so we move to the left child (12). Since 12 is equal to the value in the current node, we have found the target and can return the node.

**Complexity:**

The time complexity of binary tree search is typically O(log n), where n is the number of nodes in the tree. This is because the algorithm divides the search space in half at each step. However, the worst-case complexity is O(n) when the tree is unbalanced.
