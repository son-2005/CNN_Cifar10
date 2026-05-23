# CIFAR-10 Image Classification using ResNet18

This repository contains a high-performance image classification project using Transfer Learning on the CIFAR-10 dataset.

## 🚀 Final Results & Performance
By tuning the optimization strategy from AdamW to **SGD with Momentum**, the model achieved textbook-perfect convergence and a significant boost in performance:
* **Final Test Accuracy:** `95.79%`
* **Final Test Loss:** `0.1639`
* Trained smoothly for `20 epochs` with `CosineAnnealingLR` scheduler.

## 📊 Classification Metrics
The model shows exceptional balance across all categories, achieving an overall macro average of **96%** for Precision and Recall.

* **Top Performing Classes:** `Horse` (98.37% Precision), `Frog` (98.28% Precision), and `Ship` (97.78% Precision).
* **Challenging Classes:** `Cat` (90.39% F1-Score) due to typical visual similarities with dogs in the CIFAR-10 dataset.

## 🛠️ Project Setup & Architecture
* **Base Model:** ResNet18 (Pre-trained on ImageNet)
* **Optimizer:** SGD (Learning Rate = 0.01, Momentum = 0.9, Weight Decay = 1e-4)
* **LR Scheduler:** CosineAnnealingLR (T_max=20, eta_min=1e-5)
* **Data Augmentation:** Random Horizontal Flip, Random Rotation (15°), Color Jitter (Brightness/Contrast).
* **Input Image Size:** Resized to 128x128.

