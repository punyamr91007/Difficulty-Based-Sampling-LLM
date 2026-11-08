# Difficulty-Based Sampling for Improving Mathematical Reasoning in Large Language Models

## 1. Project Overview

This research project investigates the use of fixed sampling and difficulty-based adaptive sampling to evaluate and improve mathematical reasoning in Large Language Models (LLMs).

The experiments use the GSM8K mathematical reasoning dataset and the Qwen2.5-0.5B-Instruct language model.

## 2. Objectives

- Study mathematical reasoning capabilities of Large Language Models.
- Implement fixed sampling for mathematical problem-solving.
- Implement difficulty-based adaptive sampling.
- Classify questions based on estimated difficulty.
- Compare fixed and adaptive sampling under the same generation budget.
- Explore GRPO-based fine-tuning using LoRA.

## 3. Technologies and Tools

- Python
- PyTorch
- Hugging Face Transformers
- TRL (Transformer Reinforcement Learning)
- PEFT and LoRA
- GSM8K Dataset
- Google Colab

## 4. Dataset and Model

**Dataset:** GSM8K – Grade School Math 8K

**Base Model:** Qwen2.5-0.5B-Instruct

The dataset contains mathematical word problems that require multi-step reasoning and numerical problem-solving.

## 5. Methodology

The project includes the following experimental stages:

1. Pilot Experiment – Evaluating the model using 3 attempts per question.
2. Fixed Sampling – Generating 5 attempts per question.
3. Adaptive Sampling – Allocating additional attempts based on estimated question difficulty.
4. GRPO Training – Exploring reinforcement learning-based fine-tuning.
5. Performance Evaluation – Comparing accuracy and analyzing experimental findings.

## 6. Experimental Results

### Sampling Comparison

| Experiment | Questions | Generations | Accuracy |
|---|---:|---:|---:|
| Pilot Sampling | 20 | 60 | 76.67% |
| Fixed Sampling | 20 | 100 | 79% |
| Adaptive Sampling | 20 | 100 | 54% |

### GRPO Training Results

| Metric | Result |
|---|---:|
| Original Model Accuracy | 42% |
| GRPO-Trained Model Accuracy | 41% |
| Training Questions | 100 |
| Evaluation Questions | 100 |
| Training Steps | 20 |

### Difficulty-Wise Comparison

| Difficulty | Fixed Sampling | Adaptive Sampling |
|---|---:|---:|
| Easy | 90.91% | 78.79% |
| Medium | 75% | 55.56% |
| Difficult | 56% | 32.50% |

## 7. Main Findings

- Fixed sampling achieved the highest accuracy of 79%.
- Adaptive sampling achieved 54% accuracy and did not outperform fixed sampling.
- GRPO training showed a one-percentage-point decrease compared with the original model.
- Difficulty-based allocation requires further improvement in difficulty estimation and attempt allocation.

## 8. Limitations

- The adaptive sampling controller was evaluated separately and was not directly integrated into the GRPO training loop.
- Model evaluation used a sample of 100 held-out test questions.
- The experiments used a relatively small language model.
- The current results do not establish an improvement in mathematical reasoning through adaptive sampling.

## 9. Repository Contents

- `Difficulty_Based_Sampling_Submission.ipynb` – Research implementation, experiments, evaluation and results.

## 10. Team Members

1. Punya M R
2. Sanjana D M

## 11. Institution

**Jain (Deemed-to-be University)**  
Department of Computer Science and Engineering  
Artificial Intelligence and Machine Learning (AIML)

---

*This repository contains the implementation and experimental findings of our research project.*
