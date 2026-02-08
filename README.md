# ViscoMamba: A Physics-Informed Grey-Box World Model for Cross-Modal Haptic-Visual Fusion in Robotic Surgery



> **📢 Note to Reviewers and Readers:** > This repository contains the official implementation of the paper **"ViscoMamba: A Physics-Informed Grey-Box World Model for Cross-Modal Haptic-Visual Fusion in Robotic Surgery"**, currently submitted to *The Visual Computer*.  
> To facilitate reproducibility, we provide the complete source code for the LuGre friction model, ViscoMamba encoder, and Stiffness-NeRF rendering module.

---

## 📖 Abstract

Lumbar puncture, a critical procedure in hematological malignancy management, relies on detecting a subtle haptic cue—the Loss of Resistance (LOR)—which is often masked by tissue friction and physiological noise. Existing robotic solutions struggle to balance physical interpretability with data-driven adaptability. To bridge this gap, we introduce **ViscoMamba**, a physics-informed grey-box neural world model for haptic-visual fusion. We embed discretised Kelvin-Voigt viscoelastic equations into a Mamba State Space Model, initialising the network with biomechanical priors for interpretable state estimation. Furthermore, we extend the Neural Radiance Field to reconstruct a 3D Stiffness Field, enabling visual perception of deep-tissue mechanics. 

Here we show that our framework achieves superior performance: on physics-based synthetic data, it attains a force estimation RMSE of 0.65 N and reduces LOR detection latency to 12.5 ms, significantly outperforming state-of-the-art sequence models. On public benchmarks (JIGSAWS, Cholec80), ViscoMamba demonstrates enhanced long-sequence modelling accuracy and linear computational efficiency. This work provides a transparent and efficient paradigm for perceiving invisible mechanical properties, advancing towards safer robot-assisted minimally invasive surgery.

<div align="center">
  </div>

---

## 🛠️ Installation

### 1. Environment Requirements
* **OS**: Linux (Ubuntu 20.04/22.04 recommended)
* **Python**: 3.8+
* **CUDA**: 11.8+ (Required for Mamba and PyTorch3D)
* **PyTorch**: 2.1.0+

### 2. Setup
Clone the repository and install dependencies:

```bash
git clone [https://github.com/](https://github.com/)[YOUR_GITHUB_USERNAME]/ViscoMamba.git
cd ViscoMamba

# Create a virtual environment (Recommended)
conda create -n viscomamba python=3.10
conda activate viscomamba

# Install dependencies
pip install -r requirements.txt
