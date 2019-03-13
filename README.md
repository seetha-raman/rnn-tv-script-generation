# Deep Learning - RNN - Generate TV Scripts

This is RNN implemenataion of Generating TV scripts. Model is using part of the Seinfeld dataset of scripts from 9 seasons. 
The Neural Network model generates a new ,"fake" TV script, based on patterns it recognizes in this training data 

Below are some samples of newly generated TV scripts:
```
jerry: i'm gonna be in the mood with the show, but you have a lot of money.

george: i don't know how to be in a lot of people, but you know what? i mean, the only way to be the most important thing about the other day.

george: oh, i got to get it to the game.

george: what is this. you know what i want?

jerry: well, i don't have it.

kramer: well, i don't think so.

jerry: what about this?

george: i think it's a little good..

hoyt: so, uh- you are a maid of humor?

jerry: yeah, yeah. i mean, i was just in my house.

jerry: what is that?

elaine: i think that's it.

chiles: you know what i said.

george: i thought you were talking with him.

hoyt: and the doctor was a real little.

jerry: i don't know what this is.

elaine: oh...(laughs)

chiles: hey, george, i don't think so.

elaine: you know the guy, uh... i think it's a good one.

george: i know, but i don't have to talk.

jerry: what?

elaine: i think you can get a little.

jerry: you know what? i think i can get a little to see a little problem with this.

hoyt: what do you mean?

jerry: i can't do that, but i don't know how i can tell you, this is not that.

elaine: i was thinking.

george: well, i can't get out of the car.

jerry: you know what this means, you were a man, and you know that i could get the one in the world.

kramer: yeah, that's right.

jerry: what are you gonna do?

elaine: i don't want
```


There are 2 main parts of this model:

1. **Pre-Processing**: split TV scripts into word, construct lookup table, encode and create Data Loader for training data

2. **RNN**: LSTM Model - Given a vocab_size, output_size, embedding_dim, hidden_dim, n_layers and dropout, construct RNN model and train model with the TV scripts. 

## Repository 

This repository contains:
* **dlnd_tv_script_generation.ipynb** : Complete code for pre-processing and batching data, creating Data Loader, building RNN - LSTM, training RNN, and generate the TV Scripts
					  
## Datasets

Datasets necessary for this implementation can be downloaded from **./data/Seinfeld_Scripts.txt**

## List of Hyperparameters used:

* Embedding Dimensions = **400**
* Hidden Dimensions  = **512**   
* Number of Layers = **2**  

* Sequence Length = **12**
* Batch Size  = **128**   
* Epoch = **10**  
  
* Vocabulary Size = **Length of vocab_to_int map + padding**  
* Output Size = **Equal to vocab_size**  

* Loss Function = **CrossEntropyLoss**  
* Optimizer  = **Adam**  
* Learning Rate = **0.001**  

