======================
A_1_telephone_hashing
======================
Problem Statement :
Consider telephone book database of N clients. Make use of a hash table implementation to quickly look up cliens telephone number.
Objectives:
To understand concept of Hashing
To understand to find record quickly using hash function.
To understand concept & features of object oriented programming.

Learning Objectives :
To understand concept of hashing.
To understand operations like insert and search record in the database. To understand the collision handling technique.

Learning Outcome :
Learn object oriented Programming features Understand & implement concept of hash table .

Hashing Functions :
A hashing function can be just about anything. How the hashing function is actually coded depends on the situation, but generally the hashing function should return a value based on a key and the size of the array the hashing table is built on. Also, one important thing that is sometimes overlooked is that a hashing function has to return the same value every time it is given the same key.

Basic Operations :
Following are the basic primary operations of a hash table. Search − Searches an element in a hash table.
Insert − inserts an element in a hash table. delete − Deletes an element from a hash table.

Search Operation: 
Whenever an element is to be searched, compute the hash code of the key passed and locate the element using that hash code as index in the array. Use linear probing to get the element ahead if the element is not found at the computed hash code.

Insert Operation :
Whenever an element is to be inserted, compute the hash code of the key passed and locate the index using that hash code as an index in the array. Use linear probing for empty location, if an element is found at the computed hash code.

Delete Operation :
Whenever an element is to be deleted, compute the hash code of the key passed and locate the index using that hash code as an index in the array. Use linear probing to get the element ahead if an element is not found at the computed hash code. When found, store a dummy item there to keep the performance of the hash table intact.

Collisions and Collision Handling :
Problems, of course, arise when we have last names with the same first letter. So "Webster" and "Whitney" would correspond to the same index number, 22. A situation like this when two keys get sent to the same location in the array is called a collision. If you're trying to insert an element, you might find that the space is already filled by a different one.

Conclusion:
In this way we have implemented Hash table for quick lookup using C++.






======================
A_4_Set
======================

Problem Statement:
Implement all the functions of a dictionary (ADT) using hashing.
Data : Set of (key, value) pairs, Keys are mapped to values, Keys must be comparable, Keys must be unique
Standard Operations : Insert (key, value), Find(key), Delete(key)

Objectives:
To understand Dictionary (ADT)
To understand concept of hashing
To understand concept & features like searching using hash function.

Theory:
Dictionary ADT -
Dictionary (map, association list) is a data structure, which is generally an association of unique keys with some values. One may bind a value to a key, delete a key (and naturally an associated value) and lookup for a value by the key. Values are not required to be unique. Simple usage example is an explanatory dictionary. In the example, words are keys and explanations are values.

Dictionary Operations -
Dictionary create()
creates empty dictionary
boolean isEmpty(Dictionary d)
tells whether the dictionary d is empty
put(Dictionary d, Key k, Value v)
associates key k with a value v; if key k already presents in the dictionary old value is replaced by v
Value get(Dictionary d, Key k)
returns a value, associated with key kor null, if dictionary contains no such key
remove(Dictionary d, Key k)
removes key k and associated value
destroy(Dictionary d)
destroys dictionary d

Hashing :
Hashing is a technique to convert a range of key values into a range of indexes of an array. We're going to use modulo operator to get a range of key values. Consider an example of hash table of size 20, and the following items are to be stored. Item are in the (key,value) format.

Basic Operations of hash table :
Following are the basic primary operations of a hash table.
Search − Searches an element in a hash table.
Insert − inserts an element in a hash table.
delete − Deletes an element from a hash table.

DataItem :
Define a data item having some data and key, based on which the search is to be conducted in a hash table.

struct DataItem { int data;
int key;
};
Hash Method
Define a hashing method to compute the hash code of the key of the data item. int hashCode(int key){
return key % SIZE;
}
Search Operation :
Whenever an element is to be searched, compute the hash code of the key passed and locate the element using that hash code as index in the array. Use linear probing to get the element ahead if the element is not found at the computed hash code.
Insert Operation :
Whenever an element is to be inserted, compute the hash code of the key passed and locate the index using that hash code as an index in the array. Use linear probing for empty location, if an element is found at the computed hash code.
Delete Operation :
Whenever an element is to be deleted, compute the hash code of the key passed and locate the index using that hash code as an index in the array. Use linear probing to get the element ahead if an element is not found at the computed hash code. When found, store a dummy item there to keep the performance of the hash table intact.

Software Required : 
Dev C++ compiler- / 64 bit windows
Input : 
No. of. elements with key and value pair.
Output : 
Create dictionary using hash table and search the elements in table.
Conclusion :
This program gives us the knowledge of dictionary(ADT).


======================
B_5_Book
======================
Problem Statement:
A book consists of chapters, chapters consist of sections and sections consist of subsections.
Construct a tree and print the nodes. Find the time and space requirements of your method.
Objectives :
To understand concept of Tree.
To understand to find the record of book which consist of no of chapters,sections and subsections.
To   understand   concept   &   features   of   creating   nodes   in object oriented programming.
Learning Objectives
To understand concept of tree.
To understand operations like insert nodes in tree.

Theory :
A tree is a hierarchical data structure defined as a collection of nodes. Nodes represent value and nodes are connected by edges. A tree has the following properties:

The tree has one node called root. The tree originates from this, and hence it does not have any parent.
Each node has one parent only but can have multiple children.
Each node is connected to its children via edge.
A tree is non-linear and a hierarchical data structure consisting of a collection of nodes such that each node of the tree stores a value, a list of references to nodes (the “children”).

Basic Terminology In Tree Data Structure:
Parent Node: The node which is a predecessor of a node is called the parent node of that node. {2} is the parent node of {6, 7}.
Child Node: The node which is the immediate successor of a node is called the child node of that node. Examples: {6, 7} are the child nodes of {2}.
Root Node: The topmost node of a tree or the node which does not have any parent node is called the root node. {1} is the root node of the tree. A non-empty tree must contain exactly one root node and exactly one path from the root to all other nodes of the tree.
Degree of a Node: The total count of subtrees attached to that node is called the degree of the node. The degree of a leaf node must be 0. The degree of a tree is the maximum degree of a node among all the nodes in the tree. The degree of the node {3} is 3.
Leaf Node or External Node: The nodes which do not have any child nodes are called leaf nodes. {6, 14, 8, 9, 15, 16, 4, 11, 12, 17, 18, 19} are the leaf nodes of the tree.
Ancestor of a Node: Any predecessor nodes on the path of the root to that node are called Ancestors of that node. {1, 2} are the parent nodes of the node {7}
Descendant: Any successor node on the path from the leaf node to that node. {7, 14} are the descendants of the node. {2}.
Sibling: Children of the same parent node are called siblings. {8, 9, 10} are called siblings.
Depth of a node: The count of edges from the root to the node. Depth of node {14} is 3.
Height of a node: The number of edges on the longest path from that node to a leaf. Height of node {3} is 2.
Height of a tree: The height of a tree is the height of the root node i.e the count of edges from the root to the deepest node. The height of the above tree is 3.
Level of a node: The count of edges on the path from the root node to that node. The root node has level 0.
Internal node: A node with at least one child is called Internal Node.
Neighbour of a Node: Parent or child nodes of that node are called neighbors of that node.
Subtree: Any node of the tree along with its descendant.


======================
B_6_BST
======================


Statement:
Beginning with an empty binary search tree, Construct binary search tree by inserting the values in the order given. After constructing a binary tree -
Insert new node
Find number of nodes in longest path from root
Minimum datavalue found in the tree
Change a tree so that the roles of the left and right pointers are swapped at every node
Search a value
Objectives:
To understand concept of binary search tree .
To understand the concept of Insert new node, Find number of nodes,	Minimum datavalue found in the tree
Learning Objectives :
To understand concept of binary search tree
Learning Outcome :
Learn object oriented Programming features
Understand & implement concept of Insert new node, Find number of nodes, Minimum datavalue found in the tree
Theory :
A node in Binary Search tree will be represented as follows:
Declare a structure to represent a node in the binary tree Struct BinTre
Find Height of the tree-
There are two conventions to define height of Binary Tree
Number of nodes on longest path from root to the deepest node.
Number of edges on longest path from root to the deepest node.
In this post, the first convention is followed. For example, height of the below tree is 3.
Recursive method to find height of Binary Tree is discussed here. How to find height without recursion? We can use level order traversal to find height without recursion. The idea is to traverse level by level. Whenever move down to a level, increment height by 1 (height is initialized as 0). Count number of nodes at each level; stop traversing when count of nodes at next level is 0.
Software Required: Dev C++ compiler- / 64 bit windo
Input: node names
Output:
Implement concept of Insert new node, Find number of nodes,	Minimum data value found in the tree
Conclusion: 
Successfully implemented Binary search tree as an ADT using linked list in C++ language.

======================
B_7_ExprTree
======================


Problem Statement:
Construct an expression tree from the given prefix expression eg. +--a*bc/def and traverse it using post order traversal (non recursive) and then delete the entire tree.
Objectives:
To understand concept of expression tree.
To understand the concept of converting the given expression into prefix and postfix order.
To understand concept & features of creating expression tree in object oriented programming.
Theory :
The expression tree is a binary tree in which each internal node corresponds to the operator and each leaf node corresponds to the operand so for example expression tree for 3 + ((5+9)*2) would be:

Evaluating the expression represented by an expression tree:
Let t be the expression tree If t is not null then
If t.value is operand then Return t.value
A = solve(t.left) B = solve(t.right)

// calculate applies operator 't.value'
// on A and B, and returns value Return calculate(A, B, t.value)
Construction of Expression Tree:
Now For constructing an expression tree we use a stack. We loop through input expression and do the following for every character.
If a character is an operand push that into the stack
If a character is an operator pop two values from the stack make them its child and push the current node again.
In the end, the only element of the stack will be the root of an expression tree.
Prefix to Postfix step by step

Scan the given prefix expression from right to left character by character.

If the character is an operand, push it into the stack.

But if the character is an operator, pop the top two values from stack.

Concatenate this operator with these two values (operator+1st top value+2nd top value) to get a new string.
Now push this resulting string back into the stack.

Repeat this process untill the end of prefix expression. Now the value in the stack is the desired postfix expression.
How to convert Postfix to Prefix?

Scan the given postfix expression from left to right character by character.

If the character is an operand, push it into the stack.

But if the character is an operator, pop the top two values from stack.

Concatenate this operator with these two values (operator+2nd top value+1st top value) to get a new string.
Now push this resulting string back into the stack.

Repeat this process untill the end of postfix expression. Now the value in the stack is the desired prefix expression.

Software Required: Dev C++ compiler- / 64 bit windows

Input:
 Expression in prefix order.

Output:Convert the given prefix expression into tree and write the post order traversal (non recursive) and then delete the entire tree.
Conclusion: 
This program gives us the knowledge of create and display expression tree.


======================
C_14_flight
======================


Problem Statement:
There are flight paths between cities. If there is a flight between city A and city B then there is an edge between the cities. The cost of the edge can be the time that flight take to reach city B from A, or the amount of fuel used for the journey. Represent this as a graph. The node can be represented by airport name or name of the city. Use adjacency list representation of the graph or use adjacency matrix representation of the graph.
Check whether the graph is connected or not. Justify the storage representation used

Objectives:

 To understand concept of Graph
Theory
A Graph is a non-linear data structure consisting of nodes and edges. The nodes are sometimes also referred to as vertices and the edges are lines or arcs that connect any two nodes in the graph.

In the above Graph, the set of vertices V = {0,1,2,3,4} and the set of edges E = {01, 12, 23, 34, 04, 14, 13}.
Graphs are used to solve many real-life problems. Graphs are used to represent networks. The networks may include paths in a city or telephone network or circuit network. Graphs are also

used in social networks like linkedIn, Facebook. For example, in Facebook, each person is represented with a vertex(or node). Each node is a structure and contains information like person id, name, gender, locale etc.
The following two are the most commonly used representations of a graph.
Adjacency Matrix
Adjacency List
Adjacency Matrix:
Adjacency Matrix is a 2D array of size V x V where V is the number of vertices in a graph. Let the 2D array be adj[][], a slot adj[i][j] = 1 indicates that there is an edge from vertex i to vertex j. Adjacency matrix for undirected graph is always symmetric. Adjacency Matrix is also used to represent weighted graphs. If adj[i][j] = w, then there is an edge from vertex i to vertex j with weight w.
Adjacency List:
An array of lists is used. The size of the array is equal to the number of vertices. Let the array be an array[]. An entry array[i] represents the list of vertices adjacent to the ith vertex. This representation can also be used to represent a weighted graph. The weights of edges can be represented as lists of pairs. Following is the adjacency list representation of the above graph.

Software Required: Dev C++ compiler- / 64 bit windows
Input: Graph
Output: implement concept of Graph for flight path between two cities.
Conclusion: Successfully implemented graph in C++ language.



======================
C_15_Business
======================

NA
