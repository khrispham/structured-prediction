# Structured Prediction: Sequence Tagging with HMMs and CRFs

This project implements probabilistic models for sequence tagging tasks in natural language processing, including Hidden Markov Models (HMMs) and Conditional Random Fields (CRFs).

## Overview

This project explores sequence tagging by implementing both generative (HMM) and discriminative (CRF) models and comparing their behavior in practice. All models were implemented in Python with minimal reliance on high-level ML libraries, focusing on understanding the underlying algorithms. 

In this project, I implemented:

- Hidden Markov Models (HMMs) for probabilistic sequence modeling
- Conditional Random Fields (CRFs) for discriminative sequence tagging
- Training and inference procedures for both models
- Evaluation of tagging performance on labeled datasets

This project evaluates part-of-speech tagging on endev, measuring accuracy and cross-entropy. The results highlight the tradeoffs between generative and discriminative models, and provides insight into how structured prediction differs from standard classification tasks.

## Skills Demonstrated

- Python programming
- Probabilistic modeling and structured prediction
- Implementation of sequence models (HMM, CRF)
- Working with linguistic datasets and evaluation metrics

## How to Run

### 1. Train a supervised model

python3 tag.py <dev_data> --model model.pkl --train <supervised_data>

### 2. Train a semi-supervised model:

python3 tag.py <dev_data> --model <final_model.pkl> --checkpoint <pretrained_model.pkl> --train <training_data>

### 3. Run HMM-augmented tagging:

python3 tag.py <input_file> --model <model_file.pkl> --train <training_files> 

### 4. Run tagging

python3 tag.py <input_file> --model model.pkl

### 5. Evaluate performance

python3 tag.py <input_file> --model model.pkl --loss viterbi_error

## Notes

While modern NLP often relies on neural network models, HMMs and CRFs remain foundational methods for understanding structured prediction and sequence modeling. This project reflects hands-on experience implementing and evaluating these approaches. 