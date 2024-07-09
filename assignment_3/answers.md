# 1

## A

i) With Beta1 set to 0.9, 90% of the size of the update will be the rolling average of
the rate of change of the error with respect to the parameters, and only 10% the specific
rate of change from this minibatch. This means that if the current minibatch is an outlier
in terms of the parameter update, its effect will be diluted.

ii) v adjusts the learning rate alpha so that if there are large gradients bigger steps are taken.
There will be larger updates when the absolute magnitude of the gradients are higher, and when the
rolling average of previous gradients have been higher

## B

i) Gamma needs to increase the values of the non-dropped out units in proportion to the number of dropped out units. That means:

gamma = 1/(1-p_drop)

ii) Drop out will drop out units at random during training to prevent over fitting. Different units will be dropped out during each batch. At evaluation, the goal is to test the whole model, so all units should be included.

# 2.

## A

| Stack                          | Buffer                                 | New dependency   | Transition            |
| ------------------------------ | -------------------------------------- | ---------------- | --------------------- |
| [ROOT]                         | [I, parsed, this, sentence, correctly] |                  | Initial Configuration |
| [ROOT, I]                      | [parsed, this, sentence, correctly]    |                  | SHIFT                 |
| [ROOT, I, parsed]              | [this, sentence, correctly]            |                  | SHIFT                 |
| [ROOT, parsed]                 | [this, sentence, correctly]            | parsed→I         | LEFT-ARC              |
| [ROOT, parsed, this]           | [sentence, correctly]                  |                  | SHIFT                 |
| [ROOT, parsed, this, sentence] | [correctly]                            |                  | SHIFT                 |
| [ROOT, parsed, sentence]       | [correctly]                            | sentence→this    | LEFT-ARC              |
| [ROOT, parsed]                 | [correctly]                            | parsed→sentence  | RIGHT-ARC             |
| [ROOT, parsed, correctly]      | []                                     |                  | SHIFT                 |
| [ROOT, parsed]                 | []                                     | parsed→correctly | RIGHT-ARC             |
| [parsed]                       | []                                     | ROOT→parsed      | RIGHT-ARC             |

## B

It takes 2n steps, because each word has to be moved the Stack and then given a dependence.

Could think of it as 2n+1 because of the ROOT item, which starts in the Stack

## C

In parser_transistions.py

## D

In parser_transitions.py

## E

In parser_transitions.py

## F

In parser_transitions.py
