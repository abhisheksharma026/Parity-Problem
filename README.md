# Parity-Problem
Parity-Problem using RNN

## Problem Statement
Let us define a sequence parity function as a function that takes in a sequence of binary inputs and returns a sequence indicating the number of 0’s in the input so far; specifically, if at time t the 0’s in the input so far is odd it returns 1, and 0 if it is even. For example, given input sequence [0, 1, 0, 1, 1, 0], the parity sequence is [1, 1, 0, 0, 0, 1].

Implement the minimal vanilla recurrent neural network to learn the parity function. Explain your rationale using a state transition diagram and parameters of the network.

## Thought Process:
- Each parity bit is the XOR of the input and the previous parity bit.
- Parity is a classic example of a problem that’s hard to solve with a shallow feed-forward net, but easy to solve with an RNN.
## Strategy:
- The output unit tracks the current parity, which is the XOR of the current input and previous output.
- Let’s use hidden units to help us compute XOR. Have one unit compute AND, and the other one compute OR.
