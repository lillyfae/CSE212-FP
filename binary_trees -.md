# Binary Trees 

[Back to Welcome Page](https://github.com/lillyfae/CSE212-FP/blob/main/Welcome%20to%20my%20Project!.md)

    Binary trees are like linked lists in the way that they are nodes that are linked. But, with binary 
    
    trees, it is non linear. There is a root or a parent node and this node can be linked to 2 different
    
    nodes which are child nodes, those can then be linked to 2 more node each and so on and so forth. 

     
    
    In a binary search tree the smaller value is always on the left and the bigger value on the right.

     To find a value in a binary tree, it might helo to use recursion, because it will cut the 
     
     information in half and then go through it again and again while it gets smaller and smaller until 
     
     it finds the correct value. The Big O notation is O(log n) because it can rule out a sub tree every
     
    time the code recursively runs through to find a value.

    To understand binary trees better and to see some real life applications of it, here is a video:

[binary search](https://www.youtube.com/watch?v=6ysjqCUv3K4&ab_channel=CSDojo)


 ### Traversing

    We can traverse a BST when we want to display everything, all the data in the tree. A traversal will
    
    visit each node from smallest to largest. We can also traverse the tree from largest to smallest,
     
    but for this example, we will be starting from the smallest. This is a recursive process:

``` if node is not None:
		yield from self._traverse_forward(node.left)
		yield node.data
		yield from self._traverse_forward(node.right)
```

 ### Balancing 

    The AVL algorithm will detect that the tree has become unbalanced. A balanced search tree is one
    
    where the subtrees aren't very different in size. To balance a tree, a node rotation needs to be
    
    preformed. This is where the node that is unbalanced is switched to a different sub tree so that the 
    
    binary can be balanced once more. 


# Example:

![Binary Tree Diagram](https://github.com/lillyfae/CSE212-FP/blob/main/binary_tree.png)

## Student Example:

```
def _traverse_backward(self, node):
        """
        Does a backwards traversal (reverse in-order traversal) through the 
        BST.  If the node that we are given (which is the current
        sub-tree) exists, then we will keep traversing on the right
        side (thus getting the larger numbers first), then we will 
        provide the data in the current node, and finally we will 
        traverse on the left side (thus getting the smaller numbers last).

        This function is intended to be called the first time by 
        the __reversed__ function.        
        """
        yield "???"  # Replace this when you implement your solution
```


[Back to Welcome Page](https://github.com/lillyfae/CSE212-FP/blob/main/Welcome%20to%20my%20Project!.md)