### MSAI-VetDisease-CRNN-2026
Veterinary Disease Detection using CRNN (Convolutional Recurrent Neural Network) An AI project focused on identifying pet skin diseases (Healthy, Fungal, Bacterial, and Allergic) using a custom-built CRNN architecture. Developed for the MSAI program (Fall 2025) and aligned with SDG 3 to improve animal healthcare through automated diagnostics.
### 🐾 Veterinary Disease Detection via Custom CRNN
Domain: Veterinary | Algorithm: CRNN | Goal: >75% Accuracy | Status: Completed

###3📌 Project Overview
This repository hosts a from-scratch implementation of a Convolutional Recurrent Neural Network (CRNN) designed for automated veterinary diagnostics. By combining the spatial feature extraction of CNNs with the sequential pattern recognition of GRUs, this model provides a robust solution for classifying common animal skin conditions, contributing directly to UN SDG 3: Good Health and Well-being.

### 🎯 Key Objectives

### Multi-Class Classification
Accurately categorize 4 distinct skin conditions: Healthy, Fungal, Bacterial, and Allergic.
### From-Scratch Development
Zero reliance on pre-trained weights or Transfer Learning.
### Performance Benchmark
Achieve and maintain a validation accuracy of ≥75%.
### Reproducibility
Utilize fixed seeding (torch.manual_seed(42)) to ensure consistent results across environments.

### 🚀 Development & Methodology
### 🧠 Model Architecture
The "brain" of this project is a hybrid CRNN architecture built using PyTorch 2.0:
### CNN Component
Two stages of Conv2d layers with BatchNorm2d for mathematical stability and ReLU activation for non-linearity.
### RNN Component
A 2-layer Gated Recurrent Unit (GRU) with a hidden size of 256 and dropout (0.2) to process temporal/sequential dependencies within image features.
### Final Layer
A Fully Connected (FC) layer that maps the 256 GRU features to the 4 target disease classes.

📥 Data Pipeline & Preprocessing
I established a working data pipeline that handles the following
### Resizing: 
All images standardized to $128 \times 128$ pixels.
### Augmentation: 
Applied RandomHorizontalFlip and normalization to improve model generalization.
### Splitting: 
Utilized an 80/20 split for training and validation to ensure rigorous testing.

### 📉 Training & Optimization Strategy
The model was trained over 30+ epochs using the following experimental setup:
### Optimizer:
Adam Optimizer (Initial LR: 0.001).
### Loss Function: 
Cross-Entropy Loss.
### Learning Rate Scheduler: 
Implemented StepLR to refine weights in later epochs, which was critical for jumping from 50% to >75% accuracy.

### Model Checkpointing: 
Automatically saved the "Best Brain" whenever validation accuracy improved.

### 📈 Experimental Results
### Final Accuracy: 
Achieved a peak validation accuracy of 75.11%, surpassing the project requirement.
### Evaluation Metrics:
Generated a full Classification Report including Precision, Recall, and F1-Scores for each disease class.
### Visualizations:
Learning Curves: Plotted Accuracy vs. Loss to document the training journey.
### Confusion Matrix: 
Implemented to visualize class-specific performance and identify common misclassifications.
### Live Inference:
Created a visualization script to show the model's "sight" and confidence percentage on new images.

