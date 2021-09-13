---
layout: project
type: project
image: ![emotion-spectrogram](https://user-images.githubusercontent.com/60335981/133031304-923b20b5-c0b3-4976-b10c-80b76564b9b5.png)
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
<br><br>Part of the objective of the present study is also to demonstrate how eliminating any sort of manual effort required on extracting features (using deep learning with image data approach) compares with the approach that constitute manual effort to a certain extent in designing the time or frequency time-series features.
<br>Overall the main objective of this study is to explore new avenues with potential performance improvements in Neural network-based emotion classification models with time-frequency features such as spectrograms, chromagrams etc., time series features extracted from the waveforms as inputs, experimented on different neural network architectures.

<br><br>
### Data Distribution:

<br>
<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="![data-distribution](https://user-images.githubusercontent.com/60335981/133029494-64f099db-40f6-4ff2-97e5-8fe7933848d5.png)"><br>
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
  <img class="ui image" src="![image](https://user-images.githubusercontent.com/60335981/133028336-02ce5114-53bd-42d7-b0cb-573694e62d0d.png)"><br>
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
  <img class="ui image" src="![time-freq-feature-spectrograms](https://user-images.githubusercontent.com/60335981/133028580-dd51894a-0b43-4b22-bfa3-d50307c23d3e.png)"><br>
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
  <img class="ui image" src="![time-domain-model-impl](https://user-images.githubusercontent.com/60335981/133029814-9e0bea89-fcf9-48fb-a863-bc744166ae7b.png)"><br>
</div>
<br><br>

<div style="text-align:center" class="ui large rounded images">
  <img class="ui image" src="![vgg19net](https://user-images.githubusercontent.com/60335981/133030884-b1a38fa1-1379-478c-a5d7-c31b3bd0cd18.png)"><br>
</div>
<br><br>

### Results:
1. Amplitude Envelope (approach1)
<br>
<div class="ui medium rounded images">
  <img class="ui image" src="![mse-AE](https://user-images.githubusercontent.com/60335981/133033981-e75e1bfe-ff04-4d47-ab95-854565ef2f68.png)">
  <img class="ui image" src="![accuracy-AE](https://user-images.githubusercontent.com/60335981/133034014-6c27bb22-522d-4be5-b9e3-1ba2488cfc95.png)">
</div>
<br>
2. Combined Time and Frequency approach
<br>
<div class="ui medium rounded images">
  <img class="ui image" src="![accuracy-app2](https://user-images.githubusercontent.com/60335981/133033700-43662711-6734-4b51-8d76-b4b234d23e8a.png)">
</div>
<br>
3. Time-Frequency approach
  1. Linear Spectrogram
<br>
<div class="ui medium rounded images">
  <img class="ui image" src="![linear-spectrogram](https://user-images.githubusercontent.com/60335981/133032769-4a8c23fe-e7f7-4df8-a067-cf094403f8d2.png)">
  <img class="ui image" src="![linear-spectrogram-Acc-mse](https://user-images.githubusercontent.com/60335981/133032824-f043b6d8-0292-441a-8d51-b95fce6de981.png)">
  <img class="ui image" src="![linear-spectrogram-auc-mse](https://user-images.githubusercontent.com/60335981/133032845-3a282434-2ef5-4cc4-8637-c5ba612681f7.png)">
</div>
<br>
  2. CQT
<br>
<div class="ui medium rounded images">
  <img class="ui image" src="![cqt](https://user-images.githubusercontent.com/60335981/133033227-5157a32f-2cf7-4f9f-aaf0-e163c4b5cbc0.png)">
  <img class="ui image" src="![cqt-acc-loss](https://user-images.githubusercontent.com/60335981/133033251-98c698b7-445a-4c49-a29e-1c4da563fc24.png)">
  <img class="ui image" src="![cqt-mse-auc](https://user-images.githubusercontent.com/60335981/133033281-6ce43da5-ef14-4841-93b2-baf2d661a2ab.png)">
</div>
<br>
  3. Log-CQT
<br>
<div class="ui medium rounded images">
  <img class="ui image" src="![log-cqt](https://user-images.githubusercontent.com/60335981/133033341-cf9f4ff5-8a31-4d34-b1c9-87e72787d878.png)">
  <img class="ui image" src="![log-cqt-acc-loss](https://user-images.githubusercontent.com/60335981/133033365-75bca5e6-3e1e-4d46-91eb-e0ad30aca46c.png)">
  <img class="ui image" src="![log-cqt-acc-mse](https://user-images.githubusercontent.com/60335981/133033390-bf9d9561-6ee0-4c23-89df-12417e5adb88.png)">
</div>
<br>
  4. Chroma
<br>
<div class="ui medium rounded images">
  <img class="ui image" src="![chroma-cqt](https://user-images.githubusercontent.com/60335981/133033442-0151cb22-031f-48d0-8b60-a446c0b0d39e.png)">
  <img class="ui image" src="![chroma-cqt-acc-loss](https://user-images.githubusercontent.com/60335981/133033458-81ab19ac-75bf-47be-9515-89798c6c500c.png)">
  <img class="ui image" src="![chroma-cqt-auc-mse](https://user-images.githubusercontent.com/60335981/133033477-784e3a1e-4bc1-4637-97e3-9e9bd192487b.png)">
</div>
<br>
  5. MFCCs 
<br>
<div class="ui medium rounded images">
  <img class="ui image" src="![mfcc](https://user-images.githubusercontent.com/60335981/133033496-4bcbc4aa-8bf6-416e-a91a-bb8ec5215b8b.png)">
  <img class="ui image" src="![mfcc-acc-loss](https://user-images.githubusercontent.com/60335981/133033513-64a4898f-37c4-46ea-ae27-15b7a0d4c02d.png)">
  <img class="ui image" src="![mfcc-auc-mse](https://user-images.githubusercontent.com/60335981/133033598-d1d38106-a65b-4b7f-92ba-8584a0d030df.png)">
</div>
<br>
