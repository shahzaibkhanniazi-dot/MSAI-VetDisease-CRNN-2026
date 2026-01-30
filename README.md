MSAI-VetDisease-CRNN-2026
Veterinary Disease Detection using CRNN (Convolutional Recurrent Neural Network) An AI project focused on identifying pet skin diseases (Healthy, Fungal, Bacterial, and Allergic) using a custom-built CRNN architecture. Developed for the MSAI program (Fall 2025) and aligned with SDG 3 to improve animal healthcare through automated diagnostics.

🐾 Veterinary Disease Detection via Custom CRNN
Domain: Veterinary | Algorithm: CRNN | Goal: >75% Accuracy 

📌 Phase 1: Planning & Documentation (Completed)
This repository contains a from-scratch implementation of a CRNN for veterinary diagnostics.

🎯 Key Objectives
Classify 4 skin disease categories.

Zero use of pre-trained models.

Achieve 75%+ accuracy with reproducible seeding.

Address UN SDG 3: Good Health and Well-being.

📁 Initial Structure

Documentation/: Project Initial Doc & Timeline.


Data/: Placeholder for Drive-mounted dataset.


Scripts/: Training and Model architecture.

📥 Data Acquisition
Downloaded and organized Veterinary skin disease dataset into 4 classes: Healthy, Fungal, Bacterial, and Allergic.

💻 Environment Setup
Successfully uploaded the dataset to Google Drive and synced the directory structure for Colab integration.

🚀 Phase 2: Development & Training (Completed)
In this phase, the core AI "brain" was developed and trained from scratch to meet the performance benchmarks.

🧠 Model Architecture (CRNN)

CNN Layers: Custom convolutional layers designed to extract spatial features from animal skin images.


RNN Layers: Integrated GRU (Gated Recurrent Units) to process sequence patterns in the image data.

Seeding: Applied torch.manual_seed(42) to ensure the 75%+ accuracy is reproducible every time the code runs.

📈 Experimental Results

Training Strategy: Optimized using the Adam optimizer with Cross-Entropy Loss.


Final Accuracy: Achieved a validation accuracy of >75%, meeting the project's passing criteria.


Visualizations: Generated learning curves for Loss and Accuracy to track model convergence.

💾 Model Export
The final trained model weights have been saved as vet_model_brain.pth for future inference and testing.
