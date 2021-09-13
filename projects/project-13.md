---
layout: project
type: project
image: images/emotion-spectrogram.png
title: Music Emotion Recognition using Time, Frequency and Time-Frequency audio feature based inputs with Neural Networks
permalink: projects/mer
# All dates must be YYYY-MM-DD format!
date: 2021-01-16
labels:
  - Digital Audio Processing
  - Music Information Retrieval
  - Spectrograms
  - BiLSTM
  - VGG19Net
  
summary: Three approaches differentiated by time and frequency domain are undertaken to determine the emotions in a given musical clip with Convolutional Neural Networks, deep recurrent neural networks such as Long Short-Term Memory (LSTMs), Bidirectional LSTMs (BiLSTMs) and pre-trained model such as VGG19 Net.
---

### Problem Statement:
To classify emotions out of musical pieces with the help of deep neural network models using time, frequency and time-frequency based audio inputs.

### Approach:
In this project the MER problem has been looked at in the context of time and frequency acoustic features. A number of features are implemented across <br><br>
(i) time domain, <br>
(ii) frequency domain and <br>
(iii) time-frequency domain,
<br><br>rather than limiting to just waveform or a spectrogram visual feature, as has been the study in the past.
<br>
This means that features from time domain that are characterized by loudness, pitch etc. such as Amplitude Envelope, zero crossing rate, root-mean square energy are studied as time series. Features from frequency domain such as spectral features or temporal features are studied as numerical or time series format again. The time-frequency domain features in visual representation such as Spectrogram, chromagrams, CQT transform, MFCCs are taken as image inputs to pre-trained models.
  - Multiple model experiments are demonstrated along with relevant reasoning.
  - The performance for all the three approaches is demonstrated and compared.
<br>
Part of the objective of the present study is also to demonstrate how eliminating any sort of manual effort required on extracting features (using deep learning with image data approach) compares with the approach that constitute manual effort to a certain extent in designing the time or frequency time-series features.
<br>
Overall the main objective of this study is to explore new avenues with potential performance improvements in Neural network-based emotion classification models with time-frequency features such as spectrograms, chromagrams etc., time series features extracted from the waveforms as inputs, experimented on different neural network architectures.

<br><br>
### Data Distribution:

<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/data-distribution.png"><br>
</div>
<br>

- Time-domain Feature Extraction Pipeline
  - Below are some of the common time domain features:
    1.	Amplitude Envelope (AE)
    2.	Root-Mean-Square Energy (RMSE)
    3.	Zero-Crossing Rate (ZCR)

- Combined Time and Frequency Domain Feature Extraction Pipeline
  - Below are some of the frequency domain features:
    1. Time domain features (e.g., Amplitude Envelope, RMSE, Zero-Crossing Rate)
    2. Spectral Features (e.g., Spectral Flux, Spectral roll-off etc.)
    3. Temporal Features (e.g., MFCCs)

<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/audio-signal-with-frames-AE.png"><br>
</div>
<br>

- Time-Frequency Feature Extraction Pipeline
  - Below are the some of the time-frequency domain features:
    1. Spectrograms/ Mel-Spectrograms
    2. Chromagrams
    3. CQT Transforms
    4. Tempograms

<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/time-freq-feature-spectrograms.png"><br>
</div>
<br><br>

### Model Implementation:
1. Time Domain Feature Model Implementation: 
  - the model combination of 1D CNN and BiLSTM has the best performance, with a moderately good accuracy of 70% and low MSE on test data.
2. Combined Time and Frequency Domain Feature Model Implementation: 
  - a densely deep ANN has the best performance with high accuracy of 84% an low MSE on test data.
3. Time-Frequency Feature Model Implementation: 
  - the transfer learning based model (VGG19Net) with 7 fully connected layers on top has the best performance with high accuracy of 80% and an AUC of 97% on test data.

<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/time-domain-model-impl.png"><br>
</div>
<br><br>

<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/vggnet19.png"><br>
</div>
<br><br>

### Results:
#### Amplitude Envelope (approach1)
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/mse-AE.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/accuracy-AE.png">
</div>
<br>

#### Combined Time and Frequency approach
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/accuracy-app2.png">
</div>
<br>

#### Time-Frequency approach
- Linear Spectrogram
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/linear-spectrogram.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/linear-spectrogram-Acc-mse.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/linear-spectrogram-auc-mse.png">
</div>
<br>
- CQT
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/cqt.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/cqt-acc-loss.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/cqt-mse-auc.png">
</div>
<br>
- Log-CQT
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/log-cqt.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/log-cqt-acc-loss.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/log-cqt-acc-mse.png">
</div>
<br>
- Chroma
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/chroma-cqt.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/chroma-cqt-acc-loss.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/chroma-cqt-auc-mse.png">
</div>
<br>
- MFCCs
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/mfcc.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/mfcc-acc-loss.png">
</div>
<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="../images/mfcc-auc-mse.png">
</div>
<br>
