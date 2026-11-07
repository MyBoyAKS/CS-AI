# Test Bank: Part 3 questions

> **Author:** Amadeus Kenzie Solihin (first draft by Claude) · **To be checked by:** Antony Wijaya · **Chapters covered:** 3.1 to 3.6 (3.5 is merged into 3.4)

## Part A: True / False

**TF1** [3.1] In symbolic AI, people write the rules by hand, while in connectionist AI the system learns patterns from labelled examples.

**TF2** [3.2] In the perceptron from Chapter 3.2, if the total comes to exactly 0, the output is 1.

**TF3** [3.3] In the quiz score example in 3.3.4, a learning rate of 0.5 got close to the best weight faster than a learning rate of 0.1.

**TF4** [3.3] During inference, a model's weights normally stay fixed.

**TF5** [3.4] A network with one hidden layer can compute XOR, even though a single perceptron cannot.

**TF6** [3.6] A model with 97% overall accuracy can still be wrong for one person in five in a smaller group.

**TF7** [3.6] If a chatbot gives a reference with an author, a year and a journal name, the reference must exist.

## Part B: Multiple choice

**MC1** [3.1] Choose ONE. A spam filter has these word scores: free +1, prize +2, today -3. Unknown words count 0, and a total greater than 0 means spam. What does it say about `free prize today`?  
A. Spam, total 3  
B. Not spam, total 0  
C. Spam, total 6  
D. Not spam, total -6

**MC2** [3.2] Choose ONE. A perceptron has w1 = 2, w2 = -3, b = 0. The inputs are x1 = 1, x2 = 1. The output is 1 only if the total is greater than 0. What is the output?  
A. 1, because the total is 5  
B. 0, because the total is -1  
C. 1, because w1 is a positive weight  
D. 0, because the total is -3

**MC3** [3.3] Choose ONE. A perceptron has w1 = 1, w2 = -1, b = 0 and a learning rate of 1. For the example x1 = 1, x2 = 1, the target is 1. After this one example, what are w1, w2 and b?  
A. 1, -1, 0  
B. 2, 0, 0  
C. 2, 0, 1  
D. 0, -2, -1

**MC4** [3.3] Choose ONE. Which model should a team choose for real users?  
A. Training 100%, test 60%  
B. Training 97%, test 71%  
C. Training 88%, test 86%  
D. Training 70%, test 69%

**MC5** [3.4] Choose ONE. A fully connected feedforward network has 3 inputs, two hidden layers of 4 neurons each, and 1 output. How many weights does it have (not counting biases)?  
A. 12  
B. 32  
C. 41  
D. 48

**MC6** [3.4] Choose ALL that apply. Which statements are true?  
A. CNNs use small filters that slide across an image.  
B. RNNs read a sequence one item at a time and carry a memory forward.  
C. Chatbots such as ChatGPT are built on transformers, which use attention.  
D. In a feedforward network, values travel backwards from the output during inference.

**MC7** [3.1] Choose ONE. Which task is the best fit for symbolic AI?  
A. Checking whether a student meets the university's written graduation rules  
B. Recognising handwritten digits in photos  
C. Spotting a kind of tumour that doctors can see but cannot describe in rules  
D. Turning speech into text

## Part C: Open-ended

**OQ1** [3.3, 3.4] A perceptron must learn OR: the targets for (x1, x2) = (0,0), (0,1), (1,0), (1,1) are 0, 1, 1, 1. It starts with w1 = 1, w2 = 0, b = -1 and a learning rate of 1. The output is 1 only if the total is greater than 0, and each change is error × input (just error for the bias).
(a) Work through the examples in this order, showing the total, output, error and weights after each one, until one whole round has no mistakes.
(b) Explain why training can stop at that point.
(c) A classmate says: "So if I run this method long enough, it can learn any rule, including XOR." Is this right? Explain why, and say what must change in the network.
(d) Explain why the learning rate matters by describing what would go wrong if a weight's corrections were much too large.

**OQ2** [3.6] A software company builds a model that screens job applicants for a bank. It trains the model on the bank's past hiring decisions. The software company reports "94% accurate" and removes the "gender" input to show that the model is fair. Later, you find out that:

| Group | Applicants tested | Wrong decisions |
|---|---|---|
| Men | 900 | 36 |
| Women | 100 | 24 |

(a) Show that 94% is correct overall, then work out the accuracy for men and for women.
(b) Explain two reasons why removing the "gender" input may not make the model fair.
(c) Argue who should be responsible if a good applicant is wrongly rejected: the software company that built it, the bank that uses it, or the model itself.
(d) Recommend two specific changes, and explain how each one reduces harm.

---

## Answer key

### True / False
| Q | Answer | Explanation (if false: give the correct statement) |
|---|---|---|
| TF1 | True | This is the main difference between the two approaches (3.1.2). |
| TF2 | False | The Chapter 3.2 rule is "greater than 0". 0 is not greater than 0, so the output is **0** (3.2). |
| TF3 | False | With 0.5, the weight jumped past 4 further and further and never settled. With 0.1, it reached about 3.99 after 2 rounds (3.3.4 Parts B and C). |
| TF4 | True | Weights change in training. In inference the finished model is only used (3.3.6). |
| TF5 | True | The hidden layer creates new facts, such as OR and AND, that the output neuron can combine (3.4.4). |
| TF6 | True | A large group can hide a smaller one. In 3.6.4, overall accuracy is 97.1% but group B is at 80%. |
| TF7 | False | A language model can produce realistic but invented references, and a neat format proves nothing. Look the reference up in a real library or database. In *Mata v. Avianca* (2023), lawyers were fined for citing cases that ChatGPT invented (3.6.2). |

### Multiple choice
| Q | Answer | Why it is right, and why the others are wrong |
|---|---|---|
| MC1 | B | 1 + 2 - 3 = 0, which is not greater than 0, so not spam. A ignores "today". C adds the size of -3 as if it were positive. D subtracts all three. |
| MC2 | B | 2 × 1 + (-3) × 1 + 0 = -1, which is not greater than 0, so the output is 0. A treats the negative weight -3 as +3. C looks at one weight, not the total. D leaves out w1's +2. |
| MC3 | C | Total = 1 - 1 + 0 = 0, so output 0 and error = 1 - 0 = 1. Each weight adds error × input = 1, and the bias adds 1. A makes no update. B forgets the bias. D subtracts when it should add. |
| MC4 | C | It has the best test score, and test data predicts results on new users. A and B have big gaps, which suggests overfitting. D has no gap but a lower test score. |
| MC5 | B | 3 × 4 + 4 × 4 + 4 × 1 = 12 + 16 + 4 = 32. A counts only the first pair of layers. C also adds the 9 biases. D multiplies 3 × 4 × 4. |
| MC6 | A, B and C | A, B and C describe each architecture correctly (3.4.6). D is false: "feedforward" means values only move forward when the model is used. Backpropagation works backwards, but only during training. |
| MC7 | A | The graduation rules are already written down exactly, and the university must be able to explain each decision, so symbolic AI fits (3.1.2, 3.1.8). B, C and D are tasks where people cannot write exact rules but labelled examples exist, so connectionist AI fits better. |

### Open-ended: expected key points
| Q | Key points a good answer includes | Other valid answers |
|---|---|---|
| OQ1 | (a) Round 1: (0,0) total -1, output 0, error 0, no change. (0,1) total -1, output 0, error 1, so w2 = 1, b = 0. (1,0) total 1, output 1, error 0. (1,1) total 2, output 1, error 0. Round 2: totals 0, 1, 1, 2, outputs 0, 1, 1, 1, no mistakes. Final w1 = 1, w2 = 1, b = 0. (b) A whole round had error 0 on every example, so no weight would change if we continued. (c) Not right. A single perceptron can only draw one straight cut, and XOR needs more than one, so it never finds weights that work. It needs a hidden layer, trained with backpropagation. (d) Corrections that are too large jump past the good values, so the loss can grow rather than settle. | Any clear layout of the trace. May use the bubble tea or quiz score example to explain the learning rate, or describe a too-small rate being slow. |
| OQ2 | (a) Wrong 60 of 1,000, so 940 ÷ 1,000 = 94%. Men: 864 ÷ 900 = 96%. Women: 76 ÷ 100 = 76%. (b) Past decisions may already be biased, so the labels carry the bias. Proxies such as hobbies or school can reveal gender. (c) The model cannot be responsible. A strong answer shares responsibility between the software company (data, testing, honest reporting) and the bank (its biased past decisions, checking the model on its own applicants, human oversight) and gives reasons. (d) Any two reasoned changes, such as: report accuracy per group; retrain with better labels and more data on women; a person reviews rejections; give applicants a reason and a way to appeal. | Arguing mainly for one party is fine if it is reasoned. Other fairness measures are fine if explained. |
