COMP3031 Assignment 3
=====================

HKUST COMP3031 Principles of Programming Languages (2013 Fall) Assignment 3

=====================
Question 1. Odd number list (15 points)

Define a relation odd_list (X,Y) such that Y is a list of all odd numbers that are less than X. X is a natural number and is always given. Assume users always give valid input.

Examples:

```
?- odd_list(1,Y).

Y = [].

?- odd_list(12,Y).

Y = [1, 3, 5, 7, 9, 11].

?- odd_list(13,Y).

Y = [1, 3, 5, 7, 9, 11].
```

=====================
Question 2. Next triangular number (15 points)

A triangular number is the sum of n consecutive natural numbers from 1 to n, e.g. T(n) = 1 + 2 + 3 + ... + n. Define a relation nexttri(X,Y) such that Y is the least triangular number that is greater than X. Assume X is a natural number and is always given. Assume users always give valid input.

Examples:

```
?- nexttri(1,3).

true.

?- nexttri(6,Y).

Y = 10.
```

=====================
Question 3. List difference (15 points)

Define a relation list_diff(A,B,X) where all items in A but no item in B occur in X. Order in the list is not important. Assume users always give valid input.

Examples:

```
?- list_diff([1,2,3,4],[1,2],X).

X = [3, 4].

?- list_diff([7,1,5,3,1],[1,2],X).

X = [7, 5, 3].

?- list_diff([a,a,b], [b],X).

X = [a, a].
```

=====================
Question 4. Merging two integer lists (25 points)

Define a relation list_merge (X,Y,Z) where X and Y are integer lists, Z contains all elements from both X and Y, and there is no duplicate in Z. Assume both X and Y are given. Order in the list is not important. Assume users always give valid input.

Examples:

```
?- list_merge([],[],L).

L = [].

?- list_merge([1],[1],L).

L = [1].

?- list_merge([],[1,3,1,1,1],L).

L = [1, 3] .

?- list_merge([5,3,1,2,1],[7,3,2,5,7],L).

L = [5, 7, 3, 2, 1] .
```

=====================
Question 5. And-Or expressions (30 points)

Implement two relations and(A,B) and or(A,B) that perform the logical ?œAND??and the logical ?œOR??operations on two Boolean operands A and B. Relation and(A,B)holds if A and B both evaluate to true. Relation or(A,B)holds if either A or B evaluates to true, or both A and B evaluate to true. An And-OR expression can be nested, e.g., and(or(A,B),and(C,D)). For simplicity, assume each variable appears only once (i.e., there will be no input as and(or(A,B),and(A,C)) where variable A appears twice). Given a query with variables, the user will get all possible answers one by one by typing????(see the examples below for an illustration). Order in the answers is not important. 

Assume users always give valid input.

Examples:

```
?- and(true,false).

false.

?- or(true,false).

true;

false.

?- and(A,true).

A = true ;

false.

?- or(A,B).

A = true ;

B = true ;

false.

?- and(or(A,B),and(C,D)).

A = true,

C = true,

D = true ;

B = true,

C = true,

D = true ;

false.

?- or( and(or(A,B),C), or(and(D,E),or(F,G)) ).

A = true,

C = true ;

B = true,

C = true ;

D = true,

E = true ;

F = true ;

G = true ;

false.
```
