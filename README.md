**Binary Tree**

* A binary tree is a hierarchical data structure where each node has at most two children, referred to as the left child and the right child. The topmost node of the tree is called the root.

1. **Top View:**  The top view of a binary tree consists of the nodes that are visible when you look at the tree directly from above. To determine the top view:
   - Assign each node a horizontal distance (root is at distance 0, left child is -1, right child is +1).
   - For each distinct horizontal distance, store only the first node you encounter.
   - The top view is the collection of these stored nodes.

2. **Bottom View:** Similar to top view, but you store the *last* node encountered at each horizontal distance. This represents the view from the bottom of the tree.

3. **Left View:**  The nodes visible when viewing the tree from the left side. To find the left view:
   - Perform a recursive traversal.
   - At each level, the first node visited is part of the left view.

4. **Right View:**  The nodes visible when viewing the tree from the right side. You can find this with similar logic to the left view, but prioritizing the right child during traversal.

**Algorithms**

* **Level Order Traversal:**  A core technique for many tree view problems. You visit nodes level by level, from left to right. It's often combined with a data structure like a queue to manage the order of visiting nodes.
* **Hashing/Mapping:**  Often used to keep track of the first/last node seen at each horizontal distance to compute top and bottom views.
