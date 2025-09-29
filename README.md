The project, "The Issue of Pattern Recognition in EEG Signals," focuses on classifying emotional responses elicited during the viewing of VR videos using EEG data. The experiment involved collecting EEG signals while participants watched VR videos containing positive, neural and negative content. Frequency and statistical features were extracted from the EEG signals using the Fisher method and evolutionary algorithms. Two types of neural network classifiers, Multi-Layer Perceptron (MLP) and Radial Basis Function (RBF) networks, were constructed and trained using cross-validation. This project aims to contribute insights into the application of machine learning in analyzing EEG signals and understanding human cognitive and emotional processes.


# EEG Signal Classification with Feature Extraction and Neural Networks

## Overview
This repository contains the code and report for my *AI and Biological Computation* course project at Sharif University of Technology, supervised by Dr. Sepideh Hajipur. The project investigates the impact of feature extraction and selection on the performance of neural networks, specifically focusing on **EEG signal classification in response to VR stimuli**.  

The work combines time- and frequency-domain feature extraction, statistical analysis, and advanced feature selection methods with machine learning models to achieve effective EEG pattern recognition.

---

## Objectives
- To examine how feature extraction and feature selection influence classification performance.  
- To apply **Fisher Score** and **Particle Swarm Optimization (PSO)** for selecting the most relevant features from EEG data.  
- To compare the performance of **Multilayer Perceptron (MLP)** and **Radial Basis Function (RBF)** neural networks under different feature sets.  

---

## Methodology

### Data & Feature Extraction
- EEG signals recorded during **3D VR video exposure** were used.  
- Extracted features included maximum, mean, and median frequencies; relative energy of power spectrum bands; variance; amplitude histograms; form factor; and inter-channel correlations.  
- A total of **2832 features** were computed across 59 channels.  

### Feature Selection
- **Fisher Criterion**: Ranked features by discriminative power; top 50 features were selected for baseline experiments.  
- **Particle Swarm Optimization (PSO)**: Applied to optimize feature subsets, balancing classification accuracy and compact feature sets using Random Forest as the fitness evaluator.  

### Neural Network Models
- **Multilayer Perceptron (MLP)**: Trained with Min–Max normalization, parameter tuning, and 5-fold cross-validation.  
- **Radial Basis Function (RBF)**: Implemented using SVM with RBF kernel, also trained with cross-validation.  
- Comparative experiments assessed Fisher-only features vs. Fisher + PSO optimized subsets.  

---

## Results
- MLP consistently outperformed RBF in classification accuracy.  
- Feature selection with **PSO** improved model generalization compared to Fisher-only selection.  
- The experiments confirmed that carefully designed feature extraction and selection pipelines significantly enhance EEG signal classification performance.  

---

## Repository Contents
- `Project_data.mat` — EEG dataset used for training and testing.  
- `MLP_RBF.ipynb` — Implementation of MLP and RBF models with Fisher-based feature selection.  
- `PSO_FeatureSelection.ipynb` — PSO-based feature optimization experiments.  
- `Report.pdf` — Full project report with methodology, derivations, and results.  

Sharif University of Technology – Electrical Engineering

