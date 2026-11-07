# Test Bank: Part 1 questions

> **Author:** Derren Manuel Natalis · **Checked by:** Kenzie, with Claude · **Chapters covered:** 1.1 to 1.5

## Part A: True / False

**TF1** [1.1] An algorithm must always stop after a finite number of steps.

**TF2** [1.2] In a flowchart, a decision (diamond) can have three arrows coming out of it.

**TF3** [1.2] A computer can run pseudocode directly, without turning it into a program first.

**TF4** [1.3] Binary search works on any list, whether it is sorted or not.

**TF5** [1.4] After the first full pass of bubble sort, the largest item is in its final place at the end of the list.

**TF6** [1.4] In the card-sorting activity with 7, 3, 9, 2, 5, selection sort needed fewer swaps than bubble sort.

**TF7** [1.5] A recursive function without a base case will eventually stop by itself.

## Part B: Multiple choice

**MC1** [1.1] Choose ONE. Which instruction breaks **definiteness** (each step must have only one meaning)?
A. Add 5 to x.  B. Wait 3 minutes.  C. Add some salt.  D. Return the largest number.

**MC2** [1.2] Choose ONE. In the morning routine activity, a flowchart has two decisions, one after the other: "Is it raining?" and then "Do I have time?". How many different paths go from Start to End?
A. 2  B. 3  C. 4  D. 6

**MC3** [1.2] Choose ONE. You trace FIND-MAX on the list `4, 9, 2, 7`. How many times is the step `max ← A[i]` carried out?
A. 0  B. 1  C. 2  D. 3

**MC4** [1.3] Choose ONE. You use binary search to find 23 in the sorted list `3, 8, 12, 15, 23, 31, 40` (positions 1 to 7, mid rounded down). How many items do you check?
A. 1  B. 2  C. 3  D. 5

**MC5** [1.4] Choose ONE. What is the list after the **first** full pass of bubble sort on `6, 2, 8, 1`?
A. `2, 6, 8, 1`  B. `2, 6, 1, 8`  C. `1, 2, 6, 8`  D. `2, 1, 6, 8`

**MC6** [1.4] Choose ONE. Which method needs the fewest comparisons to sort the list `1, 2, 3, 4, 5`, which is already sorted?
A. Bubble sort  B. Selection sort  C. Insertion sort  D. All three need the same number

**MC7** [1.5] Choose ALL that apply. What does a correct recursive function need?
A. A base case where it stops calling itself
B. A recursive call with a smaller input
C. A `for` loop
D. A call stack that the programmer writes by hand

## Part C: Open-ended

**OQ1** [1.3, 1.4] A school library keeps a list of 5,000 books in random order. Students search the list many times every day. The librarian asks: "Should I sort the list once and then use binary search, or just keep using linear search on the unsorted list?" Give your advice. Use numbers of checks to support it, explain what sorting costs, and say which sorting method you would use when new books are added one at a time to the list after it has been sorted.

**OQ2** [1.5, 1.1] A student writes this function and tests it with `COUNTDOWN(3)`. It works. Then the program crashes when it is called with `COUNTDOWN(-2)`.

```
COUNTDOWN(n)
    if n = 0
        print "Liftoff!"
    else
        print n
        COUNTDOWN(n - 1)
```

Explain why it crashes, using the call stack. Compare what `COUNTDOWN-LOOP(-2)` (which uses `while n > 0`) would do. Then fix the recursive version and explain which property of an algorithm from Chapter 1.1 the fix protects.

---

## Answer key

### True / False

| Q | Answer | Explanation (if false: give the correct statement) |
|---|---|---|
| TF1 | True | Finiteness is one of the five properties of an algorithm (Chapter 1.1). A procedure that runs forever is not an algorithm. |
| TF2 | False | A decision is a yes/no question, so a diamond always has exactly two arrows out: Yes and No (Chapter 1.2, rule 3). |
| TF3 | False | Pseudocode is written for people. A programmer must turn it into a program in a real programming language before a computer can run it (Chapter 1.2). |
| TF4 | False | Binary search only works on a sorted list. It throws away the half where the target cannot be, which is only safe if the list is in order (Chapter 1.3). |
| TF5 | True | Each pass carries the biggest unsorted item to the end, where it stays. That is why each later pass can stop one place earlier (Chapter 1.4). |
| TF6 | True | Selection sort needed 2 swaps, bubble sort needed 6. Selection sort swaps at most once per pass (Chapter 1.4, activity sample answer). |
| TF7 | False | Without a base case, the function keeps calling itself, the call stack keeps growing, and the program crashes with a stack overflow (Chapter 1.5). |

### Multiple choice

| Q | Answer | Why it is right, and why the others are wrong |
|---|---|---|
| MC1 | C | "Some salt" can mean different amounts to different people, so the step has more than one meaning. A, B and D each have exactly one meaning. |
| MC2 | C | Each decision has 2 answers, and the two decisions come one after the other, so 2 × 2 = 4 paths. A counts only one decision; B and D are not possible with two yes/no questions in a row. |
| MC3 | B | max starts as 4. Is 9 > 4? Yes, max becomes 9 (once). Is 2 > 9? No. Is 7 > 9? No. So the step runs 1 time. A forgets the replacement by 9; D counts every check instead of every replacement. |
| MC4 | C | Check 1: mid = (1 + 7) ÷ 2 = 4, item 15. 23 > 15, so low = 5. Check 2: mid = (5 + 7) ÷ 2 = 6, item 31. 23 < 31, so high = 5. Check 3: mid = 5, item 23, found. D (5 checks) is what linear search would need. |
| MC5 | B | (6, 2) swap: 2, 6, 8, 1. (6, 8) no swap. (8, 1) swap: 2, 6, 1, 8. A stops too early; C is the fully sorted list; D is the list after the **second** pass. |
| MC6 | C | Insertion sort stops each round after 1 comparison when the list is already sorted: 4 comparisons in total. Bubble sort and selection sort still make 4 + 3 + 2 + 1 = 10, so D is wrong. |
| MC7 | A and B | A recursive function needs a base case and a recursive case that moves closer to it. A `for` loop is not needed (C). The computer manages the call stack by itself (D). |

### Open-ended: expected key points

| Q | Key points a good answer includes | Other valid answers |
|---|---|---|
| OQ1 | **Linear search** on 5,000 unsorted books needs up to 5,000 checks per search (worst case: last or missing). **Binary search** needs at most 13 checks, because halving 5,000 about 13 times leaves 1 item. But binary search **only works on a sorted list** (Chapter 1.3). **Sorting costs work once:** for example, bubble sort on 5,000 items makes 4,999 + 4,998 + ... + 1 = 12,497,500 comparisons. Because students search **many times every day**, the time saved on every search soon outweighs the one-time sorting cost, so the advice is: sort once, then use binary search. When new books are added **one at a time** to a list that is already sorted, use **insertion sort**: every old book stops after 1 comparison and only the new book slides into place (Chapter 1.4). | Choosing selection sort for the first sort is fine if justified (fewest swaps). An answer that keeps linear search can earn partial credit only if it argues that searches are very rare, which is not the case here. Exact numbers may be rounded if the reasoning is shown. |
| OQ2 | The base case only checks `n = 0`. With n = −2 the calls are COUNTDOWN(−2), (−3), (−4), ... n only gets smaller, so it **never reaches 0** and the base case never runs. Each call waits for the next one, so the **call stack keeps growing** until the computer runs out of space: a **stack overflow** crash. `COUNTDOWN-LOOP(-2)` checks `while n > 0`. −2 > 0 is No, so the loop body never runs: it prints only "Liftoff!" and stops safely. **Fix:** change the base case to `if n ≤ 0`, so it catches every input that should stop. This protects **finiteness** (Chapter 1.1): the algorithm must stop after a finite number of steps for every input. | An answer that also adds a check like "if n < 0, print an error" is valid. Mentioning that the student only tested one input (n = 3) and should test edge cases such as 0 and negative numbers is a strong extra point. |
