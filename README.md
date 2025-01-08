# Enhanced-Epilepsy-Diagnosis-through-EEG-Pattern-Recognition

# Introduction
This project explores the intersection of deep learning and neuroscience, focusing on developing a classification model for EEG data analysis to diagnose epilepsy. The model aims to identify unique patterns in EEG recordings, particularly epileptiform discharges, which are crucial for epilepsy diagnosis.
# Background
Electroencephalogram (EEG) is a vital diagnostic tool for epilepsy and other brain disorders. It captures brain waves reflecting various states of consciousness and cognitive functions:
Delta waves (0.5-4 Hz): Deep sleep

Theta waves (4-8 Hz): Light sleep, drowsiness, meditation
Alpha waves (8-13 Hz): Relaxation
Beta waves (13-30 Hz): Wakefulness, cognitive tasks
Gamma waves (30-100 Hz and beyond): Advanced cognitive functions
The project utilizes the Bonn dataset, consisting of 100 single-channel EEG recordings with a spectral bandwidth of 0.5 Hz to 85 Hz, sampled at 173.61 Hz.
# Data Preprocessing
Applied a Butterworth bandpass filter (0.5-45 Hz)
Normalized data using StandardScaler
# Feature Extraction
Extracted both frequency-domain and time-domain features:
Frequency-domain: Peak frequency, average power
Time-domain: Mean, standard deviation, skewness, kurtosis
# Model Architecture
Convolutional layer (125 filters, kernel size 3)
MaxPooling layer (pool size 3)
LSTM layers (198 units)
# Model Training
The model was trained using a dataset split into:
Training set: 300 samples
Validation set: 75 samples
Testing set: 125 samples
Hyperparameters were optimized using Optuna framework.
# Evaluation Results
Overall accuracy: 71%
Class 1: Precision 71%, Recall 100%, F1-score 83%
Class 0: Precision 0%, Recall 0%, F1-score 0%
Conclusion
The model shows promising results for Class 1 but struggles with Class 0 predictions. Further improvements are needed to address class imbalance and enhance overall performance.
# Future Work
Explore additional deep learning techniques
Enhance feature engineering
Implement data augmentation strategies
Investigate ensemble learning methods
Evaluate transfer learning approaches
Incorporate interpretable models for better explainability
