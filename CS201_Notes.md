# CS201 Discrete Math

## Logic and Mathematical Proofs (Logic)

### Propositional Logic

>  Proposition - a declarative sentence that is **either** true or false

- Negation $\neg$ 
- Conjunction (And) $\wedge$ 
- Disjunction (Inclusive Or) $\vee$ 
- Exclusive Or $\oplus$ 
- Conditional Statement (Implication) $\rightarrow$ 
  - if p then q
  - p only if q
- Biconditional $\leftrightarrow$ 
  - p iff q
  - if p then q, and conversely

| p   | $\neg$ p |
|:---:|:--------:|
| T   | F        |
| F   | T        |

| p   | q   | p $\wedge$ q | p $\vee$ q | p $\oplus$ q | p $\rightarrow$ q | p $\leftrightarrow$ q |
|:---:|:---:|:------------:|:----------:|:------------:|:-----------------:|:---------------------:|
| T   | T   | T            | T          | F            | T                 | T                     |
| T   | F   | F            | T          | T            | F                 | F                     |
| F   | T   | F            | T          | T            | T                 | F                     |
| F   | F   | F            | F          | F            | T                 | T                     |

converse of p $\rightarrow$ q is q $\rightarrow$ p

contrapositive of p $\rightarrow$ q is $\neg$ q $\rightarrow$ $\neg$ p

inverse of p $\rightarrow$ q is $\neg$ p $\rightarrow$ $\neg$ q

equivalent == same truth value

Bitwise operations - OR ($\vee$), AND ($\wedge$), XOR ($\oplus$)

### Propositional Equivalence

Tautology - always true
    e.g. p $\vee$ $\neg$ p      (p $\wedge$ q) $\rightarrow$ p

Contradiction - always false
    e.g. p $\wedge$ $\neg$ p

Contingency

    neither a tautology nor a contradiction

logically equivalent denoted by $p \equiv q$ or $p \Leftrightarrow q$ if $p \leftrightarrow q$ is a tautology

    e.g. $p \rightarrow q \equiv \neg q \rightarrow \neg p$ 

***write the names in homework***

- Identity laws
  - p $\wedge$ T $\equiv$ p
  - p $\vee$ F $\equiv$ p
- Domination laws
  - p $\vee$ T $\equiv$ T
  - p $\wedge$ F $\equiv$ F
- Idempotent laws
  - p $\vee$ p $\equiv$ p
  - p $\wedge$ p $\equiv$ p
- Double negation laws
  - $\neg$ ($\neg$ p) $\equiv$ p
- Commutative laws
  - p $\vee$ q $\equiv$ q $\vee$ p
  - p $\wedge$ q $\equiv$ q $\wedge$ q
- Associative laws
  - (p $\vee$ q) $\vee$ r $\equiv$ p $\vee$ (q $\vee$ r)
  - (p $\wedge$ q) $\wedge$ r $\equiv$ p $\wedge$ (q $\wedge$ r)
- Distributive laws
  - p $\vee$ (q $\wedge$ r) $\equiv$ (p $\vee$ q) $\wedge$ (p $\vee$ r)
  - p $\wedge$ (q $\vee$ r) $\equiv$ (p $\wedge$ q) $\vee$ (p $\wedge$ r)
- De Morgan's laws
  - $\neg$ (p $\vee$ q) $\equiv$ $\neg$ p $\wedge$ $\neg$ q
  - $\neg$ (p $\wedge$ q) $\equiv$ $\neg$ p $\vee$ $\neg$ q
- Absorption laws
  - p $\vee$ (p $\wedge$ q) $\equiv$ p
  - p $\wedge$ (p $\vee$ q) $\equiv$ p
- Negation laws
  - p $\vee$ $\neg$ p $\equiv$ T
  - p $\wedge$ $\neg$ p $\equiv$ F
- Useful law
  - p $\rightarrow$ q $\equiv$ $\neg$ p $\vee$ q

### Predicates and Quantifiers

>  Predicate Logic: make statements with variables

>  A predicate is a statement P(x1, x2, ..., xn) that contains n variables x1, x2, ... xn.

>  The domain (universe) D of the predicate variables x1, x2, ... xn is the set of all values that may be substituted in place of the variables.

>  The truth set of P(x1, x2, ..., xn) is the set of all values of the predicate variables (x1, x2, ..., xn) such that the proposition P(x1, x2, ..., xn) is true.

Quantified statements

    Universal quantifier $\forall x P(x)$

    Existential quantifier $\exist x P(x)$

Precedence of proposition and quantifiers: 

| Operators         | Precedence |
| ----------------- | ---------- |
| $\forall \exist$  | 0          |
| $\neg$            | 1          |
| $\wedge$          | 2          |
| $\vee$            | 3          |
| $\rightarrow$     | 4          |
| $\leftrightarrow$ | 5          |

$\neg (\forall x P(x)) \equiv \exist x (\neg P(x))$

$\neg (\exist x P(x)) \equiv \forall x (\neg P(x))$

## Logic and Mathematical Proofs (Mathematical Proofs)

### Rules of Inference

> Argument: A sequence of propositions that end with a conclusion.

> An argument form in propositional logic is a sequence of compound propositions involving propositional variables.

> An argument is valid if the truth of all its premises implies that the conclusion is true.

> The argument form with premises p1, p2, ..., pn and conclusion q is valid, if $(p_1 \wedge p_2 \wedge \dots \wedge p_n) \rightarrow q$ is a tautology.

Rules of Inference for Propositional Logic corresponding tautology

- modus ponens (law of detachment) 肯定前件式
  
  - $(p \wedge (p \rightarrow q)) \rightarrow q$ 

- modus tollens 否定后件式
  
  - $(\neg q \wedge (p \rightarrow q)) \rightarrow \neg p$

- hypothetical syllogism 假言三段论
  
  - $((p \rightarrow q) \wedge (q \rightarrow r)) \rightarrow (p \rightarrow r)$

- disjunctive syllogism 选言三段论
  
  - $(\neg p \wedge (p \vee q)) \rightarrow q$

- addition
  
  - $p \rightarrow (p \vee q)$

- simplification
  
  - $(p \wedge q) \rightarrow p$

- conjunction
  
  - $((p) \wedge (q)) \rightarrow (p \wedge q)$

- resolution
  
  - $((p \vee q) \wedge (\neg p \vee r)) \rightarrow (q \vee r)$

- Universal Instantiation
  
  - $\forall x P(x) \therefore P(c)$ 

- Universal Generalization
  
  - $P(c) \text{ for arbitrary c} \therefore \forall x P(x)$

- Existential Instantiation
  
  - $\exists x P(x) \therefore P(c) \text{ for some element c}$ 

- Existential Generalization
  
  - $P(c) \text{ for some element c} \therefore \exists x P(x)$

### Introduction to Proofs

> A proof is a valid argument that establishes the truth of a mathematical statement.

> Axiom: a statement or proposition which is regarded as being established. 

> Theorem: a statement that can be shown to be true.

> Lemma: a statement that can be proved to be true, and is used in proving a theorem or proposition.

Methods of Proving Theorems

- Direct proof
  - If p is true, then q follows
- Proof by contrapositive
  - Show the contrapositive: If $\neg$q is true, then $\neg$p follows
- Proof by contradiction
  - show that (p $\wedge$ $\neg$q) contradicts the assumptions
- Proof by cases
  - give proofs for all possible cases
- Proof of equivalence
  - If p is true, then q follows; If q is true, then p follows

## Sets and Functions

### Sets

> A set is an unordered collection of objects.

important sets:
natural numbers N
integers Z
positive integers $Z^+$
rational number Q
real numbers R
complex numbers C

> Two sets A, B are equal if and only if $\forall x (x \in A \leftrightarrow x \in B)$ 

> The universal set is the set of all objects under consideration, denoted by U.

> The empty set is the set of no object, denoted by $\varnothing$ or {}.

> subset 子集
> 
> The set A is a subset of B if and only if every element of A is also an element of B, i.e., $\forall x (x \in A \rightarrow x \in B)$, denoted by A $\subseteq$ B.

> proper subset 真子集

> cardinality - size of a set
> 
> If there are exactly n distinct elements in S, where n is a nonnegative integer, we say that S is a finite set and n is the cardinality of S, denoted by |S|.

> power set - the set of all subsets denoted by P(S)

> tuple - ordered collection

> Two ordered n-tuples are equal if and only if each corresponding pair of their elements is equal. (ai = bi for i = 1, 2, ..., n)

> The Cartesian product of the sets A1, A2, ..., An, denoted by A1 × A2 × ... × An, is the set of ordered n-tuples (a1, a2, ..., an) where ai ∈ Ai for i = 1, ..., n: $A_1 \times A_2 \times \dots \times A_n = \{(a_1, a_2, ..., a_n) | a_i \in A_i \text{\quad for } i = 1, 2, ..., n\}$

> Let A be a set. An denotes A × A × ... × A with n sets: $A^n = {(a_1, a_2, ..., a_n) | a_i \in A \text{\quad for } i = 1, 2, ..., n}$

> A subset R of the Cartesian product A × B is called a relation from the set A to the set B.

### Set Operations

> Union: Let A and B be sets. The union of the sets A and B, denoted by A ∪ B, is the set {x | x ∈ A ∨ x ∈ B}.

> Intersection: The intersection of the sets A and B, denoted by A ∩ B, is the set {x | x ∈ A ∧ x ∈ B}.

> Complement: If A is a set, then the complement of the set A (with respect to U), denoted by $\bar{A}$ is the set U − A, $\bar{A} = \{x \in U | x \not\in A\}$

> Difference: Let A and B be sets. The difference of A and B, denoted by A − B, is the set containing the elements of A that are not in B. $A − B = \{x | x \in A \wedge x \not\in B\} = A \cap \bar{B}$.

> Two sets A and B are called disjoint if their intersection is empty, i.e., $A \cap B = \varnothing$

### Functions

> Let f be a function from A to B.
> 
> > A is the domain of f ; B is the codomain of f
> > If f (a) = b, b is called the image of a and a is a preimage of b.
> > The range of f is the set of all images of elements of A, denoted by f (A).
> > We also say f maps A to B.

> One-to-one function (injection) if and only if f (x) = f (y) implies x = y for all x, y in the domain of f

> onto function (surjection) if and only if for every b ∈ B there is an element a ∈ A such that f (a) = b

> one-to-one correspondence (bijection) if and only if it is both one-to-one and onto

> inverse function denoted by $f^{−1}$

A bijection is called invertible.

> The composition of the functions f and g, denoted by f ◦ g, is defined by (f ◦ g)(x) = f (g(x)).

> The floor function assigns a real number x the largest integer that is ≤ x, denoted by ⌊x⌋.

> The ceiling function assigns a real number x the smallest integer that is ≥ x, denoted by ⌈x⌉.

> The factorial function f : N → Z+ is the product of the first n positive integers when n is a nonnegative integer, denoted by f (n) = n!.

### Sequences and Summation

> A geometric progression is a sequence of the form a, ar, ar$^2$, ..., ar$^n$, ... where the initial term a and the common ratio r are real numbers.

> An arithmetic progression is a sequence of the form a, a + d, a + 2d, a + 3d, ..., a + nd, ... where the initial term a and common difference d are real numbers.

Some useful summation form

$\sum\limits_{k=0}^n a r^k = \dfrac{ar^{n+1}-a}{r-1} (r \not = 0, 1)$

$\sum\limits_{k=1}^n k = \dfrac{n(n+1)}{2}$

$\sum\limits_{k=1}^n k^2 = \dfrac{n(n+1)(2n+1)}{6}$

$\sum\limits_{k=1}^n k^3 = \dfrac{n^2(n+1)^2}{4}$

$\sum\limits_{k=0}^\infty x^k = \dfrac{1}{1-x} \quad(\lvert x \rvert <1)$

$\sum\limits_{k=0}^\infty k x^{k-1} = \dfrac{1}{(1-x)^2} \quad(\lvert x \rvert <1)$

### Cardinality of Sets

> The sets A and B have the same cardinality if there is a one-to-one correspondence between elements in A and B.

> If there is a one-to-one function from A to B, the cardinality of A is less than or equal to the cardinality of B, denoted by |A| ≤ |B|.

> A set that is either finite or has the same cardinality as the set of positive integers Z+ is called countable. A set that is not countable is called uncountable.
> 
> The elements of the set can be enumerated and listed.

> A function is computable if there is a computer program in some programming language that finds the values of this function.

Cantor’s theorem: If S is a set, then |S| < |P(S)|.

## Complexity of Algorithms

### The Growth of Functions

Big-O Notation: Let f and g be functions from the set of integers or the set of real numbers to the set of real numbers. We say that f (x) is O(g(x)) if there are constants C and k such that |f (x)| ≤ C|g(x)|, whenever x > k. [This is read as “f (x) is big-oh of g(x).”]

Big-O Estimates for Some Functions

- $1 + 2 + \cdots + n = O(n^2)$

- $n! = O(n^n)$

- $\log{n!} = O(n\log{n})$

- $\log_a{n} = O(n)$ for an integer $a \geqslant 2$

- $n^a = O(n^b)$ for integers $a \leqslant b$

- $n^a = O(2^n)$ for an integer $a$

Big-Omega Notation: Let f and g be functions from the set of integers or the set of real numbers to the set of real numbers. We say that f (x) is Ω(g(x)) if there are positive constants C and k such that |f (x)| ≥ C|g(x)| whenever x > k. [This is read as “f (x) is big-Omega of g(x).”]

f (x) is Ω(g(x)) if and only if g(x) is O(f (x))

Big-Theta Notation (Big-O & Big-Omega): Let f and g be functions from the set of integers or the set of real numbers to the set of real numbers.We say that f (x) is Θ(g(x)) if f (x) is O(g(x)) and f (x) is Ω(g(x)). When f (x) is Θ(g(x)), we say that f (x) is big-Theta of g(x), that f (x) is of order g(x), and that f (x) and g(x) are of the same order.

### Complexity of Algorithm

Horner’s algorithm f (x) = a0 + a1x + ... + an−1xn−1 + anxn = a0 + x(a1 + ... + x(an−1 + anx))

### P and NP Problem

> P: Problems that are solvable using an algorithm with polynomial worst-case complexity

> NP: Problems for which a solution can be checked in polynomial time.

> NP-Complete: If any of these problems can be solved by a polynomial worst-case time algorithm, then all problems in the class NP can be solved by polynomial worst-case time algorithms.

> An algorithm is polynomial-time if its running time is O(nk), where k is a constant independent of n, and n is the input size of the problem that the algorithm solves.

> A decision problem is a question that has two possible answers: yes and no.

> An optimization problem requires an answer that is an optimal configuration.

> A problem is solvable in polynomial time (or more simply, the problem is in polynomial time) if there exists an algorithm which solves the problem in polynomial time. This problem is called tractable.

> The class P consists of all decision problems that are solvable in polynomial time.

> A certificate (or witness) is a specific object corresponding to a yes-input, such that it can be used to show that the input is indeed a yes-input.

> The class NP consists of all decision problems such that, for each yes-input, there exists a certificate which allows one to verify in polynomial time that the input is indeed a yes-input.

## Number Theory

### Divisibility and Modular Arithmetic

> if $a$ and $b$ are integers with $a \neq 0$ , we say that $a$ divides $b$ if there is an integer $c$ such that $b = ac$ 
> 
> a is a factor or divisor of b, and b is a multiple of a, denoted by a $|$ b, a $\not|$ b

> If $a$ is an integer and $d$ a positive integer, then there are unique integers $q$ and $r$, with $0 \leq r < d$ , such that $a = dq + r$ .
> In this case, $d$ is called the divisor, $a$ is called the dividend, $q$ is called the quotient, and $r$ is called the remainder.
> 
> denoted q = a div d and r = a mod d

> If a and b are integers and m is a positive integer, then a is congruent to b modulo m if m divides a − b, denoted by a ≡ b (mod m). This is called congruence and m is its modulus.

> Let $\mathbf{Z}_m$ be the set of nonnegative integers less than m: {0, 1, ..., m − 1}.
> $+_m$: $a +_m b = (a + b) \mod m$ 
> $\cdot_m$: $a \cdot_m b = ab \mod m$ 

### Integer Representations

decimal binary octal hexadecimal

Binary Modular Exponentiation (ANY PROOF?)

### Primes and Greatest Common Divisors

> Fundamental Theorem of Arithmetic: Every integer greater than 1 can be written uniquely as a prime or as the product of two or more primes where the prime factors are written in order of nondecreasing size.

> Let a and b be integers, not both 0. The largest integer d such that d|a and d|b is called the greatest common divisor of a and b, denoted by gcd(a, b).

> Let a and b be positive integers. The least common multiple of a and b is the smallest positive integer that is divisible by both a and b, denoted by lcm(a, b).

Let $a = p_1^{a_1} p_gcd(a, b) = p_1^{min(a_1,b_1)} p_2^{min(a_2,b_2)} \cdots p_n^{min(a_n,b_n)}2^{a_2} \cdots p_n^{a_n} $ and $b = p_1^{b_1} p_2^{b_2} \cdots p_n^{b_n}$ then $gcd(a, b) = p_1^{min(a_1,b_1)} p_2^{min(a_2,b_2)} \cdots p_n^{min(a_n,b_n)}$ $lcm(a, b) = p_1^{max(a_1,b_1)} p_2^{max(a_2,b_2)} \cdots p_n^{max(a_n,b_n)}$ 

Euclidean Algorithm

Let a = bq + r, where a, b, q and r are integers. Then gcd(a, b) = gcd(b, r).

Bezout’s Theorem: If a and b are positive integers, then there exist integers s and t such that gcd(a, b) = sa + tb. This equation is called Bezout’s identity.

### Linear Congruences

An integer $\bar a$ such that $\bar a a$ ≡ 1 (mod m) is said to be an inverse of a modulo m.

If a and m are relatively prime integers and m > 1, then an inverse of a modulo m exists. The inverse is unique modulo m.

The Chinese Remainder Theorem: Let m1, m2, . . . , mn be
pairwise relatively prime positive integers greater than 1 and a1, a2, . . . ,
an arbitrary integers. Then, the system
x ≡ a1 (mod m1)
x ≡ a2 (mod m2)
...
x ≡ an (mod mn)
has a unique solution modulo m = m1m2...mn.

### Cryptography

shift ciphers

RSA Cryptosystem: Pick two large primes p and q. Let n = pq. Encryption key (n, e) and
decryption key (n, d) are selected such that
(1) gcd(e, (p − 1)(q − 1)) = 1
(2) ed ≡ 1 (mod (p − 1)(q − 1))
RSA encryption: C = M^e mod n;
RSA decryption: M = C^d mod n;

Fermat's little theorem: If p is prime and a is an integer not divisible by p, then $a^{p-1} \equiv 1 \pmod p$ 

## Mathematical Induction and Recursion

### Mathematical Induction

Well-Ordering Property: Every nonempty set of nonnegative integers has a least element.

Principle. (Weak Principle of Mathematical Induction)
(a) Basic Step: the statement P(b) is true
(b) Inductive Step: the statement P(n − 1) → P(n) is true for all n > b
Thus, P(n) is true for all integers n ≥ b.

### Recusion

Theorem: For any positive constants a and r, and any function g defined on nonnegative integers, the solution to the first-order linear recurrence

$$
T(n) = \left\{ 
\begin{aligned}
&a &&\text{if } n=0 \\
&rT(n − 1) + g(n) &&\text{if } n > 0
\end{aligned}
\right.
$$

is $T(n) = r^n a + \sum\limits_{i=1}^n r^{n-i} g(i)$ 

Divide and conquer, e.g. binary search

$$
T(n) = \left\{ 
\begin{aligned}
&1 &&\text{if } n=1 \\
&T(n/2) + 1 &&\text{if } n \geqslant 2
\end{aligned}
\right.
$$

Iterating recurrences

Theorem: Suppose that we have a recurrence of the form T(n) = aT(n/2) + n, where a is a positive integer and T(1) is nonnegative. Then we have the following big Θ bounds on the solution:
If a < 2, then T(n) = Θ(n).
If a = 2, then T(n) = Θ(n log2 n).
If a > 2, then T(n) = Θ(nlog2 a).

## Counting

### Counting Basis

Product rule

Sum rule

Subtraction rule

Principle of inclusion–exclusion: |A1 ∪ A2| = |A1| + |A2| − |A1 ∩ A2|.

Division rule e.g. sit around round table

The Pigeonhole Principle: If k is a positive integer and k + 1 or more objects are placed into k boxes, then there is at least one box containing two or more of the objects.

### Permutations

A permutation of a set of distinct objects is an ordered arrangement of these objects.

An ordered arrangement of r elements of a set is called an r-permutation.

P(n, r) = n(n − 1)(n − 2) · · · (n − r + 1) = n! / (n − r)!

### Combinations

An r-combination of elements of a set is an unordered selection of r elements from the set.

The number of r-combinations of a set with n distinct elements is denoted
by C(n, r).

Note that C(n, r) is also denoted by (n <cr> r) and is called a binomial coefficient.

$$
\left(
\begin{aligned}
n \\ r 
\end{aligned}
\right)
= C(n,r) = \frac{P(n,r)}{r!} = \frac{n!}{r!(n-r)!}
$$

### Binomial Coefficients

Let n and r be nonnegative integers with r ≤ n. Then C(n, r) = C(n, n − r).

A combinatorial proof of an identity is

- a proof that uses counting arguments to prove that both sides of the
  identity count the same objects but in different ways

- or a proof that is based on showing that there is a bijection between
  the sets of objects counted by the two sides of the identity.

These two types of proofs are called double counting proofs and bijective proofs, respectively.

The Binomial Theorem: Let x and y be variables, and let n be a nonnegative integer:

$$
(x+y)^n = \sum\limits_{j=0}^{n} \left(
\begin{aligned}
n \\ j
\end{aligned}
\right) x^{n-j} y^{j}
$$

Pascal’s Identity Let n and k be positive integers with n ≥ k. Then,

$$
\left(\begin{gather*}n+1 \\ k\end{gather*}\right) = 
\left(\begin{gather*}n \\ k-1\end{gather*}\right) +
\left(\begin{gather*}n \\ k\end{gather*}\right)
$$

trinomial coefficient

$$
\left(\begin{gather*}n \\ k_1 \quad k_2 \quad k_3\end{gather*}\right) = \frac{n!}{k_1!k_2!k_3!}
$$

### Generalized Permutations and Combinations

C(n + r − 1, r) = C(n + r − 1, n − 1)

### Generating Function

$G(x) = a_0 + a_1x + \cdots + a_kx_k + \cdots = \sum\limits_{k=0}^\infty a_kx^k$ 

Let $f(x) = \sum_{k=0}^\infty a_k x_k$ and $g(x) = \sum_{k=0}^\infty b_k x_k$ . Then

$$
f(x) + g(x) = \sum_{k=0}^\infty (a_k + b_k) x^k \\
f(x)g(x) = \sum_{k=0}^\infty (\sum_{j=0}^k a_j b_{k-j}) x^k
$$

Useful generating functions

$(1 + ax)^n = \sum_{k=0}^n C(n,k)a^kx^k = C(n, 0) + C(n, 1)ax + C(n, 2)a^2x^2 + ... + C(n, n)x^nx^n$ 

$(1+x^r)^n = \sum_{k=0}^n C(n,k)x^{rk}$ 

$1/(1 − ax) = \sum_{k=0}^{\infty} a^kx^k = 1 + ax + a^2x^2 + \cdots$ 

$1/(1 − x^r) = \sum_{k=0}^{\infty} x^{rk} = 1 + x^r + x^{2r} + \cdots$ 

$1/(1 − x)^n = \sum_{k=0}^\infty C(n + k - 1,k) x^k$ 

$1/(1 + x)^n = \sum_{k=0}^\infty C(n + k - 1, k) (-1)^k x^k$ 

$1/(1 - ax)^n = \sum_{k=0}^\infty C(n + k - 1, k) a^k x^k$ 

$e^x = \sum_{k=0}^\infty \frac{x^k}{k!}$ 

$\ln(1 + x) = \sum_{k=0}^\infty \frac{(-1)^{k+1} x^k}{k}$ 

Extended binomial coefficient

$$
\left(
\begin{gather*}
u \\ k
\end{gather*}
\right)
= \left\{
\begin{aligned}
&u(u-1)(u-2)\cdots (u-k+1) / k! &&\text{ if } k>0 \\
&1 &&\text{ if } k=0
\end{aligned}
\right.
$$

Let x be a real number with |x| < 1 and let u be a real number. Then

$$
(1+x)^u = \sum_{k=0}^\infty \left(
\begin{gather*}
u \\ k
\end{gather*}
\right)
x^k
$$

### Solving Linear Recurrrence Relations

A linear homogeneous relation of degree k with constant coefficients is a recurrence relation of the form $a_n = c_1a_{n−1} + c_2a_{n−2} + ... + c_ka_{n−k}$ , where c1, c2, . . . , ck are real numbers, and ck != 0.

Let c1 and c2 be real numbers. Suppose that $r^2 − c_1r − c_2 = 0$ has two distinct roots r1 and r2. The sequence {a_n} is a solution of the recurrence relation $a_n = c_1a_{n−1} + c_2a_{n−2}$ with the initial condition $a_0 = C_0$ and $a_1 = C_1$ if and only if $a_n = \alpha_1 r_1^n + \alpha_2 r_2^n$ for n = 0, 1, 2, ..., where $\alpha_1$ and $\alpha_2$ are constants.

Consider an arbitrary linear homogeneous relation of degree k with constant coefficients $a_n = \sum_{i-1}^k c_i a_{n-i}$ the characteristic equation (CE) is $r^k - \sum_{i=1}^k c_i r^{k-i} = 0$ . If this CE has k distinct roots ri, then the solutions to the recurrence are of the form $a_n = \sum_{i=1}^k \alpha_i r_i^n$ for all $n \geq 0$ , where the $\alpha_i$ 's are constants.

If the $r^2 − c_1r − c_2 = 0$ has only 1 root $r_0$ , then $a_n = (\alpha_1 + \alpha_2 n) r_0^n$ for all $n \geq 0$ and two constants $\alpha_1$ and $\alpha_2$ .

Suppose that there are t roots r_1, . . . , r_t with multiplicities m_1, . . . , m_t. Then, $a_n = \sum_{i=1}^t (\sum_{j=0}^{m_i-1}a_{i,j} n^j) r_i^n$ for all $n \geq 0$ and constants $\alpha_{i,j}$ .

A linear nonhomogeneous relation with constant coefficients may contain some terms F(n) that depend only on n: $a_n = c_1a_{n−1} + c_2a_{n−2} + ... + c_ka_{n−k} + F(n)$ . The recurrence relation $a_n = c_1a_{n−1} + c_2a_{n−2} + ... + c_ka_{n−k}$ is called the associated homogeneous recurrence relation.

Every solution is the sum of a particular solution and a solution of the associated linear homogeneous recurrence relation.

If {a(p) n } is any particular solution to the linear nonhomogeneous relation with constant coefficients, an = c1an−1 + c2an−2 + ... + ckan−k + F(n), then all its solutions are of the forman = a_n^(p)+a_n^(h) 

## Relations

### Relation

Let A and B be two sets. A binary relation from A to B is a subset of a Cartesian product A × B.

Representation: graph, table

Theorem: The number of binary relations on a set A, where |A| = n, is $2^{n^2}$. 

**Reflexive Relation**: A relation R on a set A is called reflexive if (a, a) ∈ R for every element a ∈ A.

A relation R is reflexive if and only if MR (table form) has 1 in every position on its main diagonal.

Theorem: The number of reflexive relations on a set A with |A| = n is $2^{n(n−1)}$. 

**Irreflexive Relation**: A relation R on a set A is called irreflexive if (a, a) /∈ R for every element a ∈ A.

A relation R is irreflexive if and only if MR has 0 in every position on its main diagonal.

**Symmetric Relation**: A relation R on a set A is called symmetric if (b, a) ∈ R whenever (a, b) ∈ R for all a, b ∈ A.

A relation R is symmetric if and only if MR is symmetric.

The number of symmetric relations on set A, where A has n elements, is $2^{n(n+1)/2}$. 

**Antisymmetric Relation**: A relation R on a set A is called antisymmetric if (b, a) ∈ R and (a, b) ∈ R implies a = b for all a, b ∈ A.

A relation R is antisymmetric if and only if mij = 1 implies mji = 0 for i ̸= j. (mij and mji can be both 0 but cannot be both 1, main diagonal is not taken into consideration)

The number of antisymmetric relations on set A, where A has n elements, is $2^n 3^{n(n−1)/2}$.

**Transitive Relation**: A relation R on a set A is called transitive if (a, b) ∈ R and (b, c) ∈ R implies (a, c) ∈ R for all a, b, c ∈ A.

Let R be a relation from a set A to a set B and S be a relation from B to C. The composite of R and S is the relation consisting of the ordered pairs (a, c) where a ∈ A and c ∈ C and for which there is a b ∈ B such that (a, b) ∈ R and (b, c) ∈ S. We denote the composite of R and S by S ◦ R.

Definition: Let R be a relation on A. The powers Rn, for n = 1, 2, 3, ..., is 

Theorem: The relation R on a set A is transitive if and only if Rn ⊆ R for
n = 1, 2, 3, ...defined inductively by R1 = R and Rn+1 = Rn ◦ R

### n-ary Relations

An n-ary relation R on sets A1, ..., An, written as R : A1, ..., An, is a subset R ⊆ A1 × · · · × An.

The sets A1, ..., An are called the domains of R.

The degree of R is n.

primary key, composite key

selection operator, projection operator, join operator

### Representing Relations

zero-one matrx $m_{ij} = 1, 0$ 

join: $a_{ij} \vee b_{ij}$ 

meet: $a_{ij} \wedge b_{ij}$ 

boolean product A ⊙ B: cij = (ai1 ∧ b1j) ∨ (ai2 ∧ b2j) ∨ · · · ∨ (aik ∧ bkj)

M_{S◦R} = MR ⊙ MS

directed graph: reflective: loop on every point; symmetric: both directions of each edge

edge (a, b): initial vertex a, terminal vertex b

### Closures of Relations

Let R be a relation on a set A. A relation S on A with property P is called the closure of R with respect to P if S is subset of every relation Q (S ⊆ Q) with property P that contains R (R ⊆ Q).

S is the minimal set containing R satisfying the property P.

Definition: A path from a to b in the directed graph G is a sequence of edges (x0, x1), (x1, x2), . . . , (xn−1, xn) in G, where n is nonnegative and x0 = a and xn = b.

A path of length n ≥ 1 that begins and ends at the same vertex is called a circuit or cycle.

Theorem: Let R be relation on a set A. There is a path of length n from a to b if and only if (a, b) ∈ R^n.

Lemma: Let A be a set with n elements, and R a relation on A. If there is a path from a to b with a ̸= b, then there exists a path of length ≤ n − 1.

Theorem: The transitive closure of a relation R equals the connectivity relation R∗, where R∗ = $\cup_{k=1}^\infty R^k$.

Theorem: Let MR be the zero–one matrix of the relation R on a set with n elements. Then the zero–one matrix of the transitive closure R∗ is $M_{R∗} = M_R ∨ M^{[2]}_R ∨ M^{[3]}_R ∨ \cdots ∨ M^{[n]}_R$ where $M^{[n]}_R = M_R \odot M_R ⊙ · · · ⊙ M_R$

### Relation Equivalence

Definition: A relation R on a set A is called an equivalence relation if it is reflexive, symmetric, and transitive.

Definition: Let R be an equivalence relation on a set A. The set of all elements that are related to an element a of A is called the equivalence class of a, denoted by \[a\]~R~. When only one relation is considered, we use the notation [a].

Theorem: Let R be an equivalence relation on a set A. The following statements are equivalent: (i)aRb (ii) \[a\] = \[b\] (iii) [a] ∩ [b] $\neq \varnothing$

Definition: Let S be a set. A collection of nonempty subsets of S, i.e A1, A2, . . . , Ak, is called a partition of S if: Ai ∩ Aj = ∅, i ̸= j and S = $\cup_{i=1}^k A_i$

Theorem: Let R be an equivalence relation on a set A. Then, union of all the equivalence classes of R is A: A = $\cup_{a∈A} [a]_R$

Theorem: The equivalence classes form a partition of A.

Theorem: Let {A1, A2, ..., Ai, ...} be a partition of S. Then, there is an equivalence relation R on S, that has the sets Ai as its equivalence classes.

### Partial Ordering

A relation R on a set S is called a partial ordering, or partial order, if it is reflexive, antisymmetric, and transitive.

A set S together with a partial ordering R is called a partially ordered set, or poset, denoted by (S, R).

The notation a $\preceq$ b is used to denote that (a, b) ∈ R in an arbitrary poset (S, R). The notation a ≺ b denotes that a $\preceq$ b, but a $\neq$ b.

If (S, $\preceq$) is a poset and every two elements of S are comparable, S is called a totally ordered or linearly ordered set, and $\preceq$ is called a total order or a linear order. A totally ordered set is also called a chain.

(S, $\preceq$) is a well-ordered set if it is a poset such that $\preceq$ is a total ordering and every nonempty subset of S has a least element.

The Principle of Well-Ordered Induction: Suppose that (S, $\preceq$) is a well-ordered set. Suppose x0 is the least element of a well ordered set. Then P(x) is true for all x ∈ S, if
**Basic Step**: P($x_0$) is true.
**Inductive Step**: For every y ∈ S \ \{x0\}, if P(x) is true for all x ∈ S with x ≺ y, then P(y) is true.
Or equivalently,
**Inductive Step**: For every y ∈ S, if P(x) is true for all x ∈ S with x ≺ y, then P(y) is true.

EQUIVALENT NOTATION
- a $\prec$ b
- aRb
- (a,b) $\in$ R

Definition: a is a maximal (resp. minimal) element in poset (S, ≼) if there is no b ∈ S such that a ≺ b (resp. b ≺ a).

a is the greatest (resp. least) element of the poset (S, ≼) if b ≼ a (resp. a ≼ b) for all b ∈ S.

A partial ordered set in which every pair of elements has both a least upper bound and a greatest lower bound is called a lattice.

Topological sorting: Given a partial ordering R, find a total ordering ≼ such that a ≼ b whenever aRb. ≼ is said compatible with R.

Every finite nonempty poset (S, ≼) has at least one minimal element.

## Graphs

A graph G = (V , E) consists of a nonempty set V of vertices
(or nodes) and a set E of edges. Each edge has either one or two vertices associated with it, called its endpoints. An edge is said to be incident to (or connect) its endpoints.

simple graph: A graph in which each edge connects two different vertices and where no two edges connect the same pair of vertices.

Multigraph: Graphs that may have multiple edges connecting the same vertices.

Pseudograph: Graphs that may include loops, and possibly multiple edges connecting the same pair of vertices or a vertex to itself.

A directed graph (or digraph) (V , E) consists of a nonempty set of vertices V and a set of directed edges (or arcs) E. The directed edge associated with the ordered pair (u, v) is said to start at u and end at v.

Influence graphs: directed graphs where there is an edge from one person to another if the first person can influence the second one.
Collaboration graphs: undirected graphs where two people are connected if they collaborate in some way

Two vertices u, v in an undirected graph G are called
adjacent (or neighbors) in G if there is an edge e between u and v. Such an edge e is called incident with the vertices u and v and e is said to connect u and v.

The set of all neighbors of a vertex v of G = (V , E), denoted by N(v), is called the neighborhood of v.

If A is a subset of V , we denote by N(A) the set of all vertices in G that are adjacent to at least one vertex in A.

The degree of a vertex in an undirected graph is the number of edges incident with it, except that a loop at a vertex contributes two to the degree of that vertex. The degree of the vertex v is denoted by deg(v).

An directed graph G = (V , E) consists of V , a nonempty set of vertices, and E, a set of directed edges.

Let (u, v) be an edge in G. Then u is the initial vertex of the edge and is adjacent to v, and v is the terminal vertex of this edge and is adjacent from u.

The in-degree of a vertex v, denoted by deg−(v), is the
number of edges which terminate at v. The out-degree of v, denoted by deg+(v), is the number of edges with v as their initial vertex.

Theorem: Let G = (V , E) be a graph with directed edges.Then, $\vert{E}\vert = \sum_{v\in V} deg^-(v) = \sum_{v\in V} deg^+ (v)$

### Graph and Terminologies

Definition: A simple graph G is bipartite if V can be partitioned into two disjoint subsets V1 and V2 such that every edge connects a vertex in V1 and a vertex in V2.
An equivalent definition of a bipartite graph is a graph where it is possible
to color the vertices red or blue so that no two adjacent vertices are of the same color.

Definition: A complete bipartite graph K~m,n~ is a graph that has its vertex set partitioned into two subsets V1 of size m and V2 of size n such that there is an edge from every vertex in V1 to every vertex in V2.

Given a bipartite graph, a matching is a subset of edges E such that no two edges are incident with the same vertex.
In other words, a matching is a subset of edges such that if {s, t} and {u, v} are distinct edges of the matching, then s, t, u, and v are distinct.

A maximum matching is a matching with the largest number of edges.

A matching M in a bipartite graph G = (V , E) with bipartition (V1, V2) is a complete matching from V1 to V2 if every vertex in V1 is the endpoint of an edge in the matching, or equivalently, if |M| = |V1|.

Theorem (Hall’s Marriage Theorem): The bipartite graph G = (V , E) with bipartition (V1, V2) has a complete matching from V1 to V2 if and only if |N(A)| ≥ |A| for all subsets A of V1.

Definition: A subgraph of a graph G = (V , E) is a graph (W , F), where W ⊆ V and F ⊆ E.
A subgraph H of G is a proper subgraph of G if H ̸= G.

Definition: The union of two simple graphs G1 = (V1, E1) and G2 = (V2, E2) is the simple graph with vertex set V1 ∪ V2 and edge set E1 ∪ E2, denoted by G1 ∪ G2.

### Representing Graphs and Graph Isomorphism

Definition: An adjacency list can be used to represent a graph with no multiple edges by specifying the vertices that are adjacent to each vertex of the graph.

Definition: Suppose that G = (V , E) is a simple graph with |V | = n. Arbitrarily list the vertices of G as v1, v2, . . . , vn. The adjacency matrix AG of G, is the n × n zero-one matrix with 1 as its (i, j)-th entry when v~i~ and v~j~ are adjacent, and 0 as its (i, j)-th entry when they are not adjacent.

Definition: Let G = (V , E) be an undirected graph with vertices v1, v2, . . . , vn and edges e1, e2, . . . , em. The incidence matrix with respect to the ordering of V and E is the n × m matrix M = [m~ij~]~n×m~, where
$m_{ij} = \left\{
\begin{aligned}
&1 \quad \text{if edge e} _\text{j} \text{ is incident with v} _\text{i} \\ &0 \quad \text{otherwise.}
\end{aligned}
\right.$

Definition: The simple graphs G1 = (V1, E1) and G2 = (V2, E2) are isomorphic if there is a one-to-one and onto function from V1 to V2 with the property that a and b are adjacent in G1 if and only if f (a) and f (b) are adjacent in G2, for all a and b in V1. Such a function is called an isomorphism.

### Connectivity

Definition: Let n be a nonnegative integer and G an undirected graph. A path of length n from u to v in G is a sequence of n edges e1, e2, . . . , en of G for which there exists a sequence x0 = u, x1, . . . , xn−1, xn = v of vertices such that ei has the endpoints xi−1 and xi for i = 1, ..., n.

The path is a circuit if it begins and ends at the same vertex, i.e., if u = v, and has length greater than zero.

A path or circuit is simple if it does not contain the same edge more than once.

Definition: Let n be a nonnegative integer and G an directed graph. A path of length n from u to v in G is a sequence of n edges e1, e2, . . . , en of G for which there exists a sequence x0 = u, x1, . . . , xn−1, xn = v of vertices such that ei is associated with initial vertex xi−1 and terminal vertex xi for i = 1, ..., n.

An undirected graph is called connected if there is a path between every pair of distinct vertices of the graph.

Lemma: If there is a path between two distinct vertices x and y of a graph G, then there is a simple path between x and y in G.

Theorem: There is a simple path between every pair of distinct vertices of a connected undirected graph.

A connected component of a graph G is a connected subgraph of G that is not a proper subgraph of another connected subgraph of G.

Definition: A directed graph is strongly connected if there is a path from a to b and a path from b to a whenever a and b are vertices in the graph.

Definition: A directed graph is weakly connected if there is a path between every two vertices in the underlying undirected graph.

A set of edges E ′ is called an edge cut of G if the subgraph G − E ′ is disconnected. The edge connectivity λ(G) is the minimum number of edges in an edge cut of G.

The existence of a simple circuit of length k is isomorphic invariant. This can be used to construct mappings that may be isomorphisms.

Theorem: Let G be a graph with adjacency matrix A with respect to the ordering v1, v2, . . . , vn of vertices. The number of different paths of length r from vi to vj, where r is a positive integer, equals the (i, j)-th entry of Ar.

Theorem: Let R be relation on a set A. There is a path of length n from a to b if and only if (a, b) ∈ Rn. (Boolean product.)

Theorem: The number of different paths of length r from vi to vj, where r is a positive integer, equals the (i, j)-th entry of Ar.

### Euler and Hamilton Path

Definition: An Euler circuit in a graph G is a simple circuit containing every edge of G. An Euler path in G is a simple path containing every edge of G.

Consider undirected graph:
Euler Circuit ⇒ The degree of every vertex must be even
Euler Path ⇒ The graph has exactly two vertices of odd degree

Theorem: A connected multigraph with at least two vertices has an Euler circuit if and only if each of its vertices has even degree.

Theorem: A connected multigraph has an Euler path but not an Euler circuit if and only if it has exactly two vertices of odd degree.

Definition: A simple path in a graph G that passes through every vertex exactly once is called a Hamilton path, and a simple circuit in a graph G that passes through every vertex exactly once is called a Hamilton circuit.

### Shortest-path Problem

**Dijkstra’s Algorithm**

S: a distinguished set of vertices;
L(v): the length of a shortest path from a to v that contains only the vertices in S as the interior vertices.
(i) Set L(a) = 0 and L(v) = ∞ for all v, S = ∅
(ii) While z /∈ S
u := a vertex not in S with L(u) minimal
S := S ∪ {u}
For all vertices v not in S
L(v) := min{L(u) + w(u, v), L(v)}

### Planar Graphs

Theorem (Euler’s Formula): Let G be a connected planar simple graph with e edges and v vertices. Let r be the number of regions in a planar representation of G. Then, r = e − v + 2.

Definition: The degree of a region is defined to be the number of edges on the boundary of this region. When an edge occurs twice on the boundary, it contributes two to the degree.

Corollary 1: If G is a connected planar simple graph with e edges and v vertices, where v ≥ 3, then e ≤ 3v − 6.

Corollary 2: If G is a connected planar simple graph, then G has a vertex of degree not exceeding 5.

Corollary 3: In a connected planar simple graph has e edges and v vertices with v ≥ 3 and no circuits of length three, then e ≤ 2v − 4.

Theorem: A graph is nonplanar if and only if it contains a subgraph homomorphic to K3,3 or K5.

### Graph Coloring

The chromatic number of a graph is the least number of colors needed for a coloring of this graph, denoted by χ(G).
Theorem (Four Color Theorem): The chromatic number of a planar graph is no greater than four.

## Trees

### Tree

Definition: A tree is a connected undirected graph with no simple circuits.

Theorem: An undirected graph is a tree if and only if there is a unique simple path between any two of its vertices.

Definition: A rooted tree is a tree in which one vertex has been designated as the root and every edge is directed away from the root.

The parent of v is the unique vertex u such that there is a directed edge from u to v.
When u is the parent of v, v is called a child of u.
Vertices with the same parent are called siblings.

The ancestors of a vertex are the vertices in the path from the root to this vertex, excluding the vertex itself and including the root.
The descendants of a vertex v are those vertices that have v as an ancestor.

A vertex of a rooted tree is called a leaf if it has no children.
Vertices that have children are called internal vertices.

Subtree with a as its root: consists of a and its descendants and all edges incident to these descendants.

Definition: A rooted tree is called an m-ary tree if every internal vertex has no more than m children. The tree is called a full m-ary tree if every internal vertex has exactly m children. In particular, an m-ary tree with m = 2 is called a binary tree.

Definition: An ordered rooted tree is a rooted tree where the children of each internal vertex are ordered. Ordered rooted trees are drawn so that the children of each internal vertex are shown in order from left to right.

Theorem: A tree with n vertices has n − 1 edges.

Theorem: A full m-ary tree with i internal vertices has n = mi + 1 vertices.

Theorem: A full m-ary tree with
(i) n vertices has i = (n − 1)/m internal vertices and l = [(m − 1)n + 1]/m leaves,
(ii) i internal vertices has n = mi + 1 vertices and l = (m − 1)i + 1 leaves,
(iii) l leaves has n = (ml − 1)/(m − 1) vertices and i = (l − 1)/(m − 1) internal vertices.
Using n = mi + 1 and n = i + l

The level of a vertex v in a rooted tree is the length of the unique path from the root to this vertex.
The height of a rooted tree is the maximum of the levels of the vertices.

A rooted m-ary tree of height h is balanced if all leaves are at levels h or h − 1.

Theorem: There are at most mh leaves in an m-ary tree of height h.
Corollary: If an m-ary tree of height h has l leaves, then h ≥ ⌈logm l⌉. If the m-ary tree is full and balanced, then h = ⌈logm l⌉.

### Tree Traversal

The procedures for systematically visiting every vertex of an ordered tree are called traversals.

in preorder: listing each vertex the first time this curve passes it
in inorder: listing a leaf the first time the curve passes it and listing each internal vertex the second time the curve passes it
in postorder: listing a vertex the last time it is passed on the way back up to its parent.

preorder: visit root first
inorder: visit the left subtree then root then right subtree
postorder: 

An inorder traversal of the tree representing an expression produces the original expression when parentheses are included except for unary operation. The fully parenthesized expression obtained in this way is said to be in infix form.

The preorder traversal of expression trees leads to the prefix form of the expression (Polish notation).
Prefix expressions are evaluated by working from right to left. When we encounter an operator, we perform the operation with the two operands to the right.

The postorder traversal of expression trees leads to the postfix form of the expression (reverse Polish notation).
Postfix expressions are evaluated by working from left to right. When we encounter an operator, we perform the operation with the two operands to the left.

### Spanning Trees

Definition: Let G be a simple graph. A spanning tree of G is a subgraph of G that is a tree containing every vertex of G.

Depth-First Search
- First, arbitrarily choose a vertex of the graph as the root.
- Form a path by successively adding vertices and edges. Continue adding to this path as long as possible.
- If the path goes through all vertices of the graph, the tree is a spanning tree.
- Otherwise, move back to some vertex to repeat this procedure (backtracking).

Breadth-First Search
- First arbitrarily choose a vertex of the graph as the root.
- Form a path by adding all edges incident to this vertex and the other endpoint of each of these edges
- For each vertex added at the previous level, add edge incident to this vertex, as long as it does not produce a simple circuit.
- Continue in this manner until all vertices have been added.

### Minimum Spanning Trees

Definition: A minimum spanning tree in a connected weighted graph is a spanning tree that has the smallest possible sum of weights of its edges.

Two greedy algorithms: Prim’s Algorithm, Kruscal’s Algorithm.

Prim's Algorithm
**procedure** Prim(G: weighted connected undirected graph with n vertices)
T := a minimum-weight edge
for i := 1 to n-2
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;e := an edge of minimum weight incident to a vertex in T and not forming a simple circuit in T if added to T
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;T:= T with e added
return T \{T is a minimum spanning tree of G\}

Kruskal's Algorithm
**procedure** Kruskal(G: weighted connected undireced graph with n vertices)
T := empty graph
for i := 1 to n-1
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;e:= any edge in G with smallest weight taht does not form a simple circuit when added to T
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;T := T with e added
return T (T is a mininmum spanning tree of G)
