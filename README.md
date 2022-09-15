# Nueral_Machine_Translation_Eng_to_Hin
Using Sq2Sq LSTM based model alsg with attension 

## Data Sets:

- Go to this page: http://workshop.colips.org/news2018/dataset.html
- Under the “NEWS2018 DATASET_04” section, you will find Hindi mentioned.
- Press the “request data” link to register &amp; get the download link.
- After downloading the dataset, have a look at the Hindi training set and validation set XML files.

# Model Building

- About LSTM 
LSTM stands for “long short-term memory.” (Quick aside: talk about one of the coolest names in all of machine learning!)

Right, so an LSTM network is a special kind of recurrent neural network (RNN). One way to motivate LSTMs is to think about RNNs that suffer from vanishing gradients. Gradients contain information, and over time if gradients vanish important localized information is lost. This is an issue for a famous application of RNNs, understanding language.

One odd way of thinking about language / sentences: they contain long-term dependencies. This happens for many reasons, but one reason is because of concrete grammar rules.

Consider these two sentences:

The man drives away.
The man, after robbing a bank and rushing to his car, drives away.
We know that the correct verb form is “drives” because the subject is singular (“the man”). This is an example of a concrete long-term dependency. For RNNs, you want to make sure that the network “remembers” that the subject is singular, so that it knows to predict the correct verb form.

This is where the LSTM comes in. LSTMs are a more general version of a gated recurrent unit (you might have heard of GRUs). The idea here is that the LSTM module has multiple “gates” inside of it with trained parameters. Some of these gates control the modules “output” and other gates control “forgetting.” In this way the LSTM helps remember cell states.

Hopefully this helps. Several people recommend reading this to learn more, but I often find pictures like this to make things more complicated. LSTMs are really one of the few places in my experience where the math is easier than the diagrams like this


- Sq2Sq Encoder and Decoder based Model

<p align = 'center'>
  <img src = './utils/MLT.jpg' align = 'center'>
</p>

- Introduce Attention 


