# ECG Abnormal Heartbeat Detection
## Project Plan

COSC 3337 Data Science I | Data Science Showcase | December 4, 2026

## Research Question and Objective

Can a Support Vector Machine (SVM) and a Multilayer Perceptron (MLP) neural network identify 
irregular heartbeats in ECG recordings from patients never seen during model training? 
The project will classify individual heartbeats as normal or irregular. We will compare SVM and 
MLP using the same patient-separated training, validation, and test partitions. For below we will 
use the expert annotations to confirm good or bad readings.

## Dataset

We will use the MIT-BIH Arrhythmia Database from PhysioNet, which has 48 approximately 
30-minute two-channel ECG recordings from 47 individuals, sampled at 360 Hz with expert 
reviewed heartbeat annotations.

Dataset: [PhysioNet - MIT-BIH Arrhythmia Database](https://physionet.org/content/mitdb/1.0.0/)

Required file types: `.dat` (ECG samples), `.hea` (metadata), and `.atr` (beat annotations).

## Methods: SVM / MLP

### 1. Support Vector Machine (SVM) - Traditional Method

This method will learn features such as beat to beat timing and waveform shape. This will only 
have access to the training set. SVM provides a strong traditional classifier in comparison to 
logistic regression. 

### 2. Multilayer Perceptron (MLP) - Neural Network

I’m not too sure on the Neural Network side yet, but it will learn using normalized ECG beat 
segments. The MLP learns nonlinear waveform patterns then we will use the validation patients 
to check.

## Evaluation Plan

Partition recordings by patient before fitting any model. Keep both recordings from the same 
individual together. Use distinct patients for training, validation and final testing. Apply the same 
partitions to both models, and learn normalization or other preprocessing parameters from 
training data only. 
Separating them by patients rather than randomizing the heartbeats will help keep consistency, 
because every patient is different, rather than their heartbeats. This should help the accuracy.  
 
Evaluate both models with sensitivity (recall for irregular heartbeats), precision, specificity, F1 
score, confusion matrix, and overall accuracy. Report class counts and analyze false negatives 
and false positives. Because this is a historical and relatively small dataset, discuss class 
imbalance and limits on clinical generalization.

## Showcase Demonstration

Build a simple ECG viewer that allows attendees to select a held-out (not tested on) patient 
record. Display the real ECG waveform, identify annotated beats, and overlay the SVM and 
MLP predictions. Highlight disagreements and misclassifications. Every selectable 
demonstration patient must be absent from model training and validation for showcase!!

## Team Responsibilities

| Team Member | Responsibility |
| --- | --- |
| Justin |  |
| Gian |  |
| Anaya |  |

## Dates

**November 1, 2026:** Project proposal (1-2 pages, PDF) due and showcase registration deadline. \
**December 4, 2026:** Data Science Showcase presentation. \
**December 6, 2026:** Final project report due.

## References

[1] [PhysioNet - MIT-BIH Arrhythmia Database](https://physionet.org/content/mitdb/1.0.0/)

[2] [WFDB Python package](https://wfdb.readthedocs.io/)

