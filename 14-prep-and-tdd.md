# Read14 :Trees

### *Trees* 
- The tree is one of the most common data structures in computer science and the natural way to model certain subject areas. 

### *Common Terminology*
- Node - A Tree node is a component which may contain its own values, and references to other nodes.
- Root - The root is the node at the beginning of the tree.
- K - A number that specifies the maximum number of children any node may have in a k-ary tree. In a binary tree, k = 2.
- Left - A reference to one child node, in a binary tree.
- Right - A reference to the other child node, in a binary tree.
- Edge - The edge in a tree is the link between a parent and child node.
- Leaf - A leaf is a node that does not have any children.
- Height - The height of a tree is the number of edges from the root to the furthest leaf.

### *Sample Tree*
![sample tree](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree1.PNG)

### *Traversals*
 Traversing a tree allows us to search for a node, print out the contents of a tree, and much more! There are two categories of traversals when it comes to trees:
- Depth First
- Breadth First

### *Depth first traversal*
- Depth first traversal is where we prioritize going through the depth (height) of the tree first. There are multiple ways to carry out depth first traversal, and each method changes 
the order in which we search/print the root. Here are three methods for depth first traversal:

   * Pre-order: root >> left >> right
   * In-order: left >> root >> right
   * Post-order: left >> right >> root

- The most common way to traverse through a tree is to use recursion.

- Pre-order:
Pre-order means that the root has to be looked at first. In our case, looking at the root just means that we output its value. When we call preOrder for the first time, the root will 
be added to the call stack.

- the pseudocode for this traversal method:
           ALGORITHM preOrder(root)

            OUTPUT <-- root.value

            if root.left is not NULL
           preOrder(root.left)
          
            if root.right is not NULL
          preOrder(root.right)

- In-order:
- the pseudocode for this traversal method:
            ALGORITHM inOrder(root)
            // INPUT <-- root node
            // OUTPUT <-- in-order output of tree node's values

            if root.left is not NULL
           inOrder(root.left)

            OUTPUT <-- root.value

              if root.right is not NULL
                  inOrder(root.right)

- Post-order:
- the pseudocode for this traversal method:
           ALGORITHM postOrder(root)
           // INPUT <-- root node
           // OUTPUT <-- post-order output of tree node's values
           
             if root.left is not NULL
                   postOrder(root.left)
               if root.right is not NULL
                postOrder(root.right)
             OUTPUT <-- root.value
 
### *Breadth First*
- Breadth first traversal iterates through the tree by going through each level of the tree node-by-node. So, given our starting tree one more time:

![breadth tree](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/tree-example.png)

- Our output using breadth first traversal is now:

       Output: A, B, C, D, E, F

- Traditionally, breadth first traversal uses a queue (instead of the call stack via recursion) to traverse the width/breadth of the tree. Let’s break down the process.
- Pseudocode:
             ALGORITHM breadthFirst(root)
             // INPUT  <-- root node
             // OUTPUT <-- front node of queue to console

               Queue breadth <-- new Queue()
               breadth.enqueue(root)

               while ! breadth.is_empty()
                 node front = breadth.dequeue()
                 OUTPUT <-- front.value

                 if front.left is not NULL
                   breadth.enqueue(front.left)

                 if front.right is not NULL
                   breadth.enqueue(front.right)

### *Binary Tree Vs K-ary Trees*
- Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).
- There is no specific sorting order for a binary tree. Nodes can be added into a binary tree wherever space allows. Here is what a binary tree looks like:

![Binary Tree Vs K-ary Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BinaryTree2.PNG)

- K-ary Trees
If Nodes are able have more than 2 child nodes, we call the tree that contains them a K-ary Tree. In this type of tree we use K to refer to the maximum number of children that each 
Node is able to have.
- Breadth First Traversal
Traversing a K-ary tree requires a similar approach to the breadth first traversal. We are still pushing nodes into a queue, but we are now moving down a list of children of length k, 
instead of checking for the presence of a left and a right child.

![K-ary Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/KaryTree1.png)

- If we traversed this tree Breadth First we should see the output:
         Output: A, B, C, D, E, F, G, H
         
- Pseudocode:
            ALGORITHM breadthFirst(root)
            // INPUT  <-- root node
            // OUTPUT <-- front node of queue to console

              Queue breadth <-- new Queue()
              breadth.enqueue(root)

              while ! breadth.is_empty()
                node front = breadth.dequeue()
                OUTPUT <-- front.value

                for child in front.children
                    breadth.enqueue(child)

- Binary Search Trees:
A Binary Search Tree (BST) is a type of tree that does have some structure attached to it. In a BST, nodes are organized in a manner where all values that are smaller than the root are 
placed to the left, and all values that are larger than the root are placed to the right.

Here is how we would change our Binary Tree example into a Binary Search Tree:

![BST](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/images/BST1.PNG)

For more details watch this [Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html).