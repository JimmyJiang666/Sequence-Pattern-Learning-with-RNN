# Sequence-Pattern-Learning-with-RNN

main.ipynb demonstrates how to learn the output of a sequence of numbers. In this case, the sequences are of length 2 and have the form [x,y] where x,y ∈ {0,··· ,p − 1} and the output is (x − y) mod p for some integer p. Note that we do one-hot encoding of the outputs.

1. Use this idea to train a network which given a sequence of integers [x0, · · · , xk−1] where xi ∈{0,1,···,p−1}outputs(x0−x1+x2−···+(−1)k−1xk−1)modp. Youcanassume that the input sequences have length at most 5 and any shorter sequence can be padded with 0’s so that it has length 5.

2. Any text can thought of as a long string of characters and if we map each character to an integer we can think of the text as a sequence of characters. In particular, if a text T of length n has m distinct characters then we can map it to a sequence of integers x0,··· ,xn−1 where xi ∈ {0,··· ,m − 1}. Once we have such a sequence, we can define a sequence prediction problem where given any k consecutive elements [xi, xi+1, · · · , xi+k−1], the goal is to predict the next one xi+k.

− Use the above idea to train a network on a large text (e.g. this text.).

− Use the trained model to generate text as follows: set [x0, · · · , xk−1] as you wish and the repeatedly use the model to predict the next element from the previous k. Note that the model actually predicts a probability distribution on the next element - you should pick the next element randomly according to this distribution.
