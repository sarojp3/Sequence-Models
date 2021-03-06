# Sequence-Models

Sequence Models have sequence data as both input and output. Such models are used in speech recognition, music generation, sentiment analysis, machine translation, video acitvity recognition, name-entity recognition and many more. All these can be addressed as a supervised learning with labeled data X and Y as training set.

## Recurrent Neural Network

Using a standard neural network for sequence data donot work well because inputs and outputs can be of different lengths in different examples. Also, it doesnot share features learned across different positions of texts. That is why we use Recurrent Neural Network for such problems. In this neural network, the parameters used in each time steps are shared because it uses the information that is earlier in the sequence to make a prediction. There are different RNN architectures like Many-to-Many, Many-to-One, One-to-One, and One-to-Many. Also, we can build deep RNNs by just stacking the layers of RNN on top of each other but very deep RNNs is not used. Only some few layers are used.

## Gated Recurrent Unit(GRU)

It is one of the effective solution for vanishing gradient problem in the Recurrent Neural Network and will allow neural network to capture much longer range dependencies(connections) in a sequence. GRU address the issue of vanishing gradient problem by storing memory from the previous time step to help inform the network for future prediction. It have a memory cell 'c' which provides a bit of memory to remember. 

The main idea of GRU is that there will be a gate called update gate whose job is to decide when to update the values of c at each time step. This gate will be a value of either 0 or 1. If value of gate is equal to 1, it is saying to set the new value of c to that candidate value c tilde.
c tilde is the candidate for replacing c at each time step.

## Long-Short Term Memory(LSTM)

It is also a solution for vanishing gradient descent like GRU which has been historically more proven choice to use which is more powerful, effiecnt than GRU. LSTM is also a more general version of GRU. The model is a bit similar to the GRU but it uses extra two gates forget gate and output gate. These gates is a vector of dimensions equal to the number of hidden units in a layer. 

Both LSTM as well as GRU are good at memorizing certain values for a long time because some values of c at previous time step is passed all the way forward.

## Bi-directional Recurrent Neural Network(BRNN)

This neural network takes the information from the previous time steps as well as from the future time steps to make predictions. Note that, it donot perform backward propagation insted it uses backward sequence computation to get activations for backward sequence. For most of the NLP problems, bidirectional RNN with LSTM model is used most often but this model is not useful for machine translation and speech recognition.

# Natural Language Processing(NLP) and Word Embeddings

For natural language processing, we will use word embedding technique where we will use featurized representation of each words and then embed it to a 2D space so that we can visualize them. One of the common algorithm for that is t-SNE algorithm. In the visualization, we can see the grouping of similar word or close to similar words. We will use cosine similarity fuction to detect the similarity of the words. Basic neural language model is a reasonable way to learn a set of embeddings.

The algorithms which is widely used for natural language processing are Word2Vec Algorithm(Skip-Gram Model) and GloVe Word Vector Model along with negative sampling technique.

## Sequence-to-Sequence Architecture

Such models are useful for everything from machine translation to speech recognition. The basic architecture for this model consists of a encoder which only takes the whole input sequence 'X' and a decoder which then converts that input into required format using RNN/LSTM/GRU. This is used in machine translation to translate from one language to another language. Mainly used algorithm for machine translation purpose is Beam Search Algorithm which is an approximate Optimization Algorithm.

### Attention Model

This model translated maybe a bit more like humans by looking at part of the sentence at a time and by working on one part of the sentence at a time, it won't have to memorize long sequences. Attention model allows a neural network to pay attention to only a part of an input sequence ehile it is generating a translation. One downside of this algorithm is that it runs in a quadratic time.
