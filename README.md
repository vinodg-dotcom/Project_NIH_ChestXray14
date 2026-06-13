AI-Powered Chest Disease Detection using Deep Learning and Explainable AI
Project Overview
This project develops an AI-assisted radiology system capable of detecting multiple thoracic diseases from chest X-ray images using deep learning. The system is trained on the NIH ChestXray14 dataset and supports multi-label classification across 14 disease categories.
The project compares three deep learning architectures:
•	Custom Convolutional Neural Network (CustomCNN)
•	ResNet18 (Transfer Learning)
•	VGG19 (Transfer Learning)
To improve transparency and clinical trust, Grad-CAM visualizations are generated to highlight image regions influencing model predictions. A Retrieval-Augmented Generation (RAG) module further provides clinical explanations and AI-generated summaries.
________________________________________
Dataset
Dataset: NIH ChestXray14
Total Images: 112,120+
Diseases:
•	Atelectasis
•	Cardiomegaly
•	Effusion
•	Infiltration
•	Mass
•	Nodule
•	Pneumonia
•	Pneumothorax
•	Consolidation
•	Edema
•	Emphysema
•	Fibrosis
•	Pleural Thickening
•	Hernia
________________________________________
Key Features
Multi-Label Disease Classification
Predicts multiple diseases simultaneously from a single chest X-ray.
Patient-Wise Data Split
Patient-level separation prevents data leakage between training and testing datasets.
Class Imbalance Handling
Weighted Binary Cross Entropy Loss is used to address severe label imbalance.
Explainable AI
Grad-CAM visualizations identify image regions responsible for model predictions.
Retrieval-Augmented Generation (RAG)
Clinical knowledge base provides disease definitions and generates physician-oriented summaries.
________________________________________
Models Evaluated
CustomCNN
A lightweight CNN built specifically for chest X-ray classification.
ResNet18
Transfer learning architecture utilizing residual connections.
VGG19
Deep transfer learning architecture with strong feature extraction capability.
________________________________________
Evaluation Metrics
The following metrics are reported:
•	Mean AUROC
•	Mean PR-AUC
•	Macro F1 Score
•	Micro F1 Score
•	Precision
•	Recall
•	Per-label AUROC
•	Per-label PR-AUC
________________________________________
Explainability
Grad-CAM heatmaps are generated for:
•	CustomCNN
•	ResNet18
•	VGG19
These visualizations highlight image regions influencing model decisions.
________________________________________
Clinical Summary Generation
A retrieval-based knowledge module provides:
•	Disease definitions
•	Confidence assessment
•	Grad-CAM interpretation
•	Clinical notes
•	Model limitations
•	Research-use disclaimer
________________________________________
Repository Structure
models/
•	customcnn_best_model.pth
•	resnet18_best_model.pth
•	vgg19_best_model.pth
history/
•	customcnn_history.pth
•	resnet18_history.pth
•	vgg19_history.pth
results/
•	final_model_comparison.csv
notebook/
•	NIH_ChestXray14.ipynb
________________________________________
Future Enhancements
•	FastAPI deployment
•	Real-time inference API
•	Clinical report generation using LLMs
•	PACS integration
•	Additional explainability methods
________________________________________
Disclaimer
This system is intended for research and educational purposes only. It is not a medical device and must not replace professional clinical judgment.
