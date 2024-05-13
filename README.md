# extremist_bias_llm_eval_multi_method

## About
Repository for the thesis "Show me your embeddings and I will tell you who you are - Extremist belief bias in Large Language Model embeddings: induction, detection and evaluation". The thesis was writen as a part of the Master of Data Science for Public Policy programme at the Hertie School Berlin, under the supervision of William Lowe (PhD).

## Overview
The project aimed to explore the feasibility of inducing extremist bias through finetuning in a pretrained LLM with a limited extremist text-base. The specific finetuning applied was IT and QLoRA on the phi-2 model. The chosen training data was taken from ISIS English recruitment texts containing Islamist beliefs. These were processed into training data as quotes. Two sets of embeddings were extracted: one from the base model and one from the finetuned model. Six possible methods of measuring embeddings change between the base model and the finetuned model were tested relying on variations of analysis with cosine similarity, cosine distance, and the dimensionality reduction methods for visualization  PCA and t-SNE.

## Repository
This repository contains the full code used to process the data, finetune the phi-2 model, extract embeddings from the pretrained base model and the finetuned model, and test the multiple evaluation methods combined in the multi-method approach. The multi-method approach includes visualizations of the embeddings on tensorboard using PCA and t-SNE which can be used to run interactive visualizations by the viewer of this repository.

## Navigation
* The finetuned model, its response test and the extraction of embeddings from it can be found in the notebbok Experimental_Finetuhne_phi_2
* The base model's response test is in the notebook response_phi_2, the base model embedding extraction is in the notebook base_model_embeddings
* The method applications can be found in the notebooks cosine_similarity_2_embeddings, embedding_word_distance_bm, embedding_word_distance_fm, sclaes_bm, scales_fm
* The notebooks creating the tensorboard dynamic 3D visualizations are tensorboard_embeddings_bm and tensorboard_embeddings_finetuned
* The visualization plot created for the scale as shown in the paper can be recreated with vizz_scales
  
## Data
The data is the "ISIS-religious-text" data curated by fith tribe. It is available on kaggle https://www.kaggle.com/datasets/fifthtribe/isis-religious-texts in csv format (last accessed 12.05.2024). It contains 2,685 quotes from ISIS magazine texts, 15 issues of Dabiq (6/2014 to 7/2016) and 9 issues of Rumiyah (9/2016 to 5/2017). It is published under License CC0: Public Domain. Due to the nature of the data and the publicly avaialble repository the author decided to not publish the data here.

## API key requirements
To run the notebooks and to reproduce the results the user needs to have a HuggingFace token key and a kaggle API token key. These can be obtained free of charge once a user account is created.

## Sources and building on prior work
* to interact with and finetune the phi-2 model the transformers library and its documentation were used and indications in the notebooks are visible 
* where indicated in the notebooks ChatGPT was used to support changing file formats and for other minor operations, as there were several iterations and own modifications even where it was used to support, the genral timeframe of use was 15.02.2024 to 12.05.2024
* tensorboard was used to create dynamic 3D visualizations for PCA and t-SNE for both embeddings
