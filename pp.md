# Exam Questions and Answers

## SECTION A [20 MARKS]
(Answer all questions from this section)

1. **Which data structure follows the Last In First Out (LIFO) principle?**
   - b) Stack

2. **Which sorting algorithm has the worst-case time complexity of O(n^2)?**
   - c) Bubble Sort

3. **What is the time complexity of searching in a binary search tree (BST) in the worst-case scenario?**
   - b) O(n)

4. **Which of the following is NOT a type of tree traversal?**
   - d) Height-First Traversal

5. **In which data structure are elements accessed in a First In First Out (FIFO) manner?**
   - b) Queue

6. **What is the worst-case time complexity of the Quick Sort algorithm?**
   - c) O(n^2)

7. **Which of the following is an example of a non-linear data structure?**
   - d) Graph

8. **What is the time complexity of inserting an element into a binary search tree (BST) in the worst-case scenario?**
   - b) O(n)

9. **What is the purpose of the hash function in a hash table?**
   - d) To map keys to array indices

10. **Which of the following is NOT a type of hash function collision resolution technique?**
    - c) Binary Search

11. **In which data structure is data stored in a hierarchical manner?**
    - d) Tree

12. **Which of the following data structures is based on the principle of "First In First Out"?**
    - b) Queue

13. **Which sorting algorithm has the best time complexity in the average case?**
    - a) Quick Sort

14. **What is the time complexity of finding an element in a hash table with a good hash function?**
    - c) O(1)

15. **Which data structure allows for efficient insertion and deletion at both ends?**
    - c) Linked List

16. **What is the primary purpose of using a binary search tree (BST)?**
    - a) To efficiently search for an element

17. **Which algorithm is used for finding the shortest path in a weighted graph?**
    - a) Dijkstra's algorithm

18. **Which of the following is NOT a characteristic of a binary tree?**
    - d) It is a linear data structure

19. **Which data structure is typically used to implement recursion?**
    - a) Stack

20. **What is the primary purpose of dynamic programming?**
    - b) To solve problems by breaking them down into smaller, overlapping subproblems

## SECTION B [60 MARKS]

**Question 1**

a) An algorithm is a step-by-step procedure or formula for solving a problem. Examples of divide-and-conquer algorithms include:
   - Merge Sort
   - Quick Sort

b) Flowchart to compute the nth Fibonacci number:
   ```plaintext
   Start -> Input n -> If n <= 1 -> Output n
                     |
                    else
                     |
                     v
                  f1 = 0, f2 = 1
                     |
                     v
             Repeat until n > 2: fn = f1 + f2; f1 = f2; f2 = fn
                     |
                     v
               Output fn -> End


 Pseudocode for computing the nth Fibonacci number:

Function Fibonacci(n):
   if n <= 1:
      return n
   else:
      f1 = 0
      f2 = 1
      for i from 2 to n:
         fn = f1 + f2
         f1 = f2
         f2 = fn
      return fn
d) Differences between a Brute Force Algorithm and a Greedy Algorithm:

Brute Force Algorithm: Examines all possible solutions to find the best one.
Example: Exhaustive search for the traveling salesman problem.

Greedy Algorithm: Makes the locally optimal choice at each step with the hope of finding a global optimum.
Example: Kruskal's algorithm for finding the minimum spanning tree.


Question 2

a) Time complexity is a measure of the amount of time an algorithm takes to complete as a function of the input size. Examples:

O(1): Accessing an array element by index.
O(n): Linear search in an unsorted array.
O(log n): Binary search in a sorted array.
b) A Binary Search Tree (BST) is a tree structure where each node has at most two children: the left child's value is less than the parent's, and the right child's value is greater. This differs from AVL trees, which maintain balanced heights.

c) Example usage of BSTs: Storing and searching for keys in a database.
Time complexity for BST operations:

Insertion: O(log n) average, O(n) worst-case
Deletion: O(log n) average, O(n) worst-case
Search: O(log n) average, O(n) worst-case
d) Dijkstra's algorithm:

Initialize distances from the source to all vertices as infinite except the source itself (distance 0).
Set the source vertex as the current vertex.
For the current vertex, update the distance to each neighbor if a shorter path is found.
Mark the current vertex as visited.
Repeat with the next unvisited vertex with the smallest distance.


Question 3

a) Performance complexities for a linear search algorithm:

Best case: O(1) (first element is the target).
Worst case: O(n) (target is the last element or not present).
Average case: O(n) (target is somewhere in the middle).
b) Sorting algorithms:

Bubble Sort:
for i from 0 to n-1:
   for j from 0 to n-i-1:
      if arr[j] > arr[j+1]:
         swap arr[j] and arr[j+1]

Insertion Sort
for i from 1 to n-1:
   key = arr[i]
   j = i-1
   while j >= 0 and arr[j] > key:
      arr[j+1] = arr[j]
      j = j-1
   arr[j+1] = key


Selection Sort
for i from 0 to n-1:
   min_idx = i
   for j from i+1 to n:
      if arr[j] < arr[min_idx]:
         min_idx = j
   swap arr[i] and arr[min_idx]

Quick Sort
Function quickSort(arr, low, high):
   if low < high:
      pi = partition(arr, low, high)
      quickSort(arr, low, pi-1)
      quickSort(arr, pi+1, high)
Question 4

a) A linked list is a data structure where nodes contain a value and a reference to the next node. Advantages over arrays include dynamic sizing and easier insertion/deletion.

b) Python function to insert a new node at the beginning:

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

def insert_at_beginning(head, new_data):
    new_node = Node(new_data)
    new_node.next = head
    head = new_node
    return head


c) Deleting a node from a singly linked list given only a pointer to that node:

Copy the data from the next node to the current node.
Point the current node to the next of the next node.
Delete the next node.
d) A stack is a data structure following LIFO. Basic operations include:

Push: Add an element to the top.
Pop: Remove the top element.
Peek: View the top element without removing it.
e) Algorithm to check if a string of parentheses is balanced using a stack:

Initialize an empty stack.
Traverse the string, pushing opening parentheses onto the stack.
For each closing parenthesis, check if it matches the top of the stack.
If it matches, pop the top element.
At the end, if the stack is empty, the string is balanced.