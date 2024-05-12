# extremist_bias_llm_eval_multi_method

## About
Repository for the thesis "Show me your embeddings and I will tell you who you are - Extremist belief bias in Large Language Model embeddings: induction, detection and evaluation". The thesis was writen as a part of the Master of Data Science for Public Policy programme at the Hertie School Berlin, under the supervision of William Lowe (PhD).

## Overview
add abstract

## Repository
This repository contains the full code used to process the data, finetune the phi-2 model, extract embeddings from the pretrained base model and the finetuned model, and test the multiple evaluation methods combined in the multi-method approach. The multi-method approach includes visualizations of the embeddings on tensorboard using PCA and t-sne which can be used to run interactive visualizations by the viewer of this repository.

## Data
The data is the "ISIS-religious-text" data curated by fith tribe. It is available on kaggle https://www.kaggle.com/datasets/fifthtribe/isis-religious-texts a csv format (last accessed 12.05.2024). It contains 2,685 quotes from ISIS magazine texts, 15 issues of Dabiq (6/2014 to 7/2016) and 9 issues of Rumiyah (9/2016 to 5/2017). It is published under License CC0: Public Domain.
