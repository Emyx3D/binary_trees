# This README file is for the 0x1D. C - Binary trees Project

This is a group project in which we learned the details, advantages, and disadvantages of using trees as data structures.

We learned how to qualify trees as well as how to traverse them.

Throughout the project, we implemented binary, binary search, AVL, and Max Binary Heap trees.

## Tests

•   tests: Folder of test files for all tasks. Provided by ALX.

## Helper File

•   binary_tree_print.c: C function that prints binary trees in a pretty way.

## Header File

•   binary_trees.h: Header file containing definitions and prototypes for all types and functions written for the project.

## Data Structures

struct binary_tree_s

{
    int n;

    struct binary_tree_s *parent;

    struct binary_tree_s*left;

    struct binary_tree_s *right;

};

typedef struct binary_tree_s binary_tree_t;

typedef struct binary_tree_s bst_t;

typedef struct binary_tree_s avl_t;

typedef struct binary_tree_s heap_t;

## Function Prototypes

| File                           | Prototype                                                                                      |
| ------------------------------ | ---------------------------------------------------------------------------------------------- |
| binary_tree_print.c            | void binary_tree_print(const binary_tree_t *tree)                                              |
| 0-binary_tree_node.c           | binary_tree_t *binary_tree_node(binary_tree_t *parent, int value);                             |
| 1-binary_tree_insert_left.c    | binary_tree_t *binary_tree_insert_left(binary_tree_t *parent, int value);                      |
| 2-binary_tree_insert_right.c   | binary_tree_t *binary_tree_insert_right(binary_tree_t *parent, int value);                     |
| 3-binary_tree_delete.c         | void binary_tree_delete(binary_tree_t *tree);                                                  |
| 4-binary_tree_is_leaf.c        | int binary_tree_is_leaf(const binary_tree_t *node);                                            |
| 5-binary_tree_is_root.c        | int binary_tree_is_root(const binary_tree_t *node);                                            |
| 6-binary_tree_preorder.c       | void binary_tree_preorder(const binary_tree_t *tree, void (*func)(int));                       |
| 7-binary_tree_inorder.c        | void binary_tree_inorder(const binary_tree_t *tree, void (*func)(int));                        |
| 8-binary_tree_postorder.c      | void binary_tree_postorder(const binary_tree_t *tree, void (*func)(int));                      |
| 9-binary_tree_height.c         | size_t binary_tree_height(const binary_tree_t *tree);                                          |
| 10-binary_tree_depth.c         | size_t binary_tree_depth(const binary_tree_t *tree);                                           |
| 11-binary_tree_size.c          | size_t binary_tree_size(const binary_tree_t *tree);                                            |
| 12-binary_tree_leaves.c        | size_t binary_tree_leaves(const binary_tree_t *tree);                                          |
| 13-binary_tree_nodes.c         | size_t binary_tree_nodes(const binary_tree_t *tree);                                           |
| 14-binary_tree_balance.c       | int binary_tree_balance(const binary_tree_t *tree);                                            |
| 15-binary_tree_is_full.c       | int binary_tree_is_full(const binary_tree_t *tree);                                            |
| 16-binary_tree_is_perfect.c    | int binary_tree_is_perfect(const binary_tree_t *tree);                                         |
| 17-binary_tree_sibling.c       | binary_tree_t *binary_tree_sibling(binary_tree_t *node);                                       |
| 18-binary_tree_uncle.c         | binary_tree_t *binary_tree_uncle(binary_tree_t *node);                                         |
| 100-binary_trees_ancestor.c    | binary_tree_t *binary_trees_ancestor(const binary_tree_t *first, const binary_tree_t *second); |
| 101-binary_tree_levelorder.c   | void binary_tree_levelorder(const binary_tree_t *tree, void (*func)(int));                     |
| 102-binary_tree_is_complete.c  | int binary_tree_is_complete(const binary_tree_t *tree);                                        |
| 103-binary_tree_rotate_left.c  | binary_tree_t *binary_tree_rotate_left(binary_tree_t *tree);                                   |
| 104-binary_tree_rotate_right.c | binary_tree_t *binary_tree_rotate_right(binary_tree_t *tree);                                  |
| 110-binary_tree_is_bst.c       | int binary_tree_is_bst(const binary_tree_t *tree);                                             |
| 111-bst_insert.c               | bst_t *bst_insert(bst_t **tree, int value);                                                    |
| 112-array_to_bst.c             | bst_t *array_to_bst(int *array, size_t size);                                                  |
| 113-bst_search.c               | bst_t *bst_search(const bst_t *tree, int value);                                               |
| 114-bst_remove.c               | bst_t *bst_remove(bst_t *root, int value);                                                     |
| 120-binary_tree_is_avl.c       | int binary_tree_is_avl(const binary_tree_t *tree);                                             |
| 121-avl_insert.c               | avl_t *avl_insert(avl_t **tree, int value);                                                    |
| 122-array_to_avl.c             | avl_t *array_to_avl(int *array, size_t size);                                                  |

## Project Tasks

```0. New node```

o   0-binary_tree_node.c: C function that creates a binary tree node with a given parent and value.

o   Returns a pointer to the new node, or NULL on failure.

```1. Insert left```

o   1-binary_tree_insert: C function that inserts a node as the left-child of another.

o   Returns a pointer to the new node, or NULL on failure.

o   If the given parent already contains a left node, the new node takes its place and the old left-child becomes the left-child of the new node.

```2. Insert right```

o   2-binary_tree_insert_right.c: C function that inserts a node as the right-child of another.

o   Returns a pointer to the new node, or NULL on failure.

o   If the given parent already contains a right node, the new node takes its place and the old right-child becomes the right-child of the new node.

```3. Delete```

o   3-binary_tree_delete.c: C function that deletes an entire binary tree.

```4. Is leaf```

o   4-binary_tree_is_leaf.c: C function that checks if a given node is a leaf.

o   Returns 1 if the node is a leaf, 0 otherwise.

```5. Is root```

o   5-binary_tree_is_root.c: C function that checks if a given node is a root.

o   Returns 1 if the node is a root, 0 otherwise.

```6. Pre-order traversal```

o   6-binary_tree_preorder.c: C function that traverses a tree using pre-order traversal.

```7. In-order traversal```

o   7-binary_tree_inorder.c: C function that traverses a tree using in-order traversal.

```8. Post-order traversal```

o   8-binary_tree_postorder.c: C function that traverses a tree using post-order traversal.

```9. Height```

o   9-binary_tree_height.c: C function that returns the height of a binary tree.

```10. Depth```

o   10-binary_tree_depth.c: C function that returns the depth of a given node in a binary tree.

```11. Size```

o   11-binary_tree_size.c: C function that returns the size of a binary tree.

```12. Leaves```

o   12-binary_tree_leaves.c: C function that returns the number of leaves in a binary tree.

```13. Nodes```

o   13-binary_tree_nodes.c: C function that returns the number of nodes in a binary tree with at least one child.

```14. Balance factor```

o   14-binary_tree_balance.c: C function that returns the balance factor of a binary tree.

```15. Is full```

o   15-binary_tree_is_full.c: C function that checks if a binary tree is full.

o   Returns 1 if a tree is full, 0 otherwise.

```16. Is perfect```

o   16-binary_tree_is_perfect.c: C function that checks if a binary tree is perfect.

o   Returns 1 if a tree is perfect, 0 otherwise.

```17. Sibling```

o   17-binary_tree_sibling.c: C function that returns a pointer to the sibling of a given node in a binary tree.

o   Returns NULL if no sibling is found.

```18. Uncle```

o   18-binary_tree_uncle.c: C function that returns a pointer to the uncle of a given node in a binary tree.

o   Returns NULL if no uncle is found.

```19. Lowest common ancestor```

o   100-binary_trees_ancestor.c: C function that returns a pointer to the lowest common ancestor node of two given nodes in a binary tree.

o   Returns NULL if no common ancestor is found.

```20. Level-order traversal```

o   101-binary_tree_levelorder.c: C function that traverses a binary tree using level-order traversal.

```21. Is complete```

o   102-binary_tree_is_complete.c: C function that checks if a binary tree is complete.

o   Returns 1 if the tree is complete, 0 otherwise.

```22. Rotate left```

o   103-binary_tree_rotate_left.c: C function that performs a left-rotation on a binary tree.

o   Returns a pointer to the new root node of the tree after rotation.

```23. Rotate right```

o   104-binary_tree_rotate_right.c: C function that performs a right-rotation on a binary tree.

o   Returns a pointer to the new root node of the tree after rotation.

```24. Is BST```

o   110-binary_tree_is_bst.c: C function that checks if a binary tree is a valid binary search tree.

o   Returns 1 if the tree is a valid BST, 0 otherwise.

```25. BST – Insert```

o   111-bst_insert.c: C function that inserts a value into a binary search tree.

o   Returns a pointer to the new node, or NULL on failure.

o   If the tree is NULL, the value becomes the root node.

o   The value is ignored if it is already present in the tree.

```26. BST - Array to BST```

o   112-array_to_bst.c: C function that builds a binary search tree from an array.

o   Returns a pointer to the root node of the created tree, or NULL on failure.

```27. BST – Search```

o   113-bst_search.c: C function that searches for a value in a binary search tree.

o   If the value is matched in the BST, returns a pointer to the matched node.

o   Otherwise, returns NULL.

```28. BST – Remove```

o   114-bst_remove.c: C function that removes a node from a binary search tree.

o   Returns a pointer to the new root node of the tree after deletion.

o   If the node to be deleted has two children, it is replaced with its first in-order successor.

```29. Big O #BST```

o   115-O: Text file containing the average time complexities of binary search tree operations (one answer per line):

       Inserting the value n.

       Removing the node with the value n.

       Searching for a node in a BST of size n.

```30. Is AVL```

o   120-binary_tree_is_avl.c: C function that checks if a binary tree is a valid AVL tree.

o   If the tree is a valid AVL tree, returns 1.

o   Otherwise, returns 0.

```31. AVL – Insert```

o   121-avl_insert.c: C function that inserts a value in an AVL tree.

o   Returns a value to the inserted node, or NULL on failure.

```32. AVL - Array to AVL```

o   122-array_to_avl.c: C function that builds an AVL tree from an array.

o   Returns a pointer to the root node of the created AVL tree, or NULL on failure.

o   Ignores duplicate values.

```35. Big O #AVL Tree```

o   125-O: Text file containing the average time complexities of AVL tree operations (one answer per line):

       Inserting the value n.

       Removing the node with the value n.
    
       Searching for a node in an AVL tree of size n.

```41. Big O #Binary Heap```

o   135-O: Text file containing the average time complexities of binary heap operations (one answer per line):

       Inserting the value n.

       Extracting the root node.

       Searching for a node in a binary heap of size n.

## Authors

* Eseigbe Emmanuel - (https://github.com/Emyx3D)

* Busola Atinsola - (https://github.com/BusolaAM)
