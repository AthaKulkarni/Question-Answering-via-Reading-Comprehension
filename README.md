# Question Answering with DistilBERT and LangChain

This project demonstrates the use of Hugging Face's `transformers` library to fine-tune the DistilBERT model on the SQuAD v2 dataset for question answering tasks. Additionally, it includes examples of using the LangChain library to create complex prompt-based workflows with OpenAI's GPT-3.5.

## Table of Contents
- [Introduction](#introduction)
- [Setup](#setup)
- [Fine-tuning DistilBERT on SQuAD v2](#fine-tuning-distilbert-on-squad-v2)
- [LangChain Workflows](#langchain-workflows)
  - [Chain 1: Review Translation and Summarization](#chain-1-review-translation-and-summarization)
  - [Chain 2: MultiPromptChain for Subject-Specific Responses](#chain-2-multipromptchain-for-subject-specific-responses)
- [Results](#results)
- [References](#references)

## Introduction
This project covers two main tasks:
1. Fine-tuning the DistilBERT model for question answering on the SQuAD v2 dataset.
2. Creating complex workflows using LangChain to process and respond to text inputs.

## Setup
To run this project, you'll need Python 3.8 or later and the following libraries:
- `transformers`
- `datasets`
- `pandas`
- `numpy`
- `torch`
- `langchain`
- `openai`
- `ratelimit`

You can install the required libraries using pip:
```bash
pip install transformers datasets pandas numpy torch langchain openai ratelimit

## Fine-tuning DistilBERT on SQuAD v2
The first part of the project involves fine-tuning DistilBERT on the SQuAD v2 dataset. The steps include:

Loading the SQuAD v2 dataset.
Tokenizing the data using AutoTokenizer.
Preparing features for training and validation.
Fine-tuning the model using the Trainer API from transformers.
Post-processing the model's predictions and evaluating its performance using the SQuAD v2 metric.
