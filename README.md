The project, "The Issue of Pattern Recognition in EEG Signals," focuses on classifying emotional responses elicited during the viewing of VR videos using EEG data. The experiment involved collecting EEG signals while participants watched VR videos containing positive, neural and negative content. Frequency and statistical features were extracted from the EEG signals using the Fisher method and evolutionary algorithms. Two types of neural network classifiers, Multi-Layer Perceptron (MLP) and Radial Basis Function (RBF) networks, were constructed and trained using cross-validation. This project aims to contribute insights into the application of machine learning in analyzing EEG signals and understanding human cognitive and emotional processes.


# EEG Signal Classification with Feature Extraction and Neural Networks

## Overview
This repository contains the code and report for my *Computational Intelligence* course project at Sharif University of Technology, supervised by Dr. Sepideh Hajipur. The project investigates how **feature extraction and feature selection** influence the performance of neural networks in classifying **EEG signals recorded during 3D VR video exposures**.  

The work integrates time- and frequency-domain analysis of EEG data with optimization-based feature selection, and compares the performance of **Multilayer Perceptron (MLP)** and **Radial Basis Function (RBF)** networks.

---

## Objectives
- To evaluate the impact of feature extraction and selection on EEG classification accuracy.  
- To compare **Fisher Score** and **Particle Swarm Optimization (PSO)** for selecting discriminative features.  
- To benchmark the performance of **MLP** and **RBF** neural networks using the selected feature sets.  

---

## Methodology

### Data and Features
EEG signals were collected during exposure to immersive VR environments. From these signals, **2832 candidate features** were extracted across 59 channels, including:  
- Time-domain features: variance, form factor, amplitude histograms.  
- Frequency-domain features: maximum, mean, and median frequencies, relative band energies.  
- Inter-channel correlations and statistical descriptors.  

### Feature Selection
- **Fisher Score** was applied to rank features based on class separability, and the top 50 features were retained for baseline experiments.  
- **Particle Swarm Optimization (PSO)** was then used to refine feature subsets, with Random Forest accuracy as the fitness function, balancing discriminative power and compactness.  

### Neural Network Models
- **MLP (Multilayer Perceptron)**: trained with parameter tuning, Min–Max normalization, and 5-fold cross-validation.  
- **RBF (Radial Basis Function)**: implemented using SVM with RBF kernel, also validated with 5-fold CV.  
- Experiments compared performance with Fisher-only features versus Fisher+PSO-optimized subsets.  

---

## Results
- **MLP consistently outperformed RBF** in classification accuracy and generalization.  
- **PSO-based feature selection** improved performance beyond Fisher-only selection.  
- The study demonstrated the importance of combining careful feature engineering with optimization-driven feature selection in EEG classification tasks.  

---

## Repository Contents
- `Project_data.mat`: EEG dataset used in experiments.  
- `MLP_RBF.ipynb`: Implementation of MLP and RBF models with Fisher-selected features.  
- `PSO_FeatureSelection.ipynb`: PSO-based feature optimization and comparison.  
- `Report.pdf`: Full project report with methodology, theoretical background, and experimental results.  


Sharif University of Technology – Electrical Engineering

