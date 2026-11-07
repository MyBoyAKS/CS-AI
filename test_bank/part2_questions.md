# Test Bank: Part 2 questions

> **Author:** Nicholas Chung · **To be checked by:** Antony Wijaya · **Chapters covered:** 2.1 to 2.5

## Part A: True / False

**TF1** [2.1] In an array of length 5, the last element is at index 5.

**TF2** [2.2] When a new node is inserted into the middle of a linked list, no node that is already in the list has to move.

**TF3** [2.3] In a stack, the item that was added first is the first one removed.

**TF4** [2.4] In a binary search tree, the root is always the smallest number in the tree.

**TF5** [2.4] A leaf is a node that has no children.

**TF6** [2.5] In a graph, two nodes are neighbours only if an edge joins them, no matter how close they are drawn on the page.

**TF7** [2.5] Breadth-first search (BFS) uses a stack to decide which node to explore next.

## Part B: Multiple choice

**MC1** [2.1] Choose ONE. The array `scores` from 2.1.5 has a fixed size of 6 and holds `82, 75, 91, 68, 88, _` (`_` is the empty position at index 5). You insert **70** at **index 3**, shifting correctly. What is the array after the insert?  
A. `82, 75, 91, 70, 68, 88`  
B. `82, 75, 70, 91, 68, 88`  
C. `82, 75, 91, 70, 68, _`  
D. `82, 75, 91, 68, 70, 88`

**MC2** [2.2] Choose ONE. A linked list holds `head -> Ayu -> Budi -> Chen -> Dewi -> null`. You want to insert **Bima** after Budi, but you do the two pointer changes in the **wrong order**: first you point Budi at Bima, while Bima's pointer is still null. Now the computer walks the list from the head. Which names does it reach?  
A. `Ayu, Budi, Bima, Chen, Dewi`  
B. `Ayu, Budi, Bima`  
C. `Ayu, Budi, Chen, Dewi`  
D. `Ayu, Budi, Chen, Dewi, Bima`

**MC3** [2.3] Choose ONE. Start with an empty queue. Do `enqueue("A")`, `enqueue("B")`, `dequeue()`, `enqueue("C")`. What is in the queue now, from front to rear?
A. `A, B, C`  B. `B, C`  C. `C, B`  D. `A, C`

**MC4** [2.4] Choose ONE. Insert `45, 20, 60, 30` in this order into an empty binary search tree. Where does 30 end up?
A. Left child of 45  B. Right child of 20  C. Left child of 60  D. Right child of 45

**MC5** [2.4] Choose ONE. In the activity in 2.4.7, you built a tree from `55, 30, 80, 65, 15`. How many checks does it take to find out that **70** is **not** in the tree?
A. 1  B. 2  C. 3  D. 5

**MC6** [2.5] Choose ALL that apply. Look at the graph in 2.5.2 (edges A-B, A-C, B-D, C-D, C-E, D-F, E-F). Which statements are true?
A. The graph has 7 edges.  B. A and F are neighbours.  C. The graph contains a loop (a cycle: a route that comes back to where it started without using any edge twice).  D. The graph is a tree.

**MC7** [2.5] Choose ONE. In the metro activity in 2.5.7, BFS starts at School. Which stations are exactly **2 stops** away from School?
Metro lines (trains go both ways; each track between two stations next to each other on a line is one stop): Red: School, Market, Park, Library, Zoo. Blue: School, Hospital, Bank. Green: Market, Theatre, Bank, Zoo.

A. Bank, Park, Theatre  B. Hospital, Market  C. Library, Zoo  D. Bank, Zoo

## Part C: Open-ended

**OQ1** [2.4] Here are three ways to store the same 5 numbers: `55, 30, 80, 65, 15`.
(a) An unsorted list in the order `55, 30, 80, 65, 15`, searched with linear search.
(b) A binary search tree built by inserting `15, 30, 55, 65, 80` in that order.
(c) A binary search tree built by inserting `55, 30, 80, 65, 15` in that order.
For each one, count the checks needed to find **65**, showing the nodes or items you check. Then explain why (b) and (c) need a different number of checks even though they hold the same numbers. Finally, a class list grows every week as new students join with new IDs. Explain what could go wrong if IDs are always added in increasing order, and why that matters more with 1,000 students than with 5.

**OQ2** [2.5] Your friend says: "BFS is pointless on the metro map in 2.5.7. I always just stay on the Red line." Run BFS from **Park** to **Hospital**. Show the queue after each step, write the route, and count the stops. Then answer your friend: can they stay on the Red line for this trip? When does "stay on one line" make sense, and what does BFS find that your friend's rule does not? Use the times from 2.5.7 (2 minutes per stop, 5 minutes per change) in your answer.

Metro lines (trains go both ways; each track between two stations next to each other on a line is one stop): Red: School, Market, Park, Library, Zoo. Blue: School, Hospital, Bank. Green: Market, Theatre, Bank, Zoo.

---

## Answer key

### True / False
| Q | Answer | Explanation (if false: give the correct statement) |
|---|---|---|
| TF1 | False | The last index is always **length - 1**, so in an array of length 5 the last element is at **index 4**. The indexes are 0, 1, 2, 3, 4, and index 5 is **out of range** (2.1.2, 2.1.6). |
| TF2 | True | Only **two pointers** change: the new node's and the one before it. The nodes already in the list stay where they are in memory (2.2.3, 2.2.4). Moving items to make room is what an **array** does. |
| TF3 | False | A stack is LIFO: the item added **last** is removed first. "First in, first out" describes a **queue**. |
| TF4 | False | The root is the **first** number inserted, whatever its size. In 2.4.4 the root is 40, but 10 is the smallest. |
| TF5 | True | A leaf has no children. It does not have to be on the bottom row. |
| TF6 | True | Only edges count. Where a node is drawn on the page means nothing. |
| TF7 | False | BFS uses a **queue** (FIFO), so it finishes all nodes 1 stop away before any node 2 stops away. |

### Multiple choice
| Q | Answer | Why it is right, and why the others are wrong |
|---|---|---|
| MC1 | A | Index 5 is free. Start from the end: move 88 from index 4 to 5, then 68 from index 3 to 4 (**2 shifts**). Put 70 at index 3 (2.1.3, 2.1.5). B counts from 1, so it puts 70 at index 2. C shifts from the front: 68 is copied over 88, so 88 is lost (the error in 2.1.7 Part B). D puts 70 at index 4, after 68 instead of before it. |
| MC2 | B | Budi now points to Bima, and Bima's pointer is null, so the walk is Ayu, Budi, Bima, then stop. Nothing points to Chen any more, so **Chen and Dewi are lost** (2.2.4 "Watch out", 2.2.6). A is what the correct order gives: point Bima at Chen **first**, then Budi at Bima. C ignores that Budi's pointer was changed. D adds Bima at the end, but a new node goes where the pointers say, not at the end. |
| MC3 | B | After two enqueues: `A, B`. Dequeue removes the front (A): `B`. Enqueue C at the rear: `B, C`. A forgets the dequeue. C has the order reversed. D removes from the wrong end (that would be a stack). |
| MC4 | B | 30 < 45, go left to 20. 30 > 20, go right: empty, so 30 is the right child of 20. A stops after the first comparison. D compares wrongly with 45 (30 is smaller, not bigger). C would need 30 > 45. |
| MC5 | C | 70 > 55, go right to 80. 70 < 80, go left to 65. 70 > 65, go right: empty. 3 checks. B stops at 80 without checking 65. D counts every number (linear search). A only checks the root. |
| MC6 | A and C | A: count the edges: 7. C: A, B, D, C, back to A is a loop (cycle). B is false: no edge joins A and F (the fewest stops between them is 3). D is false: a tree has no loops. |
| MC7 | A | 1 stop from School: Hospital and Market. From Hospital you reach Bank, from Market you reach Park and Theatre: all 2 stops. B is the 1-stop ring. C (Library, Zoo) is 3 stops. D mixes 2 and 3 stops. |

### Open-ended: expected key points
| Q | Key points a good answer includes | Other valid answers |
|---|---|---|
| OQ1 | (a) Linear search: 55, 30, 80, 65: **4 checks**. (b) Tree is one long line to the right (15, 30, 55, 65, 80): checks 15, 30, 55, 65: **4 checks**. (c) Bushy tree with root 55: checks 55, 80, 65: **3 checks**. (b) and (c) differ because **insert order decides the shape** of the tree. Sorted input makes every number go right, so the tree becomes a line and searching it is like linear search. With increasing IDs, the class tree becomes a line: with 5 students the difference is 1 check, but with 1,000 students a search could need up to 1,000 checks instead of about 10 in a bushy tree. | Mentions that a bushy tree throws away about half at each check, like binary search. Suggests adding IDs in a mixed order, or rebuilding the tree to keep it bushy (balanced trees). Any correct check counts with the nodes shown. |
| OQ2 | BFS from Park (neighbours in alphabetical order): take Park, add Library, Market (queue: Library, Market). Take Library, add Zoo (queue: Market, Zoo). Take Market, add School, Theatre (queue: Zoo, School, Theatre). Take Zoo, add Bank (queue: School, Theatre, Bank). Take School, add **Hospital: target, stop**. Route: **Park → Market → School → Hospital, 3 stops**. The friend **cannot** stay on the Red line: Hospital is only on the Blue line, so at least one change is needed. Time: 3 × 2 + 1 × 5 = **11 minutes**. Staying on one line makes sense when it avoids slow changes (School to Zoo: Red line is 8 minutes, the 3-stop BFS route is 11). BFS finds the fewest stops on **any** combination of lines, including trips one line cannot do. | Notes that BFS answers "fewest stops", not "fastest", so both people are answering different questions. Correct queue contents in any clear layout. Mentions the visited list (Market is not added twice, School is not added again). |
