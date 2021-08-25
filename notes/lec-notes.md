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
    - [Subtitle #1](#subtitle-1)
  - [Lecture 3, 08/30/21 (Wk2): Values and Containers](#lecture-3-083021-wk2-values-and-containers)
    - [Subtitle #1](#subtitle-1-1)
  - [Lecture 4, 09/01/21 (Wk2): Simple Pointer Manipulation](#lecture-4-090121-wk2-simple-pointer-manipulation)
    - [Subtitle #1](#subtitle-1-2)
  - [Lecture 5, 09/03/21 (Wk2): Arrays](#lecture-5-090321-wk2-arrays)
    - [Subtitle #1](#subtitle-1-3)
  - [Lecture 6, 09/08/21 (Wk3): Developing a Sort, Unit Testing](#lecture-6-090821-wk3-developing-a-sort-unit-testing)
    - [Subtitle #1](#subtitle-1-4)
  - [Lecture 7, 09/10/21 (Wk3): Object-Based Programming](#lecture-7-091021-wk3-object-based-programming)
    - [Subtitle #1](#subtitle-1-5)
  - [Lecture 8, 09/13/21 (Wk4): Object-oriented Mechanisms](#lecture-8-091321-wk4-object-oriented-mechanisms)
    - [Subtitle #1](#subtitle-1-6)
  - [Lecture 9, 09/15/21 (Wk4): Interfaces and Abstract Classes](#lecture-9-091521-wk4-interfaces-and-abstract-classes)
    - [Subtitle #1](#subtitle-1-7)
  - [Lecture 10, 09/17/21 (Wk4): Interfaces and Abstract Classes](#lecture-10-091721-wk4-interfaces-and-abstract-classes)
    - [Subtitle #1](#subtitle-1-8)
  - [Lecture 11, 09/20/21 (Wk5): Examples: Comparable and Reader](#lecture-11-092021-wk5-examples-comparable-and-reader)
    - [Subtitle #1](#subtitle-1-9)
  - [Lecture 12, 09/22/21 (Wk5): Additional OOP Details, Exceptions](#lecture-12-092221-wk5-additional-oop-details-exceptions)
    - [Subtitle #1](#subtitle-1-10)
  - [Lecture 13, 09/24/21 (Wk5): Packages, Access, Loose Ends](#lecture-13-092421-wk5-packages-access-loose-ends)
    - [Subtitle #1](#subtitle-1-11)
  - [Lecture 14, 09/27/21 (Wk6): Integers](#lecture-14-092721-wk6-integers)
    - [Subtitle #1](#subtitle-1-12)
  - [Lecture 15, 09/29/21 (Wk6): Integers](#lecture-15-092921-wk6-integers)
    - [Subtitle #1](#subtitle-1-13)
  - [Lecture 16, 10/01/21 (Wk6): Complexity](#lecture-16-100121-wk6-complexity)
    - [Subtitle #1](#subtitle-1-14)
  - [Lecture 17, 10/04/21 (Wk7): Collections, Amortization](#lecture-17-100421-wk7-collections-amortization)
    - [Subtitle #1](#subtitle-1-15)
  - [Lecture 18, 10/06/21 (Wk7): Sequences, Some Design Patterns](#lecture-18-100621-wk7-sequences-some-design-patterns)
    - [Subtitle #1](#subtitle-1-16)
  - [Lecture 19, 10/08/21 (Wk7): Sequences (II)](#lecture-19-100821-wk7-sequences-ii)
    - [Subtitle #1](#subtitle-1-17)
  - [Lecture 20, 10/11/21 (Wk8): Trees](#lecture-20-101121-wk8-trees)
    - [Subtitle #1](#subtitle-1-18)
  - [Lecture 21, 10/13/21 (Wk8): Tree searching](#lecture-21-101321-wk8-tree-searching)
    - [Subtitle #1](#subtitle-1-19)
  - [Lecture 22, 10/03/21 (Wk8): Game trees](#lecture-22-100321-wk8-game-trees)
    - [Subtitle #1](#subtitle-1-20)
  - [Lecture 23, 10/18/21 (Wk9): Priority Queues, Range Queries](#lecture-23-101821-wk9-priority-queues-range-queries)
    - [Subtitle #1](#subtitle-1-21)
  - [Lecture 24, 10/20/21 (Wk9): Hashing](#lecture-24-102021-wk9-hashing)
    - [Subtitle #1](#subtitle-1-22)
  - [Lecture 25, 10/22/21 (Wk9): Generics](#lecture-25-102221-wk9-generics)
    - [Subtitle #1](#subtitle-1-23)
  - [Lecture 26, 10/25/21 (Wk10): Sorting](#lecture-26-102521-wk10-sorting)
    - [Subtitle #1](#subtitle-1-24)
  - [Lecture 27, 10/27/21 (Wk10): Sorting (II)](#lecture-27-102721-wk10-sorting-ii)
    - [Subtitle #1](#subtitle-1-25)
  - [Lecture 28, 10/29/21 (Wk10): Sorting (III)](#lecture-28-102921-wk10-sorting-iii)
    - [Subtitle #1](#subtitle-1-26)
  - [Lecture 29, 11/01/21 (Wk11): Balanced Search Structures](#lecture-29-110121-wk11-balanced-search-structures)
    - [Subtitle #1](#subtitle-1-27)
  - [Lecture 30, 11/03/21 (Wk11): Review (and it's my birthday!)](#lecture-30-110321-wk11-review-and-its-my-birthday)
    - [Subtitle #1](#subtitle-1-28)
  - [Lecture 31, 11/05/21 (Wk11): Balanced Search Structures (II)](#lecture-31-110521-wk11-balanced-search-structures-ii)
    - [Subtitle #1](#subtitle-1-29)
  - [Lecture 32, 11/08/21 (Wk12): Git Internals](#lecture-32-110821-wk12-git-internals)
    - [Subtitle #1](#subtitle-1-30)
  - [Lecture 33, 11/10/21 (Wk12): Graphs, Introduction, Traversals](#lecture-33-111021-wk12-graphs-introduction-traversals)
    - [Subtitle #1](#subtitle-1-31)
  - [Lecture 34, 11/12/21 (Wk12): A* Search, Minimal spanning trees, Union-find](#lecture-34-111221-wk12-a-search-minimal-spanning-trees-union-find)
    - [Subtitle #1](#subtitle-1-32)
  - [Lecture 35, 11/15/21 (Wk13): Pseudo-Random Sequences](#lecture-35-111521-wk13-pseudo-random-sequences)
    - [Subtitle #1](#subtitle-1-33)
  - [Lecture 36, 11/17/21 (Wk13): Dynamic Programming, Enumeration Types](#lecture-36-111721-wk13-dynamic-programming-enumeration-types)
    - [Subtitle #1](#subtitle-1-34)
  - [Lecture 37, 11/19/21 (Wk13): Threads, Garbage Collection](#lecture-37-111921-wk13-threads-garbage-collection)
    - [Subtitle #1](#subtitle-1-35)
  - [Lecture 38, 11/22/21 (Wk14): Continued from Friday](#lecture-38-112221-wk14-continued-from-friday)
    - [Subtitle #1](#subtitle-1-36)
  - [Lecture 39, 11/30/21 (Wk15): Compression](#lecture-39-113021-wk15-compression)
    - [Subtitle #1](#subtitle-1-37)
  - [Lecture 40, 12/01/21 (Wk15): TBD](#lecture-40-120121-wk15-tbd)
    - [Subtitle #1](#subtitle-1-38)

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

### Subtitle #1
  
-

## Lecture 3, 08/30/21 (Wk2): Values and Containers

### Subtitle #1
  
-

## Lecture 4, 09/01/21 (Wk2): Simple Pointer Manipulation

### Subtitle #1
  
-

## Lecture 5, 09/03/21 (Wk2): Arrays

### Subtitle #1
  
-

## Lecture 6, 09/08/21 (Wk3): Developing a Sort, Unit Testing

### Subtitle #1
  
-

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
  
-e

## Lecture 24, 10/20/21 (Wk9): Hashing

### Subtitle #1
  
-e

## Lecture 25, 10/22/21 (Wk9): Generics

### Subtitle #1
  
-e

## Lecture 26, 10/25/21 (Wk10): Sorting

### Subtitle #1
  
-e

## Lecture 27, 10/27/21 (Wk10): Sorting (II)

### Subtitle #1
  
-e

## Lecture 28, 10/29/21 (Wk10): Sorting (III)

### Subtitle #1
  
-e

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