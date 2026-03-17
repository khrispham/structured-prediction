# Structured Prediction: Sequence Tagging with HMMs and CRFs

This project implements probabilistic models for sequence tagging tasks in natural language processing, including Hidden Markov Models (HMMs) and Conditional Random Fields (CRFs).

## Overview

Sequence tagging is a core problem in NLP, where each token in a sequence (e.g., words in a sentence) is assigned a label such as part-of-speech or named entity tags.

In this project, I implemented:

- Hidden Markov Models (HMMs) for probabilistic sequence modeling
- Conditional Random Fields (CRFs) for discriminative sequence tagging
- Training and inference procedures for both models
- Evaluation of tagging performance on labeled datasets

## Skills Demonstrated

- Python programming
- Probabilistic modeling and structured prediction
- Implementation of sequence models (HMM, CRF)
- Working with linguistic datasets and evaluation metrics

## How to Run
Supervised pre-training: 
$ python3 tag.py <dev_data> --model <output_model.pkl> --train <supervised_data>

Semi-supervised training: 
$ python3 tag.py <dev_data> --model <final_model.pkl> --checkpoint <pretrained_model.pkl> --train <training_data>

HMM-augmented tagging:
$ python3 tag.py <input_file> --model <model_file.pkl> --train <training_files> 

Tagging-only deployment:
$ python3 tag.py <input_file> --model <final_model.pkl>

Error rate evaluation:
$ python3 tag.py <input_file> --model <final_model.pkl> --loss viterbi_error

## Notes

While modern NLP often relies on neural network models, HMMs and CRFs remain foundational methods for understanding structured prediction and sequence modeling. This project reflects hands-on experience implementing and evaluating these approaches.