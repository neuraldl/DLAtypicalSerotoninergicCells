# Deep Learning Models for Atypical Serotoninergic Cells Recognition
[![Paper](https://img.shields.io/badge/version-1.0.1-blue)]() [![Paper](https://img.shields.io/badge/q--bio.NC-Paper-b31b1b?logo=arxiv&logoColor=red)](https://arxiv.org/) [![Paper](https://img.shields.io/badge/release-open_access-green)]()

> **Deep Learning Models for Atypical Serotoninergic Cells Recognition**<br>
>**Date**: February 28, 2024<br>
> [Corradetti Daniele](https://ualg.academia.edu/DanieleCorradetti), [Bernardi Alessandro](https://www.linkedin.com/in/alessandro-bernardi/), [Corradetti Renato](https://unifi.academia.edu/RenatoCorradetti)<br>
> *Grupo de Fisica Matematica, Instituto Superior Tecnico, Av. Rovisco Pais, Lisboa, 1049-001, Portugal*<br>
> *Departamento de Matematica, Universidade do Algarve, Campus de Gambelas, Faro, 8005-139, Faro, Portugal*<br>
> *Department of Neuroscience, Psychology, Drug Research and Child Health (NEUROFARBA), University of Florence, Viale G. Pieraccini 6, Firenze, 50139, Toscana, Italy*<br>

This repository is aimed to collect the data and models used for *Deep Learning Models for Atypical Serotoninergic Cells Recognition* by Corradetti Daniele, Bernardi Alessandro, Corradetti Renato. The work proposes an innovative deep learning approach to accurately identify both typical and atypical serotonergic neurons using convolutional neural networks (CNNs). The research is based on electrophysiological recordings from dorsal raphe nucleus slices of transgenic mice, incorporating both original and synthetic spike samples to enhance model reliability and mitigate overfitting. This study not only challenges traditional neuron identification methods but also enhances the understanding of the serotonergic system's diversity, offering robust models for neuron classification validated across diverse data sets.

## Overview
Traditional methods for identifying serotonergic neurons are based on specific electrophysiological characteristics, yet this approach often overlooks atypical neurons, thus limiting our understanding of the serotonergic system's diversity. To address this, we propose deep learning models capable of recognizing both typical and atypical serotonergic and non-serotonergic neurons with high accuracy.The research utilized electrophysiological recordings from dorsal raphe nucleus slices of transgenic mice, expressing fluorescent proteins specific to the serotonergic system. These recordings formed the basis of the training, validation, and testing data for the deep learning models. The study employed convolutional neural networks (CNNs), known for their efficiency in pattern recognition, to classify neurons based on the specific characteristics of their action potentials. The models were trained on a dataset comprising 43,327 original spike samples, alongside an extensive set of 6.7 million synthetic spike samples, designed to mitigate the risk of overfitting the background noise in the recordings, a potential source of bias. Results showed that the models achieved high accuracy and were further validated on "non-homogeneous" data, i.e., data not used for constructing the model, to confirm their robustness and reliability in real-world experimental conditions.
<div>
  <img src="https://github.com/neuraldl/DLAtypicalSerotoninergicCells/blob/main/images/Figure2.png" alt="Figure 2" width="368" style="display:inline-block;" />
  <img src="https://github.com/neuraldl/DLAtypicalSerotoninergicCells/blob/main/images/Figure3.png" alt="Figure 3" width="400" style="display:inline-block;" />
</div>
Distribution of spike duration of serotonergic and non-serotonergic neurons. Histograms report the distribution of spike width measured by the interval between spike upstroke and downstroke (UDI) in serotonergic (blue) and non-serotonergic neurons (red) recorded in slices of dorsal raphe nucleus. Note the overlap in spike duration between serotonergic and non-serotonergic neurons which indicates atypical cells.

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

## Data Requirements and Instructions
[![Data](https://img.shields.io/badge/TensorFlow-2.14-orange)]()<br>
Libraries: TensorFlow version 2.14 <br>
Download on your local device or cloud service the data folders. <br>
Notebooks are all available on Google Colab. <br>

## Original Data
[![Data](https://img.shields.io/badge/SER-Original-blue)]() SER Cellulars [ [Data](https://drive.google.com/drive/folders/1OH8HZlfHk17qekf3vjGcXjaARikYGg2E?usp=sharing) ]<br>
[![Data](https://img.shields.io/badge/NSER-Original-blue)]() NSER Cellulars [ [Data](https://drive.google.com/drive/folders/1SzHVo5lmmJy1U2PvwYhHpvdnFpe9lCyP?usp=sharing) ] <br>

The original data for the training, validation and testing of the models consisted in 43,327 spike samples extracted from 108 serotonergic cells and 45 non-serotonergic cells. More specifically, we extracted
29,773 spikes from serotonergic cells, and 13,554 spikes from non-serotonergic cells. In all cases, the triggering threshold of the event was -50 pA and the spike was then sampled 1 ms before the triggering threshold until 3 ms after (see Fig. 1). Since the sampling rate of the original recordings was 40 kHz, every spike sample consists of 160 values.
All the samples were then randomly subdivided into 30,328 for training, 6,500 for validation and 6,499 for testing. 
<figure style="text-align: center;">
  <img style="text-align: center;" src="https://github.com/neuraldl/DLAtypicalSerotoninergicCells/blob/main/images/OriginalData140313.png" alt="Original Data" width="500" />
  <figcaption>Example on how single events were isolated and selected. The image depicts the recording of the serotonergic cell A140313\#073 and the 4 ms event of triggered at point 1007585, i.e. at 25.189 sec.</figcaption>
</figure>


## Synthetic Data
[![Data](https://img.shields.io/badge/SER-Synthetic-red)]() SER Cellulars [ [Data](https://drive.google.com/drive/folders/1HumEKutqUtAkbassrVvXY6vZ3ALryLEm?usp=sharing) ] <br>
[![Data](https://img.shields.io/badge/NSER-Synthetic-red)]() [NSER Cellulars [ [Data](https://drive.google.com/drive/folders/1j0hwJ2H_GCJT7xXt05YjgNWIB1JRzPww?usp=sharing) ] <br>

The synthetic data consisted in 6,675,300 spike samples of 160 points (simulating 4 ms at 40 kHz of sampling) arising from the 43327 original training data samples. From the original training data recordings we extracted 600 noise masks.
<figure style="text-align: center;">
  <img src="https://github.com/neuraldl/DLAtypicalSerotoninergicCells/blob/main/images/SyntheticData.png" alt="Data Pipeline" width="400" />
  <figcaption>Example of 4 synthetic spikes generated by the event triggered at 1007585, i.e. 25.189 sec, of the serotonergic cell A140313#073. Top trace: the original recording of the event. The panels report four spike obtained by processing the original trace with different noise masks.</figcaption>
</figure>

## Non-Homogeonous Data
[![Data](https://img.shields.io/badge/SER-Non--Hom-green)]() SER Cellulars [ [Data](https://drive.google.com/drive/folders/1XyLrbP1sxxOk67H8gqVojcj1wM53QXkn?usp=sharing) ] <br>
[![Data](https://img.shields.io/badge/NSER-Non--Hom-green)]() NSER Cellulars [ [Data](https://drive.google.com/drive/folders/1-4eZgkowcaDTr8z4ylcT5YxMkn3OPStD?usp=sharing) ] <br>

The non-homogenous data consisted in 24,616 samples extracted from 55 serotonergic cells (18,595 spikes) and 26 non-serotonergic cells (6,021 spikes) collected in experimental days not used to obtain the training data, thus with different signal noise. These data were never part of the training set, nor validation, nor testing set during the training, and constituted just an additional independent test for
the already trained model.

## Models and Results

### Architecture
The architecture of the models is a sequence of layers commonly used in deep learning, specifically in the context of convolutional neural networks (CNNs) for image or signal processing.
We implemented the architecture using the Keras libraries in TensorFlow 2. The model of the neural network consists of a normalization layer for stabilizing the learning process and reducing training time; two repetitions of a 2D convolutional layer with 32 filters and a max pooling layer with a pool size of (2x1); a flatten layer to connect to a dropout layer and dense layers with 2 output units used for binary classification. Activation functions of the convolutional layers are the ReLU, while for the dense layer we used the classic sigmoid. For training we chose the "binary crossentropy" loss function, which is standard for binary classification problems, while the optimizer was "Adam" (Adaptive Moment Estimation) as these are common choices. A special treatment was devoted to the kernel of the 2D convolutional layers. Indeed, since the kernel of these layers express the ability of the convolutional process in enlarging a specific portion of the pattern, we explored a range of possible kernels between 1 to 32.   

**Table 1: Summary of the Model**

| *Layer (type)*        | *Output Shape*      | *Param #* |
|-----------------------|---------------------|-----------|
| Layer Normalization   | (None, 160, 2, 1)   | 320       |
| Conv2D                | (None, 141, 2, 32)  | 672       |
| MaxPooling2D          | (None, 70, 2, 32)   | 0         |
| Conv2D                | (None, 51, 2, 64)   | 41024     |
| MaxPooling2D          | (None, 25, 1, 64)   | 0         |
| Flatten               | (None, 1600)        | 0         |
| Dropout               | (None, 1600)        | 0         |
| Dense                 | (None, 2)           | 3202      |
| **Total Params**      | **45218**           |           |

Summary of the CNN architectural model with kernel 20 used for the neural network. Other models follow the same architectural structure and change only for the dimension of the kernel. 

<figure style="text-align: center;">
  <img style="text-align: center;" src="https://github.com/neuraldl/DLAtypicalSerotoninergicCells/blob/main/images/ArchitectureWork2.png" alt="Data Pipeline" width="500" />
  <figcaption>Summary of the various steps used to implement the model from recorded signals: from neuronal cell the signal is sampled at 40 kHz and recorded as .abf file, then the all events are selected and sent to 10 neural networks with the above architecture for classification (only difference between the architectures is the value of the 2D convolutional kernel with ranges between 20 to 30).</figcaption>
</figure>

### DNN Keras Models and Results 
[![Data](https://img.shields.io/badge/Models_DNN-Keras-orange)]() ModelsDNN [ [Data](https://drive.google.com/drive/folders/1zjwc-_P6zjsmc77BdwgBhxrEhBGw8Igz?usp=sharing) ] <br>
For training we chose the "binary crossentropy"
loss function, which is standard for binary classification problems,
while the optimizer was "Adam" (Adaptive Moment Estimation) as
these are common choices. A special treatment was devoted to the kernel
of the 2D convolutional layers. Indeed, since the kernel of these
layers express the ability of the convolutional process in enlarging
a specific portion of the pattern, we explored a range of possible
kernels between 1 to 32. Apart from the models with kernel $<$5, the
results were homogenous and summarized in Fig.  
<figure style="text-align: center;">
  <img style="text-align: center;" src="https://github.com/neuraldl/DLAtypicalSerotoninergicCells/blob/main/images/AccuracyLossEpoch.png" alt="Data Pipeline" width="400" />
  <figcaption>On top: in the graphic is depicted the accuracy for every epoch of the training (0-24) for all models with kernel ranging from 20 to 30.  On the bottom : the image depicts the loss function for every epoch of the training (0-24) for all models with kernel ranging from 20 to 30.</figcaption>
</figure>
All models were trained on 25 epochs with a batch size of 64 and
their test accuracy ranged from 90.6\% (model with kernel 1) to 98.7\%
(model with kernel 23, 24 and 27) with a test loss of 0.2221 and 0.037106.
To enhance the robustness of the model, instead of selecting a single
kernel and using one model for inference, we selected all models with
kernels ranging between 20 and 30 and took the consensus between the
models. This technique ensures more stability in the overall architecture
and is often considered best practice.
<figure style="text-align: center;">
  <img style="text-align: center;" src="https://github.com/neuraldl/DLAtypicalSerotoninergicCells/blob/main/images/Accuracy-Loss-Sensitivity.png" alt="Data Pipeline" width="400" />
  <figcaption>Each of the 32 models, with kernel
sizes varying from 1 to 31, was evaluated for test loss, sensitivity
at a specificity of 0.5, and accuracy. The resulting graphs depict
a monotonic trend correlating with the increasing kernel sizes, which
eventually stabilizes in the range from kernel size 20 to 31.</figcaption>
</figure>
<figure style="text-align: center;">
  <img style="text-align: center;" src="https://github.com/neuraldl/DLAtypicalSerotoninergicCells/blob/main/images/ConfusionMatrixBiologicalModelNHData.png" alt="Data Pipeline" width="400" />
  <figcaption>The confusion matrix for the biological
model over the non-homogeneous data labels serotonergic cells as 0
and non-serotonergic cells as 1. The matrix shows the True Positive
Rate 94.4\% at the Top-Left; the False Negative Rate 5.6\% at the
Bottom-Left; the False Positive Rate 11\% at the Top-Right; and the
True Negative Rate 88.4\% at the Bottom-Right.</figcaption>
</figure>
Regarding the synthetic data, the confusion matrix values vary with
each training session. The highest values attained by the synthetic
data match those of the original data, specifically a 94.4\% True
Positive Rate, 5.6\% False Negative Rate; 88.4\% True Negative Rate
and 11\% False Positive Rate. The average values for the synthetic
data across training sessions are 91.2\% for True Positive Rate, 0.8\%
for False Negative Rate; 87.6\% for True Negative Rate and 12.3\%
for False Positive Rate. These Fig.s for the synthetic data closely
align with those of the original data, indicating no overfitting specifically
due to the noise in the recorded signal.

## Acknowledgments
The original recordings and measurements of the spikes recorded in .abf files were performed
by [Dr. Boris Mlinar](https://loop.frontiersin.org/people/98296/overview) and [Dr. Alberto Montalbano](https://loop.frontiersin.org/people/110587/overview). 
