
# Full Isaac Omniverse Simulation Pipeline for Megatron Humanoid Gait Training

This repository fully integrates NVIDIA Isaac Sim, Omniverse USD pipeline, and Groot N1 foundation models to train Megatron humanoid gaits using human-in-the-loop reinforcement learning.

## Components Included:
- USD scene building for Megatron humanoid
- Groot N1 pretrained model loading and testing
- Terrain generation and difficulty scaling
- Human-in-the-loop simulation controls
- Isaac Gym RL integration

## Usage Workflow:
1. Generate Megatron humanoid scene.
2. Load Groot N1 models.
3. Run interactive training loop with terrain scaling.
4. Visualize gait performance.
5. Deploy to real or simulated hardware.

Here’s a full `README.md` draft you can include directly inside your repository for uploading the zip file and building the Isaac USD Megatron Humanoid model:

---

# Megatron Humanoid Robot: Isaac Sim USD Model Build Guide

---

This repository contains all code, configs, and resources to **generate and train the Megatron Humanoid robot model inside NVIDIA Isaac Sim using Groot N1 foundation models.**

---

## 🚀 Repository Contents

* ✅ **isaac\_omniverse\_pipeline.zip**
* ✅ Scripts for scene generation, training, and simulation
* ✅ Placeholder pretrained models for Groot N1 integration
* ✅ Terrain generation and simulation analysis utilities
* ✅ Full YAML configs for reproducibility

---

## 📦 Quick Start — Upload and Unpack

1️⃣ Upload `isaac_omniverse_pipeline.zip` into your Isaac Sim working directory.

2️⃣ Unpack:

```bash
unzip isaac_omniverse_pipeline.zip
cd isaac_omniverse_pipeline
```

---

## 🔧 Environment Setup

### Prerequisites:

* NVIDIA Isaac Sim 2024.1+ (USD Composer or Isaac Lab)
* Omniverse Kit Extensions: Isaac Sim, OmniGraph, Physics, USD Composer
* Python 3.8+
* CUDA 12.x + compatible GPU (RTX 4090 / A6000 recommended)

### Install Dependencies:

```bash
pip install -r requirements.txt
```

---

## ⚙ USD Model Generation Pipeline

### 1️⃣ Generate the Megatron Humanoid USD model

```bash
python scenes/generate_megatron_usd.py
```

* This script uses Omniverse Kit APIs to procedurally build:

  * Skeletal joints
  * Collision meshes
  * Actuator definitions
  * Sensor placeholders
  * Proper USD hierarchy

### 2️⃣ Generate Simulation Terrains

```bash
python scenes/terrain_generator.py
```

* Automatically creates mixed terrains:
  flat, stairs, ramps, obstacles, uneven grounds.

---

## 🧠 Load Groot N1 Policy

Once model is built, load the pretrained Groot N1 gait control policy:

```bash
python policies/load_groot_n1.py
```

*(Note: pretrained `.pth` model file included as placeholder. Replace with actual NVIDIA Groot N1 model if available.)*

---

## 🎮 Human-In-The-Loop Training

Start interactive fine-tuning loop:

```bash
python training/hitl_training_loop.py
```

* Use keyboard or controller inputs for HITL corrections.
* Human feedback fine-tunes balance, step-length, stability, energy efficiency.

---

## 📊 Visualization & Evaluation

Analyze gait performance and learning curves:

```bash
python visualization/gait_performance_plot.py
```

OR launch interactive notebook:

```bash
jupyter notebook notebooks/simulation_analysis.ipynb
```

---

## 🧪 Isaac Gym RL Expansion (Optional)

For reinforcement learning curriculum training:

```bash
python training/isaac_gym_rl.py
```

---

## 🌐 USD Files Location

Once generated, all USD files will reside inside:

```
megatron_usd/
 └── megatron_humanoid.usd
```

You can directly import these USDs into Isaac Sim Composer or Omniverse Code for debugging and extensions.

---

## 📚 Resources

* [NVIDIA Isaac Sim Docs](https://docs.omniverse.nvidia.com/isaacsim/latest/)
* [Omniverse USD Composer](https://developer.nvidia.com/nvidia-omniverse-platform)
* [NVIDIA Groot N1](https://nvidianews.nvidia.com/news/nvidia-isaac-gr00t-n1-open-humanoid-robot-foundation-model)

---

## ✅ Future Extensions

* Full-body humanoid dexterity using Groot N1 multi-modal foundation.
* Contact-rich manipulation and locomotion fusion.
* Isaac Lab distributed RL across Omniverse clusters.
* Deployment bridge to real Megatron prototype hardware.

---

**Author:**
*Dr. Bheemaiah Anil K — Robotics Architect*
*Generated via GPT-4o Simulation Pipeline*

---




