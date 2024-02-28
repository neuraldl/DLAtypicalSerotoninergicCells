# Deep Learning Models for Atypical Serotoninergic Cells Recognition
[![Paper](https://img.shields.io/badge/version-1.0.1-blue)]() [![Paper](https://img.shields.io/badge/q--bio.NC-Paper-b31b1b?logo=arxiv&logoColor=red)](https://arxiv.org/) [![Paper](https://img.shields.io/badge/release-open_access-green)]()

> **Deep Learning Models for Atypical Serotoninergic Cells Recognition**<br>
>**Date**: February 28, 2024<br>
> [Corradetti Daniele](https://ualg.academia.edu/DanieleCorradetti), [Bernardi Alessandro](https://www.linkedin.com/in/alessandro-bernardi/), [Corradetti Renato](https://unifi.academia.edu/RenatoCorradetti)<br>
> *Grupo de Fisica Matematica, Instituto Superior Tecnico, Av. Rovisco Pais, Lisboa, 1049-001, Portugal*
> *Departamento de Matematica, Universidade do Algarve, Campus de Gambelas, Faro, 8005-139, Faro, Portugal*
> *Department of Neuroscience, Psychology, Drug Research and Child Health (NEUROFARBA), University of Florence, Viale G. Pieraccini 6, Firenze, 50139, Toscana, Italy*

This repository is aimed to collect the data and models used for *Deep Learning Models for Atypical Serotoninergic Cells Recognition* by Corradetti Daniele, Bernardi Alessandro, Corradetti Renato. The work proposes an innovative deep learning approach to accurately identify both typical and atypical serotonergic neurons using convolutional neural networks (CNNs). The research is based on electrophysiological recordings from dorsal raphe nucleus slices of transgenic mice, incorporating both original and synthetic spike samples to enhance model reliability and mitigate overfitting. This study not only challenges traditional neuron identification methods but also enhances the understanding of the serotonergic system's diversity, offering robust models for neuron classification validated across diverse data sets.

![ Deep Learning Models for Atypical Serotoninergic Cells Recognition](https://github.com/neuraldl/DLAtypicalSerotoninergicCells/blob/main/images/ArchitectureWork2.png)

## Overview
Traditional methods for identifying serotonergic neurons are based on specific electrophysiological characteristics, yet this approach often overlooks atypical neurons, thus limiting our understanding of the serotonergic system's diversity. To address this, we propose deep learning models capable of recognizing both typical and atypical serotonergic and non-serotonergic neurons with high accuracy.The research utilized electrophysiological recordings from dorsal raphe nucleus slices of transgenic mice, expressing fluorescent proteins specific to the serotonergic system. These recordings formed the basis of the training, validation, and testing data for the deep learning models. The study employed convolutional neural networks (CNNs), known for their efficiency in pattern recognition, to classify neurons based on the specific characteristics of their action potentials. The models were trained on a dataset comprising 43,327 original spike samples, alongside an extensive set of 6.7 million synthetic spike samples, designed to mitigate the risk of overfitting the background noise in the recordings, a potential source of bias. Results showed that the models achieved high accuracy and were further validated on "non-homogeneous" data, i.e., data not used for constructing the model, to confirm their robustness and reliability in real-world experimental conditions.

## Contents of the Repository
In this GitHub repository are available the following:
1. the .abf recordings of original training data and the non-homogenous data,
2. the 43,327 single spikes samples of the original training data stored in .csv files of 160 points,
3. the 24,616 single spikes samples of the non-homogenous data stored in .csv files of 160 points,
4. the 6,675,300 million single spikes samples of the synthetic data stored as numpy vector,
5. the trained models with different kernels,
6. the results of the models,
7. the Python notebooks for training of the models and for inference.

## Citation

```bibtex
@article{CorradettiBernardiCorradetti2024,
    title={Deep Learning Models for Atypical Serotoninergic Cells Recognition},
    author={Corradetti Daniele, Bernardi Alessandro, Corradetti Renato},
    journal={arXiv},
    year={2024}
}
```

## Data Requirements
Libraries: TensorFlow version 2.14

Download on your local device or cloud service below folders:

### Biological Data 

SER Cellulars  https://drive.google.com/drive/folders/1OH8HZlfHk17qekf3vjGcXjaARikYGg2E?usp=sharing

NSER Cellulars https://drive.google.com/drive/folders/1SzHVo5lmmJy1U2PvwYhHpvdnFpe9lCyP?usp=sharing

### DNN Keras Models and Results 

ModelsDNN https://drive.google.com/drive/folders/1zjwc-_P6zjsmc77BdwgBhxrEhBGw8Igz?usp=sharing

### Synthetic Data

SER Cellulars https://drive.google.com/drive/folders/1HumEKutqUtAkbassrVvXY6vZ3ALryLEm?usp=sharing

NSER Cellulars https://drive.google.com/drive/folders/1j0hwJ2H_GCJT7xXt05YjgNWIB1JRzPww?usp=sharing

### Biological Data Non Homogeneous 

SER Cellulars https://drive.google.com/drive/folders/1XyLrbP1sxxOk67H8gqVojcj1wM53QXkn?usp=sharing

NSER Cellulars https://drive.google.com/drive/folders/1-4eZgkowcaDTr8z4ylcT5YxMkn3OPStD?usp=sharing

