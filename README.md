ATD-Federated ViT Project
Overview
The ATD Federated Vision Transformer Project (ATD-Federated ViT) is a decentralized, privacy-preserving framework for training multi-modal medical imaging datasets (e.g., CT, PET, X-ray). It leverages AI-to-Data (ATD), a federated learning paradigm, where models are trained locally on data at individual nodes and collaboratively exchange learned parameters to improve global performance. This approach ensures data privacy, scalability, and robustness across distributed datasets.

The framework integrates:

A Multi-Head Vision Transformer (ViT) architecture.
Support for CT (DICOM), PET (DICOM), and X-ray (JPG) modalities.
Decentralized ensemble learning for improved classification accuracy.
Advanced visualization techniques using Grad-CAM and t-SNE.
Key Features
Decentralized Federated Learning:

Models are trained locally at each node using a modality-specific ViT head.
Nodes exchange only the learned weights, ensuring data privacy.
Multi-Head Vision Transformer (ViT):

Each head specializes in a specific modality (e.g., CT, PET, or X-ray).
Supports scalable learning by adding new modalities without retraining the entire model.
AI-to-Data Paradigm:

Training happens where the data resides, avoiding raw data transfer between nodes.
Ensures compliance with strict data protection regulations (e.g., HIPAA).
Visualization for Interpretability:

Grad-CAM: Highlights regions of interest contributing to predictions.
t-SNE: Visualizes feature space separability for different classes.
Robust Preprocessing Pipelines:

Prepares and standardizes CT (DICOM), PET (DICOM), and X-ray (JPG) images.
Applies modality-specific preprocessing for enhanced model performance.
Fairness and Scalability:

Weighted aggregation ensures equitable learning across nodes with varying dataset sizes.
Dynamic node addition allows seamless integration of new datasets or modalities.
System Architecture
The project includes the following components:

Local Training:

Each node trains one modality-specific ViT head on its local dataset.
Training minimizes a cross-entropy loss function, retaining modality-specific features.
Weight Exchange:

Trained weights from all nodes are exchanged securely in a decentralized manner.
Updates are integrated using weighted averaging, reducing bias and improving generalization.
Ensemble Learning:

Predictions from all heads are combined through ensemble learning for final classification.
Enhances robustness by leveraging diverse features learned across modalities.
Visualization:

Grad-CAM heatmaps for model interpretability.
t-SNE plots to analyze class separability in feature space.
Supported Modalities
The framework supports the following medical imaging modalities:

CT (DICOM): Processed for structural abnormalities.
PET (DICOM): Focused on metabolic activity.
X-ray (JPG): Evaluates chest and skeletal features.
