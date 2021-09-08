# CS 61B: Data Structures

    University of California, Berkeley
    Instructors: Paul Hilfinger
    hilfingr@cs.berkeley.edu
    Office Hours: TBD
    Lecture: Mon/Wed/Fri 1:00pm-2:00pm, Stanley 105 as capacity allows
    https://berkeley.zoom.us/j/94882182481?pwd=Q1BuVGdHb2p3T3JKc2xhMHRpZE9jQT09#success
    Author: Will Tholke

## Table of Contents

- [CS 61B: Data Structures](#cs-61b-data-structures)
  - [Table of Contents](#table-of-contents)
  - [Lecture 1, 08/25/21 (Wk1): Intro, Hello World Java](#lecture-1-082521-wk1-intro-hello-world-java)
    - [Grading](#grading)
    - [Methods (Functions)](#methods-functions)
    - [Selection & Access](#selection--access)
  - [Lecture 2, 08/27/21 (Wk1): A Little Programming](#lecture-2-082721-wk1-a-little-programming)
    - [Writing Programs](#writing-programs)
    - [Example: printPrimes](#example-printprimes)
  - [Lecture 3, 08/30/21 (Wk2): Values and Containers](#lecture-3-083021-wk2-values-and-containers)
    - [Values and Containers](#values-and-containers)
    - [Primitive Operations](#primitive-operations)
    - [Destructive vs. Non-destructive](#destructive-vs-non-destructive)
  - [Lecture 4, 09/01/21 (Wk2): Simple Pointer Manipulation](#lecture-4-090121-wk2-simple-pointer-manipulation)
    - [The "Final" Keyword](#the-final-keyword)
    - [Examples of Destructive Incrementing](#examples-of-destructive-incrementing)
  - [Lecture 5, 09/03/21 (Wk2): Arrays](#lecture-5-090321-wk2-arrays)
    - [Arrays](#arrays)
    - [Insert Into an Array](#insert-into-an-array)
    - [Java Shortcut](#java-shortcut)
    - [Multidimensional Arrays](#multidimensional-arrays)
  - [Lecture 6, 09/08/21 (Wk3): Developing a Sort, Unit Testing](#lecture-6-090821-wk3-developing-a-sort-unit-testing)
    - [Multidimensional Arrays (continued)](#multidimensional-arrays-continued)
    - [How do We Know If it works?](#how-do-we-know-if-it-works)
    - [Testing Workflow (Test Driven Development)](#testing-workflow-test-driven-development)
    - [JUnit: Explained](#junit-explained)
  - [Lecture 7, 09/10/21 (Wk3): Object-Based Programming](#lecture-7-091021-wk3-object-based-programming)
    - [Subtitle #1](#subtitle-1)
  - [Lecture 8, 09/13/21 (Wk4): Object-oriented Mechanisms](#lecture-8-091321-wk4-object-oriented-mechanisms)
    - [Subtitle #1](#subtitle-1-1)
  - [Lecture 9, 09/15/21 (Wk4): Interfaces and Abstract Classes](#lecture-9-091521-wk4-interfaces-and-abstract-classes)
    - [Subtitle #1](#subtitle-1-2)
  - [Lecture 10, 09/17/21 (Wk4): Interfaces and Abstract Classes](#lecture-10-091721-wk4-interfaces-and-abstract-classes)
    - [Subtitle #1](#subtitle-1-3)
  - [Lecture 11, 09/20/21 (Wk5): Examples: Comparable and Reader](#lecture-11-092021-wk5-examples-comparable-and-reader)
    - [Subtitle #1](#subtitle-1-4)
  - [Lecture 12, 09/22/21 (Wk5): Additional OOP Details, Exceptions](#lecture-12-092221-wk5-additional-oop-details-exceptions)
    - [Subtitle #1](#subtitle-1-5)
  - [Lecture 13, 09/24/21 (Wk5): Packages, Access, Loose Ends](#lecture-13-092421-wk5-packages-access-loose-ends)
    - [Subtitle #1](#subtitle-1-6)
  - [Lecture 14, 09/27/21 (Wk6): Integers](#lecture-14-092721-wk6-integers)
    - [Subtitle #1](#subtitle-1-7)
  - [Lecture 15, 09/29/21 (Wk6): Integers](#lecture-15-092921-wk6-integers)
    - [Subtitle #1](#subtitle-1-8)
  - [Lecture 16, 10/01/21 (Wk6): Complexity](#lecture-16-100121-wk6-complexity)
    - [Subtitle #1](#subtitle-1-9)
  - [Lecture 17, 10/04/21 (Wk7): Collections, Amortization](#lecture-17-100421-wk7-collections-amortization)
    - [Subtitle #1](#subtitle-1-10)
  - [Lecture 18, 10/06/21 (Wk7): Sequences, Some Design Patterns](#lecture-18-100621-wk7-sequences-some-design-patterns)
    - [Subtitle #1](#subtitle-1-11)
  - [Lecture 19, 10/08/21 (Wk7): Sequences (II)](#lecture-19-100821-wk7-sequences-ii)
    - [Subtitle #1](#subtitle-1-12)
  - [Lecture 20, 10/11/21 (Wk8): Trees](#lecture-20-101121-wk8-trees)
    - [Subtitle #1](#subtitle-1-13)
  - [Lecture 21, 10/13/21 (Wk8): Tree searching](#lecture-21-101321-wk8-tree-searching)
    - [Subtitle #1](#subtitle-1-14)
  - [Lecture 22, 10/03/21 (Wk8): Game trees](#lecture-22-100321-wk8-game-trees)
    - [Subtitle #1](#subtitle-1-15)
  - [Lecture 23, 10/18/21 (Wk9): Priority Queues, Range Queries](#lecture-23-101821-wk9-priority-queues-range-queries)
    - [Subtitle #1](#subtitle-1-16)
  - [Lecture 24, 10/20/21 (Wk9): Hashing](#lecture-24-102021-wk9-hashing)
    - [Subtitle #1](#subtitle-1-17)
  - [Lecture 25, 10/22/21 (Wk9): Generics](#lecture-25-102221-wk9-generics)
    - [Subtitle #1](#subtitle-1-18)
  - [Lecture 26, 10/25/21 (Wk10): Sorting](#lecture-26-102521-wk10-sorting)
    - [Subtitle #1](#subtitle-1-19)
  - [Lecture 27, 10/27/21 (Wk10): Sorting (II)](#lecture-27-102721-wk10-sorting-ii)
    - [Subtitle #1](#subtitle-1-20)
  - [Lecture 28, 10/29/21 (Wk10): Sorting (III)](#lecture-28-102921-wk10-sorting-iii)
    - [Subtitle #1](#subtitle-1-21)
  - [Lecture 29, 11/01/21 (Wk11): Balanced Search Structures](#lecture-29-110121-wk11-balanced-search-structures)
    - [Subtitle #1](#subtitle-1-22)
  - [Lecture 30, 11/03/21 (Wk11): Review (and it's my birthday!)](#lecture-30-110321-wk11-review-and-its-my-birthday)
    - [Subtitle #1](#subtitle-1-23)
  - [Lecture 31, 11/05/21 (Wk11): Balanced Search Structures (II)](#lecture-31-110521-wk11-balanced-search-structures-ii)
    - [Subtitle #1](#subtitle-1-24)
  - [Lecture 32, 11/08/21 (Wk12): Git Internals](#lecture-32-110821-wk12-git-internals)
    - [Subtitle #1](#subtitle-1-25)
  - [Lecture 33, 11/10/21 (Wk12): Graphs, Introduction, Traversals](#lecture-33-111021-wk12-graphs-introduction-traversals)
    - [Subtitle #1](#subtitle-1-26)
  - [Lecture 34, 11/12/21 (Wk12): A* Search, Minimal spanning trees, Union-find](#lecture-34-111221-wk12-a-search-minimal-spanning-trees-union-find)
    - [Subtitle #1](#subtitle-1-27)
  - [Lecture 35, 11/15/21 (Wk13): Pseudo-Random Sequences](#lecture-35-111521-wk13-pseudo-random-sequences)
    - [Subtitle #1](#subtitle-1-28)
  - [Lecture 36, 11/17/21 (Wk13): Dynamic Programming, Enumeration Types](#lecture-36-111721-wk13-dynamic-programming-enumeration-types)
    - [Subtitle #1](#subtitle-1-29)
  - [Lecture 37, 11/19/21 (Wk13): Threads, Garbage Collection](#lecture-37-111921-wk13-threads-garbage-collection)
    - [Subtitle #1](#subtitle-1-30)
  - [Lecture 38, 11/22/21 (Wk14): Continued from Friday](#lecture-38-112221-wk14-continued-from-friday)
    - [Subtitle #1](#subtitle-1-31)
  - [Lecture 39, 11/30/21 (Wk15): Compression](#lecture-39-113021-wk15-compression)
    - [Subtitle #1](#subtitle-1-32)
  - [Lecture 40, 12/01/21 (Wk15): TBD](#lecture-40-120121-wk15-tbd)
    - [Subtitle #1](#subtitle-1-33)

## Lecture 1, 08/25/21 (Wk1): Intro, Hello World Java

### Grading
  
- **Homework/Labs:** ~10%	– 20
- **Projects:** ~50% – 100
- **Tests:** ~17% – 34
- **Final Exam:** ~23% – 46
- **Total:** ~100% – 200

### Methods (Functions)

- Function headers in Java specify the *types* of values *returned* by the function and taken as *parameters* to the functions
- `void` has no posisble values and returns nothing
- `String` is like Python's `str`
- `[]` means *array of*; an array is like a Python list but with a fixed size

### Selection & Access

- `Class.method`: `System.out.println` means "the method `println` that applies to the pbject references by the value of variable `System.out`
- **Public (exported) classes, methods, and variables** may be referred to anywhere else in the program; access permissions don't actually make the language more powerful, they just indicate whether something should be accessed or not
- **Static methods** and **static variables** are defined in the global frame

## Lecture 2, 08/27/21 (Wk1): A Little Programming

### Writing Programs

To write programs, one should either start with the highest level of abstraction and work downwards into its components **or** lay out its componenets and build into abstraction.

**The Main Method**

The main method of a java program is defined under `public static void main(String[] args)`.

*Writing methods inside the main method* is nearly impossible as nested functions are not supported in Java. *Tracing back through programs* is also considered to be bad practice, as Hilfinger pointed out in today's lecture. Alternatively, we should look through one iteration of a method and then refer to that method's comment, which is quite useful when looking at recursive methods.

### Example: printPrimes

**Task:** write a program that prints prime numbers up to and including a limit

**Definition:** a prime number is an integer greater than 1 that has no divisors smaller than itself other than 1: 2, 3, 5, 7, 11, etc.

```java
private static void printPrimes(int limit) {
  int np;  // notice that semicolons follow standalone lines
  np = 0;
  for (int p = 2; p <= limit; p += 1) {  // p initialized; p <= limit is the condition; p += 1 for each iteration
    if (isPrime(p)) {
      System.out.print(p + " ");  // print on same line
      n += 1;  // implementation of iteration
      if (np % 10 == 0)
        System.out.println();
    }
  }
  if (np % 10 != 0)  // if more than 10 prime numbers
    System.out.println();  // print newline
}
```

The `printPrimes` defined in lecture (not included here) is a **tail recursive method** given that, for a final result to be computed, frames opened for each recursive call are not dependent on the frame prior; that is, each frame that opens as a result of a recursive call *closes* either when a subsequent recursive call is made or if the method returns in that call.

We don't use recursion here because recursive calls are **expensive**. We should use iteration instead!

## Lecture 3, 08/30/21 (Wk2): Values and Containers

### Values and Containers

- **Values**: numbers, booleans, and pointers; values cannot change
  - Ex: `3`, `'a'`, `true`
- **Pointers**: point to containers; null points to nothing
- **Containers**:
  - **Simple Containers**: contain values; the contents of containers can change; are all named
  - **Structured Container**: contains (0 or more) other containers; are all anonymous; pointers point only to structured containers
    - Ex: Class object, Array Object, Empty Object
    - Structured containers contain only simple containers

### Primitive Operations

```java
public class IntList {
  // Constructor function (used to initialize new object)
  /** List cell containing (HEAD, TAIL). */
  public IntList(int head, IntList tail) {
    this.head = head; this.tail = tail;
}
```

- `IntList Q, L;` initialize empty list with names Q, L

- `L = new IntList(3, null);` L points to new list [3, null]
- `Q = L;` Q points to L; **it's the same object!** (very important)

- `Q = new IntList(42, null);` Q is now [42, null]
- `L.tail = Q;` the end of L is now Q, and L is [3, 42, null]

- `L.tail.head += 1;` the value of the head of the end of L, 42, is now 43
- Now `Q.head == 43` and `L.tail.head == 43`


### Destructive vs. Non-destructive

**Side note:** Instance variables should always be private!

A method is `non-destructive` when it leaves the input objects unchanged, whereas a `destructive` method may modify the input objects so that the original data is no longer available.

**Example: Non-destructive IncrList**

```java
/** List of all items in P incremented by n. */
static IntList incrList(IntList P, int n) {
  if (P == null)
    return null;
  else return new IntList(P.head+n, incrList(P.tail, n));
}
```

**Example: Destructive IncrList**
```java
static IntList incrList(IntList P, int n) {
  if (P == null)  // if the list is empty
    return null;
  IntList result, last;
  result = last = new IntList(p.head+n, null);
  while (P.tail != null) {
    P = P.tail;
  }
}
```

## Lecture 4, 09/01/21 (Wk2): Simple Pointer Manipulation

### The "Final" Keyword

In Java, the keyword **final** in a variable declaration means that the variable’s value may not be changed after the variable is initialized.

### Examples of Destructive Incrementing

Check out the [lecture slides from today](https://inst.eecs.berkeley.edu/~cs61b/fa21/materials/lectures/lect4.pdf)

## Lecture 5, 09/03/21 (Wk2): Arrays

### Arrays
  
An array is a structured container whose components are

- length, a fixed iteger
- a sequence of length simple containers of the same type, numbered from 0
- (.length field usually implicit in diagrams)

Arrays are **anonymous**, like other structured containers, and are always **referred to with pointers**

As an example, for an array pointed to by `A`,

- Length is `A.length`
- Numberered component `i` is `A[i]` (i is the index)
- Important feature: index can be any integer expression

```java
// Array Syntax
int[] q;
q = new int[] { 1, 2, 3 };

// Short form for delcarations
int[] r = { 7, 8, 9 };
```

### Insert Into an Array

The logic:

- start from the last element of an array `arr`, `arr.length - 1`
- move the last element to the right 1 and the element before it into the last element's place
  - stop doing this once you've hit the index in the list where you want to insert a value
- `arr[k] = 'new element that you want to insert'`


### Java Shortcut

Can write just `arraycopy` by including at the top of the
source file:

`import static java.lang.System.arraycopy;`

### Multidimensional Arrays

Multidimensional arrays are not primitive in Java, but we can build them with arrays of arrays!

```java
int[][] A = new int[3][];
A[0] = new int[] {2, 3, 4, 5};
A[1] = new int[] {4, 9, 16, 25};
A[2] = new int[] {8, 27, 64, 125};
```


## Lecture 6, 09/08/21 (Wk3): Developing a Sort, Unit Testing

### Multidimensional Arrays (continued)

- Since every element of an array is independent, there is no single "width" in general
  - Multidimensional arrays can take on any M x N format (think matricies in EECS 16A!)

### How do We Know If it works?

- **Unit testing** - testing of individual units (methods) within a program, rather than the whole program
- **Module testing** - testing of classes or other groupings of methods and data
- **System testing (acceptance testing)** - testing of the functionality of an entire program
- **Integration testing** - intermediate between unit and system testing, tests that modules work correctly together.
- **Regression testing** - testing with the specific goal of the cheking that fixes, enhances, or makes other changes that have not introduced faults (regressions)

### Testing Workflow (Test Driven Development)

**Test Driven Development:** write your tests *before* you write the methods

- In a unit test, give a bunch of arrays to sort and then make sure they each get sorted properly
- **Check for edge cases:**
  - empty array, one-element, all elements the same
- **Check for "middle" cases:**
  - Elements reversed, elements in order, one pair of elements reversed
- Then, write the method: test the method: refactor if necessary

### JUnit: Explained

- Provides some handy tools for unit testing
- `@Test` is java annotation (which provides information about a method, clsas, etc., that can be examined within Java itself) that tells the JUnit machinery to call a method
- In the testing method, you'll have a collection of methods with names beginning with `assert` then allow your test cases to check conditions and report failures

The main method will run all of the test cases in a given class:
```java
public static void main (String... args) {
  ucb.junit.textui.runClasses(SortTesting.class);
}
```


## Lecture 7, 09/10/21 (Wk3): Object-Based Programming

### Subtitle #1
  
-

## Lecture 8, 09/13/21 (Wk4): Object-oriented Mechanisms

### Subtitle #1
  
-

## Lecture 9, 09/15/21 (Wk4): Interfaces and Abstract Classes

### Subtitle #1
  
-

## Lecture 10, 09/17/21 (Wk4): Interfaces and Abstract Classes

### Subtitle #1
  
-

## Lecture 11, 09/20/21 (Wk5): Examples: Comparable and Reader

### Subtitle #1
  
-

## Lecture 12, 09/22/21 (Wk5): Additional OOP Details, Exceptions

### Subtitle #1
  
-

## Lecture 13, 09/24/21 (Wk5): Packages, Access, Loose Ends

### Subtitle #1
  
-

## Lecture 14, 09/27/21 (Wk6): Integers

### Subtitle #1
  
-

## Lecture 15, 09/29/21 (Wk6): Integers

### Subtitle #1
  
-

## Lecture 16, 10/01/21 (Wk6): Complexity

### Subtitle #1
  
-

## Lecture 17, 10/04/21 (Wk7): Collections, Amortization

### Subtitle #1
  
-

## Lecture 18, 10/06/21 (Wk7): Sequences, Some Design Patterns

### Subtitle #1
  
-

## Lecture 19, 10/08/21 (Wk7): Sequences (II)

### Subtitle #1
  
-

## Lecture 20, 10/11/21 (Wk8): Trees

### Subtitle #1
  
-

## Lecture 21, 10/13/21 (Wk8): Tree searching

### Subtitle #1
  
-

## Lecture 22, 10/03/21 (Wk8): Game trees

### Subtitle #1
  
-

## Lecture 23, 10/18/21 (Wk9): Priority Queues, Range Queries

### Subtitle #1
  
-

## Lecture 24, 10/20/21 (Wk9): Hashing

### Subtitle #1
  
-

## Lecture 25, 10/22/21 (Wk9): Generics

### Subtitle #1
  
-

## Lecture 26, 10/25/21 (Wk10): Sorting

### Subtitle #1
  
-

## Lecture 27, 10/27/21 (Wk10): Sorting (II)

### Subtitle #1
  
-

## Lecture 28, 10/29/21 (Wk10): Sorting (III)

### Subtitle #1
  
-

## Lecture 29, 11/01/21 (Wk11): Balanced Search Structures

### Subtitle #1
  
-

## Lecture 30, 11/03/21 (Wk11): Review (and it's my birthday!)

### Subtitle #1
  
-

## Lecture 31, 11/05/21 (Wk11): Balanced Search Structures (II)

### Subtitle #1
  
-

## Lecture 32, 11/08/21 (Wk12): Git Internals

### Subtitle #1
  
-

## Lecture 33, 11/10/21 (Wk12): Graphs, Introduction, Traversals

### Subtitle #1
  
-

## Lecture 34, 11/12/21 (Wk12): A* Search, Minimal spanning trees, Union-find

### Subtitle #1
  
-

## Lecture 35, 11/15/21 (Wk13): Pseudo-Random Sequences

### Subtitle #1
  
-

## Lecture 36, 11/17/21 (Wk13): Dynamic Programming, Enumeration Types

### Subtitle #1
  
-

## Lecture 37, 11/19/21 (Wk13): Threads, Garbage Collection

### Subtitle #1
  
-

## Lecture 38, 11/22/21 (Wk14): Continued from Friday

### Subtitle #1
  
-

## Lecture 39, 11/30/21 (Wk15): Compression

### Subtitle #1
  

## Lecture 40, 12/01/21 (Wk15): TBD

### Subtitle #1
  
-