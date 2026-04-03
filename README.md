# VertigoLM 🚀

欢迎来到 **VertigoLM** 的官方训练仓库！本项目开源了我们训练 VertigoLM 及其衍生系列模型所使用的完整配置文件和脚本。

我们的训练流程基于优秀的开源大语言模型微调框架 [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) 构建。

## 📌 目录
- [环境与准备](#环境与准备)
- [模型训练](#模型训练)
  - [VertigoLM 训练](#vertigolm-训练)
  - [VertigoLM-R1 训练](#vertigolm-r1-训练)
- [License](#license)

---

## 🛠️ 环境与准备

由于本项目的训练核心依赖于 LLaMA-Factory，请在开始前完成以下环境配置：

**1. 克隆本仓库**
```bash
git clone [https://github.com/VertigoLM/VertigoLM.git](https://github.com/VertigoLM/VertigoLM.git)
cd VertigoLM
````

**2. 安装 LLaMA-Factory**

```bash
git clone [https://github.com/hiyouga/LLaMA-Factory.git](https://github.com/hiyouga/LLaMA-Factory.git)
cd LLaMA-Factory
pip install -e ".[torch,metrics]"
```

*(注：请确保你的环境中已安装正确版本的 CUDA 和 PyTorch)*

-----

## 🚀 模型训练

本仓库的训练配置主要分为两大部分：**VertigoLM** 基础/微调训练，以及 **VertigoLM-R1** 进阶训练。我们建议直接使用 LLaMA-Factory 的命令行工具加载本仓库的 `yaml` 文件进行训练。

### VertigoLM 训练

此模块包含构建 VertigoLM 模型所需的配置文件。

**启动指令：**
在 `LLaMA-Factory` 根目录下执行以下命令：

```bash
llamafactory-cli train ../configs/vertigolm/sft.yaml
```


### VertigoLM-R1 训练

此模块包含 VertigoLM-R1 的专属训练配置（例如针对强化学习、对齐或特定能力提升的配置）。

**启动指令：**
在 `LLaMA-Factory` 根目录下执行以下命令：

```bash
llamafactory-cli train ../configs/vertigolm-r1/sft.yaml
```

-----

## 📄 License

本项目遵循 [Apache 2.0 License](https://www.google.com/search?q=LICENSE) 开源协议。

