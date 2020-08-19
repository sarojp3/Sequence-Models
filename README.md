# Sequence-Models

Sequence Models have sequence data as both input and output. Such models are used in speech recognition, music generation, sentiment analysis, machine translation, video acitvity recognition, name-entity recognition and many more. All these can be addressed as a supervised learning with labeled data X and Y as training set.

## Recurrent Neural Network

Using a standard neural network for sequence data donot work well because inputs and outputs can be of different lengths in different examples. Also, it doesnot share features learned across different positions of texts. That is why we use Recurrent Neural Network for such problems. In this neural network, the parameters used in each time steps are shared because it uses the information that is earlier in the sequence to make a prediction.
