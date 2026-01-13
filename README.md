# Offline Reinforcement Learning (Offline RL) — Survey & Course Project (EEE448/548)

This repository contains our course project report on **Offline Reinforcement Learning (Offline RL)**: learning policies **purely from a fixed dataset** of past interactions, without additional environment rollouts. The report focuses on the **core offline RL challenge: distributional shift / extrapolation error**, surveys seminal foundations, reviews state-of-the-art methods, and discusses open research directions.

## What’s inside

### Core problem
Offline RL learns from a static dataset \(D=\{(s_i,a_i,r_i,s_{i+1})\}_{i=1}^N\) collected by a behavior policy \(\pi_\beta\).  
The central difficulty is **distributional shift**: the learned policy \(\pi\) may choose actions rarely (or never) seen in the dataset, causing **unreliable Q-value estimates** and **error amplification via bootstrapping**.

### Covered topics (high level)
- **Why Offline RL matters**: safety-critical or expensive exploration (healthcare, finance, autonomy, industrial logs).
- **Seminal works**
  - Tree-based / batch RL foundations (e.g., Fitted Q-Iteration)
  - Stable off-policy TD learning with function approximation (importance sampling + eligibility traces)
  - Off-policy evaluation (Doubly Robust estimation)
- **State-of-the-art Offline RL**
  - **BCQ** (batch-constrained actions via generative modeling)
  - **CQL** (conservative Q-values for out-of-distribution actions)
  - **BRAC+** (behavior regularization with improved divergence handling)
  - **R-BVE** (behavior value estimation + ranking regularization)
- **Open problems**
  - Robustness to low-quality / noisy logs
  - Better representation learning for offline data
  - Interpretability and auditability of learned policies



