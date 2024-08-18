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

[Given as an image from my notebook]
