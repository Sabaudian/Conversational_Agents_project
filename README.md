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

**Conversational Agents** (CAs), commonly known as chatbots, are systems designed to engage users via natural language, simulating human-like interactions. Within the fields of **Artificial Intelligence** (AI) and **Natural Language Processing** (NLP), CAs represent a particularly complex challenge due to the nuanced and context-sensitive nature of human language.

The objective of this work is to explore how **personality** can be embedded into a neural chatbot’s behavior through dataset-specific fine-tuning. Personality, while abstract, can be approximated through consistent linguistic patterns, emotional tones, and thematic preferences. This study adopts a data-driven approach using the pre-trained **DialoGPT-small** model, a dialogue-specialized variant of `GPT-2`, trained on 147 million Reddit conversations. This model is known for its conversational fluency and contextual relevance, making it a robust base for persona modeling.

Two distinct sources are employed for training:

* The **Cornell Movie-Dialogs Corpus**, used to learn a general "cinematic character" style without targeting a specific identity.
* The **Friends TV Show** dataset from Kaggle, from which character-specific subsets for **Joey Tribbiani** and **Phoebe Buffay** were extracted to construct more explicitly defined personas.

The fine-tuning pipeline is implemented using Hugging Face’s `Transformers` library and PyTorch, with data preprocessing routines to clean, segment, and contextualize dialogue for training. Models are optimized over five epochs using causal language modeling objectives and evaluated using standard metrics: **Loss**, **Perplexity**, **BLEU**, **ROUGE-L**, and **BERTScore**. In addition, emotional alignment is evaluated using a DistilRoBERTa-based classifier grounded in Ekman’s six basic emotions.
