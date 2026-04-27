# VertigoLM 🚀

Welcome to the official training repository for **VertigoLM**! This project open-sources the complete configuration files and scripts used to train VertigoLM and its derivative model series.

Our training workflow is built on the excellent open-source large language model fine-tuning framework [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory).

## 📌 Table of Contents

- [Environment and Setup](#environment-and-setup)
- [Model Training](#model-training)
  - [VertigoLM Training](#vertigolm-training)
  - [VertigoLM-R1 Training](#vertigolm-r1-training)
- [License](#license)

---

## 🛠️ Environment and Setup

Because the core training pipeline of this project depends on LLaMA-Factory, please complete the following environment setup before getting started:

**1. Clone this repository**

```bash
git clone https://github.com/VertigoLM/VertigoLM.git
cd VertigoLM
```

**2. Install LLaMA-Factory**

```bash
git clone https://github.com/hiyouga/LLaMA-Factory.git
cd LLaMA-Factory
pip install -e ".[torch,metrics]"
```

*(Note: Please make sure the correct versions of CUDA and PyTorch are installed in your environment.)*

---

## 🚀 Model Training

The training configurations in this repository are mainly divided into two parts: **VertigoLM** base/fine-tuning training and **VertigoLM-R1** advanced training. We recommend directly using the LLaMA-Factory command-line tool to load the `yaml` files from this repository for training.

### VertigoLM Training

This module contains the configuration files required to build the VertigoLM model.

**Launch command:**

Run the following command from the root directory of `LLaMA-Factory`:

```bash
llamafactory-cli train ../configs/vertigolm/sft.yaml
```

### VertigoLM-R1 Training

This module contains dedicated training configurations for VertigoLM-R1, such as configurations for reinforcement learning, alignment, or improving specific capabilities.

**Launch command:**

Run the following command from the root directory of `LLaMA-Factory`:

```bash
llamafactory-cli train ../configs/vertigolm-r1/sft.yaml
```

---

## 📄 License

This project is licensed under the [Apache 2.0 License](LICENSE).
