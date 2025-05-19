<!---
{
  "id": "da751de6-10d3-4770-a4d3-359f08bc6631",
  "depends_on": [],
  "author": "Stephan Bökelmann",
  "first_used": "2025-03-27",
  "keywords": ["mathematics", "mapping", "function"]
}
--->

# Mappings and Functions

## 1) Introduction
One of computer science' many roots lies in mathematics.  
We can see echoes of this still in modern code and especially in the terminology.  
An example of this is the _function_. 

> **Definition:**  
> A *function* is a mapping from one set (the domain) to another set (the codomain), assigning each element of the domain exactly one element of the codomain.

Let's first establish the term _set_ once again:

> **Definition:**  
> A **set** is a well-defined collection of **objects**, called *elements*, such that each object is either *in* the set or *not in* the set.

We can illustrate this definition a bit more.  
Imagine you're at home and gather a few things you like:
- a **blue pen**
- a **coffee mug**
- a **guitar pick**

You mentally group these things together and call them your "**desk buddies**." That collection is now a **set**!  
Since all of the objects are well-defined thingees in your collection.  
You’ve created a **set of objects**. Each object is called an **element** of that set.  
We might write it like this:

```
DeskBuddies = { blue pen, coffee mug, guitar pick }
```

The key ideas here are, that  
**a)** each object is clearly **either in or not in** the set,  
**b)** the order of the objects doesn’t matter in terms of them being in the set or not, and  
**c)** there are no duplicates. A set does not care if you have two identical pens. The nature of “pen” is just in this set once.

Let’s now talk about a more abstract set, like:

```
A = {1, 2, 3, 4, 5}
```

This is a **set of numbers**. Just like before, each number is an **object** in the set:
- `3 ∈ A` means 3 is in the set.
- `7 ∉ A` means 7 is not in the set.

Sets can also be infinite:

```
ℕ = {0, 1, 2, 3, 4, 5, ...}
```

That’s the set of **natural numbers**. Every natural number is an object, and all of them together form a well-defined set.

---

### 1.0.2) Binary Numbers

In computer science, we often work with **binary numbers** — numbers that are written using only the digits `0` and `1`.  
These too form a set:

```
B = {0, 1, 10, 11, 100, 101, ...}
```

Here, `10` in binary represents the number 2 in decimal, `11` is 3, `100` is 4, and so on.  
Every binary number is a finite sequence of 0s and 1s, and they represent quantities just like decimal numbers do.

You can think of them as **strings** over the set `{0, 1}` or as **natural numbers written in base 2**.

---

###  1.0.3) Visualising Sets as Horizontal Bars

We can also *draw* sets to better understand them.  
For instance, the set of natural numbers up to 10 can be shown as a horizontal bar, also called a **Zahlenstrahl**:

```
0 — 1 — 2 — 3 — 4 — 5 — 6 — 7 — 8 — 9 — 10
```

Each number is an **element** of the set \( \{0, 1, ..., 10\} \).  
We can think of each point on the bar as a "location" occupied by an object in the set.

---

## 1.0.4) Visualising Functions as Arrows

Now, let’s use this idea to visualize a **function**.  
Imagine two such horizontal bars (sets), and arrows going from one to the other, assigning each element exactly one "target":

```
Domain:     0 — 1 — 2 — 3 — 4
              ↘  ↘   ↘   ↘   ↘  
Codomain:   0 — 1 — 2 — 3 — 4 — 5
```

Suppose the function \( f(x) = x + 1 \).  
Then:
- \( f(0) = 1 \)
- \( f(1) = 2 \)
- \( f(2) = 3 \)
- \( f(3) = 4 \)
- \( f(4) = 5 \)

Each number on the top bar (domain) has a unique arrow pointing to the corresponding result in the bottom bar (codomain).  
This is the essence of a **function as a mapping**.


### 1.1) Further Readings and Other Sources

- Halmos. [Naive Set Theory](https://doi.org/10.1007/978-1-4612-4284-2)
- Halmos. [How to Write Mathematics](https://doi.org/10.2307/2317880)
- Milner. [Functions as Processes](https://doi.org/10.1007/3-540-54233-7_162)
- [What is a Function?" by 3Blue1Brown](https://www.youtube.com/watch?v=ne6p6MfLBxc)
- [Interactive: Set Theory Visualizer by Visualgo](https://visualgo.net/en/set)


## 2) Tasks
1. **Visualizing a Function**: Take a sheet of paper and visualize a function of an input called `n`, which is an Element of the set of natural numbers. And has an output called m. The function is defined as 

```
m = function(n) = n * n
```

2. **Visualize a more complex function**: Visualize a function, which' domain is the set of all two capital letter character combinations in the latin alphabet, and the codomain being the set of natural numbers. Let the function definition be the sum of both characters counting distance to the letter `A`. 

<details>
  <summary>Additional information</summary>
  Distance of `A` to `A` being 0;
  Distance of `B` to `A` being 1;
  Distance of `C` to `A` being 2;
  ...

  Start by writing out a mapping table if you get confused.
</details>

3. **Investigate Function Collisions**:  
Define a function from the set of all 3-digit binary numbers (e.g. `'000'`, `'001'`, ..., `'111'`) to the set of natural numbers.  
Let the function interpret the binary string as a number in base 2.

```
f(binary_string) = value of binary_string interpreted as a base-2 number
```

Examples:
- `f('000') = 0`
- `f('001') = 1`
- `f('010') = 2`
- `f('111') = 7`

Draw both sets: the domain (all 3-digit binary strings) and the codomain (natural numbers 0 through 7), draw arrows to represent how each element of the domain maps to the codomain.


## 3) Questions
1. What are other examples of functions, where objects of one set is being mapped onto a different set?
2. Does it matter - in an abstract way - which types of elements are contained in a domain or codomain?
3. How do the terms *injective* and *surjective* relate to the here presented functions?
4. What does the verb *to evaluate* mean? What are its ethymological roots and how is the term used in math and computer-science?
5. Is a mapping from _l = m(n)_: ℕ→ℕ with _l, n ∈ ℕ_ still a function, if it adds a random value to _n_ every time the mapping is evaluated?


## 4) Advice
Understanding mappings and functions is foundational to both mathematics and computer science. While the definitions are abstract, the concepts are everywhere — from simple arithmetic to complex algorithms, from spreadsheet formulas to neural networks.

> Take your time to truly grasp what it means to associate each element of one set with exactly one in another.

When working through these exercises:
- **Draw and sketch** — diagrams often reveal structure more clearly than symbols alone.
- **Think in examples** — concrete instances help anchor abstract ideas.
- **Look for patterns** — spotting structure helps build intuition.
- **Discuss your ideas** — explaining functions to a peer is one of the best ways to test your own understanding.
- **Don’t fear mistakes** — they are stepping stones to deeper insight.

Finally, try to **connect the dots** between what you see here and what you already know:
- A hash function in a database? That’s a mapping.
- CSS styling rules mapping class names to formatting? Also a function.
- Pressing a key on your keyboard and getting a character? Yep — another mapping.

> Mastering functions means gaining access to a universal language used across all domains of computing and mathematics.

Keep going. Every insight compounds.
