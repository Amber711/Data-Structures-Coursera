# Tree
- Tree are used for lots of different things.
- Tree have a key and children.
- Tree walks: DFS(pre-order, in-order, post-order) and BFS.
- When working with a tree, recursive algorithms are common.
- In Computer Science, trees grow down.

### Terminology
Root; Child; Parent; Ancestor; Descendant; Sibling; Leaf(node with no children); Interior node(non-leaf);
Level; Height(maximum depth of subtree node and farthest leaf)

               Fred
            /    |    \
          Kate  Sally  Jim
         /   \
        Sam  Hugh
        
 Sam and Hugh has Height 1, Kate, Sally and Jim has Height 2; Fred has Height 3
 The binary search tree is defined by the fact that it's binary, so that means it has at most two children at each node. And we have the property that at the root node, 
 the value of that root node is greater than or equal to all of the nodes in the left child, and it's less than the nodes in the right child.
 
 ### Definition
 #### Node contains:
 - key
 - children: list of children nodes
 - (optional)parent
 #### For binary tree, node contains:
 - key
 - left
 - right
 - (optional)parent
 
 ### Code
 
 1. Height(tree)
    if tree == nil;
        return 0
    return 1 + Max(Height(tree.left), Height(tree.right))
    
 2. Size(tree)
    if tree == nil;
        return 0
    return 1 + Size(tree.left) + Size(tree.right)

### Walking a Tree

![walking a tree](../imgs/Screen%20Shot%202018-01-31%20at%203.36.42%20PM.png)   

#### Depth-first
1. InOrderTraversal(tree)
2. PreOrderTraversal(tree)   
3. PostOrderTraversal(tree)

#### Breadth-first

LevelTraversal(tree)