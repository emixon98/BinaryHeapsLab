# BinaryHeapsLab
Week 9 CISC 187 Lab on Binary Heaps
### Task 1: Draw what the following heap would look like after we insert the value 11 into it:

#### Original Heap:
<img width="754" height="508" alt="image" src="https://github.com/user-attachments/assets/07bd8dbc-f386-4bf4-bad0-ae10345464c8" />

#### New Heap: 
![Task1Heap](https://github.com/user-attachments/assets/9a2ae1fa-4527-4544-9ccd-746d2d13d57f)

#### Explanation: 
1. Insert 11 at the next open slot. Looking "left-to-right" the next open slot would be as the right child of 5.
2. Utilize "trickling up" comparing 11 with its parent, the value 5. Since 11 is greater we swap.
3. Compare 11 with its new parent following the swap, the value 9. 11 is greater than 9, we swap again.
4. Compare once again with the new parent, the root node containing the value 10. 11 is greater than 10, 11 is now the new root node. 

### Task 2: Draw what the previous heap would look like after we delete the root node: 
![Task2Heap](https://github.com/user-attachments/assets/e60b03ed-7f94-4e47-ab3e-466f73d811df)

#### Explanation, using the original given heap node:
Due to the phrasing of this task, I assumed we were being asked to take the original heap and delete the root node 10. However, for clarification, if we deleted the root node of the outputted heap from task 1 we would revert back to the original heap, the steps taken would be similar to what will be described below through the assumed path I took, if needed I will add an extra explanation for this other described case.
1. Our first step is to replace the root node with our last node, our furthest "right" node in the bottom row, the value 3. This both overrides and gets rid of our root node, but also allows us to begin trickling "down".
2. We compare 3 with both of its children, the values 9 and 8, swapping 3 with the largest of the two values, in this case 9. 9 becomes our root node and 3 takes the place it was residing.
3. We now compare 3 with its children again, the values 6 and 5, the largest being 6. We now swap 3 and 6.
4. We now compare 3 to its children one last time, the values 2 and 1. 3 is larger than both, and thus has found its final position in the heap following our deletion process.

### Task 3: Imagine you’ve built a brand-new heap by inserting the following numbers into the heap in this particular order: 55, 22, 34, 10, 2, 99, 68. If you then pop them from the heap one at a time and insert the numbers into a new array, in what order would the numbers now appear?

#### Explanation:

Heap sort will produce a sorted list despite the structure of the tree itself. The array order will be [99, 68, 55, 34, 22, 10, 2] if using a max heap.
If we were using a max heap, these values are in descending order, for a min heap they are ascending. The reason being that if we pop a node it needs to be the root node, which is replaced by the last node that then trickles down. We perform this operation for each pop, meaning we get a natural descending order as each next highest value eventually is sorted into the root node.

