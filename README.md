# CNN_Melody_Classifier
A convolutional neural network for detecting and classifying melodies into 88 pitch classes.

This program takes an audio input containing a monophonic melody and performs pitch analysis. The output is a sequence of MIDI note numbers ranging from 21 to 108.


## Folder Structure

- `trainingData/` – Directories are automatically generated in the program.

- `model/` – This is the folder where the trained models are output. 

## How to Use
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yuki-sato-0402/CNN_Melody_Classifier/blob/main/88midiClassification.ipynb)  
Just open the notebook(s) in Google Colab and run all the cells from top to bottom.  
No need to install anything locally — everything runs in the cloud.  
Each step is explained in the notebook itself.

## About Training Data
In this project, The data for training is generated in the program by combining SoundFont and FluidSynth.

## About output results (Model Inference)
This is the inference result using a monophonic piano audio input. The x-axis is time and the y-axis is midi note number.
As you can see, the accuracy tends to degrade in the higher pitch range.
This issue requires further improvement in future versions.

## Limitations
This is an early prototype and the pitch classification accuracy is still limited.

- Instruments with rich overtone components may be difficult to detect.

- For instruments such as piano or guitar that have a lot of noise during the attack, only the timing will be less accurate.