# 0. Module Outline: Algorithms, Data Structures & Connectionist AI

> **Part:** 00 Overview · **Author:** Amadeus Kenzie Solihin · **Reviewer:** Antony Wijaya (Content lead)
> **Version:** V1.0 (Stage 1, October 2026)
> **Coverage based on:** course slides *Chap 3 Software & Algorithms* and *Chap 5 Connectionist AI & Big Data* (Foundations of CS & AI, 2024)

---

## Who this module is for

**Intended learners:** first-year university students with no prior computer science or AI background.
No programming is required. Small code examples are optional extras.

**Prerequisites:**

| You need | Why |
|---|---|
| Basic arithmetic (add, compare, divide and round down) | Tracing searches and sorts, computing a neuron's output |
| Reading a simple table | Most worked examples are step-by-step tables |
| The idea of a list of items | Every part works with collections of data |

---

## The learning story

The three parts build on each other:

```
 Part 1: ALGORITHMS            Part 2: DATA STRUCTURES        Part 3: CONNECTIONIST AI
 "How do we solve a      ──►   "How do we organize the  ──►   "What if the computer
  problem step by step?"        data the steps work on?"       learns the steps itself
                                                               from examples?"
```

1. **Algorithms** teach precise, step-by-step thinking (searching, sorting).
2. **Data structures** show that the way data is organized changes which algorithms work well (a sorted list allows binary search; a stack gives "undo").
3. **Connectionist AI** (neural networks) uses both: a network is stored as numbers in data structures, and *training* is an algorithm that adjusts those numbers to reduce mistakes. The difference is that nobody writes the rules by hand; the network learns them from examples.

---

## Learning outcomes

After the whole module, a beginner should be able to:

| # | Outcome | Part |
|---|---|---|
| LO1 | **Explain** what an algorithm is and check whether a procedure has the key properties (finite, unambiguous, has input and output) | 1 |
| LO2 | **Trace** linear search, binary search and a simple sort on a short list, step by step | 1 |
| LO3 | **Compare** two algorithms by counting steps, and say why the faster one is faster | 1 |
| LO4 | **Describe** common data structures (array, linked list, stack, queue, tree, graph) and **choose** one for a simple real situation | 2 |
| LO5 | **Trace** stack (LIFO) and queue (FIFO) operations | 2 |
| LO6 | **Explain** the difference between symbolic AI (hand-written rules) and connectionist AI (learning from examples) | 3 |
| LO7 | **Compute** the output of a single artificial neuron (perceptron) from inputs, weights and a bias | 3 |
| LO8 | **Describe** in plain words how a neural network learns, and name real applications and ethical risks | 3 |

---

## Topics, activities and status

**Status labels:** ✅ checked (reviewed by a teammate) · 📝 drafted · 🔲 outline only · ⬜ not started

### Part 1: Algorithms

| Section | What it covers | Planned example / activity | Owner | Status |
|---|---|---|---|---|
| 1.1 What is an algorithm? | Definition, history (al-Khwarizmi, Euclid), key properties, algorithm vs program | Find-max trace, Euclid's GCD trace, "is this an algorithm?" questions | Derren | 📝 drafted, activity being added |
| 1.2 Representing algorithms | Natural language, pseudocode, flowcharts | Draw a flowchart for a morning routine | TBA | 🔲 |
| 1.3 Searching ⭐ | Linear search, binary search, why binary search needs a sorted list, counting checks | 4 traced examples, "guessing game" activity, 8 questions with answers | Nicholas | 📝 drafted, examples verified, review pending |
| 1.4 Sorting | Bubble, selection, insertion sort; comparing step counts | Sort 5 playing cards by hand with each method | TBA | 🔲 |
| 1.5 Iteration vs recursion | Loops vs a function calling itself | Countdown and factorial traced both ways | TBA | 🔲 |

### Part 2: Data structures

| Section | What it covers | Planned example / activity | Owner | Status |
|---|---|---|---|---|
| 2.1 Arrays and records | Index access, fixed size, records with fields | A class list as an array of student records | TBA | 🔲 |
| 2.2 Linked lists | Nodes and pointers, inserting without shifting | Human chain: students hold the "next" pointer | TBA | 🔲 |
| 2.3 Stacks and queues | LIFO, FIFO, push/pop, enqueue/dequeue, choosing between them | 2 traced examples, operation-tracing activity with answers | Antony | 📝 drafted |
| 2.4 Trees and binary trees | Root, parent, child, leaf; binary search tree | Build a BST from 5 numbers | TBA | 🔲 |
| 2.5 Graphs | Nodes and edges, maps and networks, BFS idea | Find the fewest stops on a small metro map | TBA | 🔲 |

### Part 3: Connectionist AI

| Section | What it covers | Planned example / activity | Owner | Status |
|---|---|---|---|---|
| 3.1 Connectionist vs symbolic AI | Rules written by people vs patterns learned from data | Spam filter: hand-written rules vs learned from examples | TBA | 🔲 |
| 3.2 The perceptron | Inputs, weights, bias, weighted sum, activation | Compute a neuron that decides "go outside?" from weather inputs | Cristo | ✅ checked |
| 3.3 How networks learn | Training data, error (loss), adjusting weights, training vs inference | Adjust one weight by hand to reduce the error | TBA | 🔲 |
| 3.4 Network architectures | Layers (input, hidden, output), feedforward; brief look at CNN, RNN | Label the layers in a diagram | TBA | 🔲 |
| 3.5 Deep learning and applications | Many layers, image recognition, speech, translation, chatbots | Match applications to the input data they use | TBA | 🔲 |
| 3.6 Ethics and challenges | Bias in data, privacy, explainability ("black box") | Discuss: who is responsible when a model is wrong? | TBA | 🔲 |

---

## How the parts connect (cross-links)

| From | To | Link |
|---|---|---|
| 1.3 Searching | 1.4 Sorting | Binary search needs a sorted list, so sorting comes next |
| 1.3 Searching | 2.4 Binary trees | A binary search tree stores data so it can be searched like binary search |
| 2.3 Stacks | 1.5 Recursion | Function calls are tracked on a call stack |
| 2.1 Arrays | 3.2 Perceptron | Inputs and weights are stored as arrays of numbers |
| 1.1 Algorithms | 3.3 How networks learn | Training is itself an algorithm that repeats small corrections |

---

## Development status (V1.0 snapshot)

| Status | Sections |
|---|---|
| ✅ Checked by a reviewer | 1.1, 1.3, 2.3, 3.2 |
| 🔲 Outline only | 1.2, 1.4, 1.5, 2.1, 2.2, 2.4, 2.5, 3.1, 3.3, 3.4, 3.5, 3.6 |

## Known gaps and uncertainties

- **Depth of Part 3:** the course slides list deep learning architectures (CNN, RNN). We plan only a short, non-mathematical introduction for beginners. To confirm with the teacher.
- **Big Data:** the Chap 5 slides pair Connectionist AI with Big Data. Our module title does not include Big Data, so we treat it only as context (why neural networks need lots of data). To confirm.
- **Code:** code examples are optional extras. Learners are not expected to program.
- **Owners "TBA":** sections not developed in V1.0 will be assigned in the Stage 2 task list.
- **Consistent terms:** all sections use the same definition: *an algorithm is a finite, step-by-step set of clear instructions that solves a problem or completes a task.*

## References

- Foundations of CS & AI course slides (2024): *Chap 3 Software & Algorithms*, slides 2 to 3 (topic list for algorithms and data structures).
- Foundations of CS & AI course slides (2024): *Chap 5 Connectionist AI & Big Data Overview*, slide 2 (topic list for connectionist AI).
