# Fine-Tuning Conversational Agents: Modeling Personality through Character-Based Dialogue

[![Python Badge](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=fff&style=flat)](https://www.python.org/)
[![PyTorch Badge](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=fff&style=flat)](https://pytorch.org/)
[![Hugging Face Badge](https://img.shields.io/badge/Hugging%20Face-FFD21E?logo=huggingface&logoColor=000&style=flat)](https://huggingface.co/)

This work explores the integration of personality into conversational agents by fine-tuning **DialoGPT-small** on two contrasting datasets: the **Cornell Movie-Dialogs Corpus** and character-specific dialogue from the **Friends** TV show. The goal is to compare generic versus persona-specific behavior in dialogue generation. Using **Hugging Face’s Transformers** and **PyTorch**, a full training pipeline was implemented. Evaluation includes Loss, Perplexity, BLEU, ROUGE-L, and emotion alignment via a DistilRoBERTa-based classifier grounded in Ekman’s six basic emotions.

## Link to Colab Notebooks
- load_and_process_movie_corpus.ipynb: [![Google Colab Badge](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=fff&style=flat-square)](https://colab.research.google.com/github/Sabaudian/Neural_Conversational_Agents_project/blob/main/load_and_process_movie_corpus.ipynb)
- load_and_process_friends_dataset.ipynb: [![Google Colab Badge](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=fff&style=flat-square)](https://colab.research.google.com/github/Sabaudian/Neural_Conversational_Agents_project/blob/main/load_and_process_friends_dataset.ipynb)
- build_chatbot.ipynb: [![Google Colab Badge](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=fff&style=flat-square)](https://drive.google.com/file/d/1J9UOfUoUKnvHuQhG09LO1p5ACFQ8b2b4/view?usp=sharing)

## Introduction
