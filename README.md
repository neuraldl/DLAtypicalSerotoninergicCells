# Deep Learning Models for Atypical Serotoninergic Cells Recognition
Corradetti Daniele, Bernardi Alessandro, Corradetti Renato

## Overview
Traditional methods for identifying serotonergic neurons are based on specific electrophysiological characteristics, yet this approach often overlooks atypical neurons, thus limiting our understanding of the serotonergic system's diversity. To address this, we propose deep learning models capable of recognizing both typical and atypical serotonergic and non-serotonergic neurons with high accuracy.
The research utilized electrophysiological recordings from dorsal raphe nucleus slices of transgenic mice, expressing fluorescent proteins specific to the serotonergic system. These recordings formed the basis of the training, validation, and testing data for the deep learning models. The study employed convolutional neural networks (CNNs), known for their efficiency in pattern recognition, to classify neurons based on the specific characteristics of their action potentials. The models were trained on a dataset comprising 43,327 original spike samples, alongside an extensive set of 6.7 million synthetic spike samples, designed to mitigate the risk of overfitting the background noise in the recordings, a potential source of bias. Results showed that the models achieved high accuracy and were further validated on "non-homogeneous" data, i.e., data not used for constructing the model, to confirm their robustness and reliability in real-world experimental conditions.

## Contents
In this github respository are available the following: 
\begin{enumerate}
\item the .abf recordings of original training data and the non-homogenous
data,
\item the 43,327 single spikes samples of the orginal training data stored
in .csv files of 160 points,
\item the 24,616 single spikes samples of the non-homogenous data stored
in .csv files of 160 points,
\item the 6,675,300 million single spikes samples of the synthetic data
stored as numpy vector,
\item the trained models with different kernels,
\item the results of the models,
\item the Python notebooks for training of the models and for inference.
\end{enumerate}

## Data Requirements
Libraries: TensorFlow version 2.14
Download on your local or cloud device below folders:

### Biological Data 

SER Cellulars  https://drive.google.com/drive/folders/1OH8HZlfHk17qekf3vjGcXjaARikYGg2E?usp=sharing

NSER Cellulars https://drive.google.com/drive/folders/1SzHVo5lmmJy1U2PvwYhHpvdnFpe9lCyP?usp=sharing

ModelsDNN https://drive.google.com/drive/folders/154nndEf4CnArvT-NpJzNA-eXTmmNJAT7?usp=sharing

### Synthetic Data

SER Cellulars https://drive.google.com/drive/folders/1k0vLhHIA7Aq0MQZzaan4QeCCEGG69IqL?usp=sharing

NSER Cellulars https://drive.google.com/drive/folders/1i-9tDp-YaFlCy4yZ7F55Ssy8vNzyhm84?usp=sharing

### Biological Data Non Homogeneous 

SER Cellulars https://drive.google.com/drive/folders/1XyLrbP1sxxOk67H8gqVojcj1wM53QXkn?usp=sharing

NSER Cellulars https://drive.google.com/drive/folders/1-4eZgkowcaDTr8z4ylcT5YxMkn3OPStD?usp=sharing

