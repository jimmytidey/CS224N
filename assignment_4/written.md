# PART 1, section g

The masking sets all padding tokens to -infinity in the attention tensor.

This prevents the model from paying attention to the padding tokens

## section i

-- Dot product attention is less learnable (is not parameterised), but simple to compute
-- Multiplicative attention is more complex, but has paramteres that can be leanred
-- Additive attention has even more paramters, separeate ones for the input and output representation, allowing even more complexity in what the network can learn

# PART 2

## A

The 1D convolutional layer has a moving window that allows it to encode pairs of carachters together. I think this is more robust in a language without spaces (chinese) than using sentencepiece. This is because common pairs of carachters in chinese may simply be words that often appear together, not carachters combining to form 'words'.

## B

### i

The phrase at the beggining only occurs twice in the training data. They were setenced for theft, not to theft, but perhaps the attnetion has failed because the concepts are in the opposite order in Chinese

### ii

It seems like the first clause has been forgotten and in the translation, and the clause repeated twice.

### iii

It seems 国殇日 is a specific phrase for national day of mourning. Perhaps the CNN failed to caputure this unique word properly

### iv

"Act not, err not" is very idomatic and usual, perhaps that is why the NMT failed
