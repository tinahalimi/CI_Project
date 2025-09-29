# EEG Signal Classification with Feature Extraction and Neural Networks

## Overview
This repository contains the code and report for my *Computational Intelligence* course project at Sharif University of Technology, supervised by Dr. Sepideh Hajipur. The project addresses the problem of **pattern recognition in EEG signals**, focusing on classifying emotional responses (positive, neutral, and negative) elicited while participants watched immersive VR videos.  

The study explores how **feature extraction and selection** impact the performance of neural network classifiers, combining time- and frequency-domain analysis of EEG data with optimization-based feature selection.

---

## Objectives
- To classify EEG responses to VR stimuli into emotional categories.  
- To apply **Fisher Score** and **Particle Swarm Optimization (PSO)** for selecting the most discriminative EEG features.  
- To evaluate and compare the performance of **Multilayer Perceptron (MLP)** and **Radial Basis Function (RBF)** neural networks using cross-validation.  

---

## Methodology

### Data Collection
EEG signals were recorded from participants during the viewing of VR videos containing **positive, neutral, and negative content**.

### Feature Extraction
A wide range of features were extracted, including:  
- **Time-domain features**: variance, amplitude histograms, and form factor.  
- **Frequency-domain features**: maximum, mean, and median frequencies, relative band energies.  
- **Statistical and correlation-based features** across multiple channels.  
In total, **2832 features** were derived from 59 EEG channels.  

### Feature Selection
- **Fisher Score** was used for initial ranking of features based on class separability.  
- **PSO (Particle Swarm Optimization)** was then applied to optimize feature subsets, using Random Forest accuracy as the fitness measure to refine and select the most relevant features.  

### Classification Models
- **MLP (Multilayer Perceptron)**: trained with parameter tuning, normalization, and 5-fold cross-validation.  
- **RBF (Radial Basis Function)**: implemented with an SVM RBF kernel, also validated with 5-fold cross-validation.  
- Classification results were compared across Fisher-only features and Fisher+PSO-optimized features.  

---

## Results
- **MLP networks achieved higher accuracy** than RBF across all feature sets.  
- **PSO-based feature selection** further improved classification accuracy and generalization compared to Fisher-only selection.  
- The results demonstrate the value of combining statistical feature extraction with evolutionary optimization for EEG-based emotion recognition.  

---

## Repository Contents
- `project.ipynb`: Jupyter Notebook implementation of feature extraction, selection, and neural network classifiers.  
- `report.pdf`: Full project report detailing theory, methodology, and results.  

