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


# Fine-tuning DistilBERT on SQuAD v2

The first part of the project involves fine-tuning DistilBERT on the SQuAD v2 dataset. The steps include:

1. **Loading the SQuAD v2 dataset.**
2. **Tokenizing the data using AutoTokenizer.**
3. **Preparing features for training and validation.**
4. **Fine-tuning the model using the Trainer API from transformers.**
5. **Post-processing the model's predictions and evaluating its performance using the SQuAD v2 metric.**

# LangChain Workflows

## Chain 1: Review Translation and Summarization

- Translates a non-English review into English.
- Summarizes the translated review.
- Identifies the language of the original review.
- Generates a follow-up message in the original language.
- Translates the follow-up message back into English.

## Chain 2: MultiPromptChain for Subject-Specific Responses

- Utilizes a router chain to direct questions to different prompt templates based on the subject matter.
- Provides subject-specific responses or generic responses if the subject is not recognized.

# Results

- **DistilBERT Fine-tuning**: The fine-tuned model was saved as `SQuAD_trained` and achieves competitive accuracy on the SQuAD v2 validation set.
- **LangChain Workflows**: The LangChain workflows successfully handle complex text processing tasks, including translation, summarization, and subject-specific question answering.
