# Assignment 5

## A

### i: Explain why α can be interpreted as a categorical probability distribution.

Alpha is a vector of values between one and zero that sum to one, like a probability distribution.
Its categories are the input tokens.
It is decribing the probability that particular token will be relevant to the meaning of another token

### ii: Describe (in one sentence) under what conditions the categorical distribution α puts almost all of its weight on some αj

K transpose Q must be near 1 for αj and have a low value for other α's. That is K & Q must be very similar for j, but not for other indices.

### iii: Under the conditions you gave in (ii), describe the output c.

C would approximately be equal to αj

### iv: Explain (in two sentences or fewer) what your answer to (ii) and (iii) means intuitively.

If a key if very similar to a query, and no other query closely matches a key, then the value of the matching query will dominate the attention head.

## B

### i

We're looking for a matrix such that when M(Va + Vb) = Va, for all Va & Vb in orthogonal subspaces

M is going to be a d x d matrix because it has to multiply Va & Vb.

Va = c1 x a1 + c2 x a2 ... = Ac
Vb = c'1 x b1 + c'2 x b2 ... = Bc'

We want all the c1 ... to = 1 so they leave Va unchanged

Atranspose x B = 0 because they are orthogonal subspaces

### ii

## C Drawbacks of single headed attention
