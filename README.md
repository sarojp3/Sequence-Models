# Sequence-Models

Sequence Models have sequence data as both input and output. Such models are used in speech recognition, music generation, sentiment analysis, machine translation, video acitvity recognition, name-entity recognition and many more. All these can be addressed as a supervised learning with labeled data X and Y as training set.

## Recurrent Neural Network

Using a standard neural network for sequence data donot work well because inputs and outputs can be of different lengths in different examples. Also, it doesnot share features learned across different positions of texts. That is why we use Recurrent Neural Network for such problems. In this neural network, the parameters used in each time steps are shared because it uses the information that is earlier in the sequence to make a prediction. There are different RNN architectures like Many-to-Many, Many-to-One, One-to-One, and One-to-Many. 

## Gated Recurrent Unit(GRU)

It is one of the effective solution for vanishing gradient problem in the Recurrent Neural Network and will allow neural network to capture much longer range dependencies(connections) in a sequence. GRU address the issue of vanishing gradient problem by storing memory from the previous time step to help inform the network for future prediction. It have a memory cell 'c' which provides a bit of memory to remember. The main idea of GRU is that there will be a gate whose job is to decide when to update the values of c at each time step. This gate will be a value of either 0 or 1. If value of gate is equal to 1, it is saying to set the new value of c to that candidate value c tilde.
