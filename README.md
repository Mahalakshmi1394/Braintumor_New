# Deep Neural Networks for Brain Tumor Segmentation and Stage Identification

## Overview
Accurate brain tumor diagnosis from MRI scans is challenging due to complex tumor structures, intensity variations, and the need for expert interpretation. Manual analysis is time-consuming and often inconsistent.  
This project presents a **unified deep learning framework** that performs **automatic brain tumor segmentation** and **tumor stage classification** in a single workflow, supporting reliable and efficient clinical decision-making.

The proposed system integrates an **Enhanced U-Net** for precise tumor segmentation with a **CNN-based classifier** for predicting WHO tumor grades (II, III, and IV).

## Objectives
- Automate brain tumor segmentation from MRI images  
- Classify tumor severity into WHO Grade II, III, and IV  
- Reduce manual workload and inter-observer variability  
- Provide a clinically viable and scalable diagnostic pipeline  


## Key Contributions
- Enhanced U-Net with **attention gates**, **residual connections**, **batch normalization**, and **dropout** for accurate tumor boundary detection  
- CNN-based tumor grading model operating on segmented tumor regions  
- End-to-end unified pipeline from MRI input to final diagnosis  
- Robust performance across diverse MRI scans  

## System Workflow
Input MRI → Preprocessing → Tumor Segmentation → Tumor Extraction
→ CNN-based Grade Classification → Output Visualization
<img width="1920" height="1080" alt="Combine Outputs Combine segmentation mask from Enhanced U-Net Combine tumor grade prediction from CNN Evaluation Metrics Segmentation metrics Dice Similarity Coefficient (DSC) Hausdorff Distance (" src="https://github.com/user-attachments/assets/97764f7c-c2df-4c5e-a287-c07920233ad9" />


## Methodology
- **Preprocessing:** MRI normalization and registration  
- **Data Augmentation:** Rotation, elastic deformation, and brightness adjustments  
- **Patch Extraction:** 128 × 128 patches  
- **Segmentation Model:** Enhanced U-Net  
- **Classification Model:** 13-layer CNN with Softmax activation  



## Dataset
- **BraTS 2021 Dataset**
  - 1251 multi-modal MRI volumes
  - Expert-annotated tumor regions
  - Standard benchmark for brain tumor analysis



## Implementation Details
- Framework: TensorFlow / Keras  
- Optimizer: Adam  
- Learning Rate: 0.0001  
- Batch Size: 32  
- Segmentation Training: 100 epochs  
- Classification Training: 50 epochs  
- Hardware: NVIDIA RTX GPU  



## Results
### Segmentation Performance
- Dice Similarity Coefficient (DSC): **0.925**

### Classification Performance
- Accuracy: **93%**
- Precision: up to **0.96**
- Recall: up to **0.98**
- F1-Score: **0.97**

The model demonstrates strong generalization, effective tumor localization, and reliable grade prediction, making it suitable for real-world clinical workflows.

<img width="1920" height="1401" alt="Screenshot 2025-11-28 at 10-17-49 Brain Tumor Segmentation Severity Analysis (Demo Model)" src="https://github.com/user-attachments/assets/8505fee1-5971-4a85-bafd-24ee2a0da27a" />


## Output
- Segmented tumor overlays on MRI scans  
- Predicted WHO tumor grade (II / III / IV)  
- Clear visual and quantitative evaluation results  


## Future Work
- Integration of transformer-based architectures for enhanced global context modeling  
- Validation on real hospital datasets  
- Incorporation of explainable AI techniques for clinical transparency  
- Deployment as a web or mobile-based diagnostic tool  
- Optimization for faster inference and real-time reporting  

## Publication Information
- **Conference:** 10th International Conference on Smart Structures and Systems (ICSSS 2025)  
- **Paper Title:** Deep Neural Networks for Brain Tumor Segmentation and Stage Identification  
- **Paper ID:** ICSSS25BIOM103  


## Project Notebook
Google Colab:  
https://colab.research.google.com/drive/1pgGyeJhDazGKbLs5dJziLt4U3Kj8hv85
