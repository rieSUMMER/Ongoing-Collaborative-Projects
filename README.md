# Ongoing-Collaborative-Projects
Ongoing collaborative projects with prof. Erik Cambria in NTU and prof.  Feng-Kuang Chiang in SJTU.

# Uni-RAG: From Query to Explanation

> **Authors**：Xinyi Wu, Yanhao Jia, Luwei Xiao, Shuai Zhao, Fengkuang Chiang, Erik Cambria  
> **Submitted to**: IEEE TKDE, 2025  

## 1. Introduction 论文简介

在AI4EDU教学场景中，如何将多模态查询（如文本、图像、手绘草图、音频）和检索增强生成 (RAG) 结合，并在 STEM 领域提供精准、可解释的学习辅助，是亟待解决的挑战。

## 2. 核心方法

- **Uni-Retrieval**：一个轻量级的多风格检索模块，利用 Prompt Bank + MoE-LoRA 动态匹配查询原型。  
- **RAG Pipeline**：将检索到的上下文输入到指令微调后的 Qwen3，对用户风格化查询生成解释性教学文本。

## 3. 模型架构

![Figure 1: Uni-RAG framework主要内容](images/tkde main.pdf)
![Figure 2: Uni-RAG 模型总体架构](images/tkde tech.pdf)
![Figure 3: Uni-RAG example模型应用案例](images/tkde example.pdf)

*图 1 Uni-RAG 的端到端检索–生成流程*

## 4. 主要贡献

1. **多风格检索-生成一体化**：首次在 STEM 场景中提出查询原型驱动的 RAG 框架；  
2. **可扩展的 Prompt Bank**：MoE-LoRA 机制让检索器能适应新风格输入；  
3. **实证验证**：在 SER 等数据集上，Uni-RAG 在 R@1/R@5、生成质量和推理速度上均超越 baselines。

## 5. 实验结果

| 方法            | Text→Image R@1 | Sketch→Image R@1 | … |
| --------------- | -------------- | ---------------- | - |
| CLIP            | 54.6%          | 47.3%            | … |
| Uni-Retrieval   | 83.2%          | 84.5%            | … |
| **Uni-RAG (Ours)** | **84.1%**    | **85.1%**        | … |

