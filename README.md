# Intro to Encoder-Decoder model and the Attention mechanism

# A neural machine translator from english to spanish short sentences in tf2

In this repository we will be implementing a simple encoder decoder model with Tensorflow 2 to familiarize ourselves with the sequence-to-sequence architecture. We are going to describe the basic architecture of an encoder-decoder model that we will apply to a neural machine translation problem, translating texts from English to Spanish. Later, we will introduce a technique that has been a great step forward in the treatment of NLP tasks: the attention mechanism. We will detail a basic processing of the attention applied to a scenario of a sequence-to-sequence model, "many to many" approach. But for the moment it will be a simple attention model, we will not comment on more complex models that will be discussed in future posts, when we address the subject of Transformers.

## The data set

For this exercise we will use pairs of simple sentences, the source in English and target in Spanish, from the Tatoeba project where people contribute adding translations every day. This is the [link](http://www.manythings.org/anki/) to some traslations in different languages. There you can download the Spanish - English spa_eng.zip file, it contains 124457 pairs of sentences. The data is also available in the data folder in this repo.

The text sentences are almost clean, they are simple plain text, so we only need to remove accents, lower case the sentences and replace everything with space except (a-z, A-Z, ".", "?", "!", ","). The code to apply this preprocess has been taken from the Tensorflow tutorial for neural machine translation.

## Problem description

*Machine translation (MT) is the task of automatically converting source text in one language to text in another language. Given a sequence of text in a source language, there is no one single best translation of that text to another language. This is because of the natural ambiguity and flexibility of human language. This makes the challenge of automatic machine translation difficult, perhaps one of the most difficult in artificial intelligence.*

From the above we can deduce that NMT is a problem where we process an input sequence to produce an output sequence, that is, a sequence-to-sequence (seq2seq) problem. Specifically of the many-to-many type, sequence of several elements both at the input and at the output, and the encoder-decoder architecture for recurrent neural networks is the standard method.

## Content
This repository contains the next source code file:
- Intro-seq2seq-Encoder-Decoder-ENG-SPA-translator-tf2: This notebook shows how to download and preprocess the text data, create a batch data generator for sequences of data, define and build a **encoder decoder architecture using LSTM units**. Then, we describe the attention mechanism and build a **decoder with the Luong's Attention** and train it for our problem.

## Contributing
If you find some bug or typo, please let me know or fixit and push it to be analyzed. 

## License

These notebooks are under a public GNU License.