# **ATD-Federated ViT Project**

## **Overview**
The **ATD-Federated Vision Transformer (ViT)** project is a decentralized, privacy-preserving machine learning framework designed for medical imaging. It leverages **multi-head Vision Transformers** and **federated learning principles** to collaboratively train models across distributed datasets, ensuring privacy and scalability. This project supports **CT (DICOM)**, **PET (DICOM)**, and **X-ray (JPG)** modalities, with robust visualization tools like **Grad-CAM** and **t-SNE** for interpretability.

---

## **Key Features**
1. **Decentralized Federated Learning**:
   - Train models locally while ensuring data privacy.
   - Share only model weights instead of raw data.

2. **Multi-Head Vision Transformer**:
   - Separate heads for each modality (CT, PET, X-ray).
   - Ensemble learning for robust classification.

3. **Privacy-Preserving**:
   - Data never leaves the local node.
   - Complies with strict data protection standards like HIPAA.

4. **Visualization Tools**:
   - **Grad-CAM** for heatmap-based interpretability.
   - **t-SNE** for feature space analysis.

5. **Scalability and Fairness**:
   - Dynamic addition of new nodes or modalities without retraining the entire model.
   - Weighted aggregation ensures fairness across nodes.

---

## **Supported Modalities**
- **CT (DICOM)**: Preprocessed for structural abnormalities.
- **PET (DICOM)**: Focused on metabolic activity.
- **X-ray (JPG)**: Evaluates structural and radiological patterns.

---

## **System Architecture**
1. **Local Training**:
   - Each node trains one modality-specific ViT head using local data.
   - Minimized cross-entropy loss retains modality-specific features.

2. **Decentralized Weight Exchange**:
   - Nodes exchange trained weights securely without requiring a central server.
   - Weighted averaging improves global generalization.

3. **Ensemble Learning**:
   - Predictions from all heads are combined for final classification.
   - Enhances robustness and reduces bias.

4. **Visualization**:
   - **Grad-CAM** heatmaps highlight regions contributing to predictions.
   - **t-SNE** visualizes class separability in feature space.

---

## **Installation**

### **1. Clone the Repository**
```bash
git clone https://github.com/ahmedalisiehood/ATD-Federated-ViT-project.git
cd ATD-Federated-ViT-project
