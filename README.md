### Bertinoro International Spring School 2024

# Large Language Models and How to Instruction Tune Them (in a Sustainable Way)

### **Authors**: [Danilo Croce](https://scholar.google.it/citations?user=dXewdYAAAAAJ&hl=it) 

### Many thanks to: [Claudiu Daniel Hromei](https://scholar.google.it/citations?user=YQRKKFoAAAAJ&hl=it) (for supporting the creation of these exaples)

This repository hosts materials from the Bertinoro International Spring School - [BISS-2024 tutorial](https://cs.unibo.it/projects/BISS/2024/), aiming to:

The **objective of this tutorial** is:

* **Introduce the Basics of Distributional Semantics**, and the interplay with neural learning.
* **Introduce Transformer-based architectures**, including encoding-decoding, encoder-only, and decoder-only structures.
* **Demonstrate fine-tuning of Large Language Models** (LLMs) on diverse datasets in a multi-task framework.
* Utilize [Low-Rank Adaptation](https://arxiv.org/abs/2106.09685) (LoRA) for **sustainable and efficient tuning** on "modest" hardware (e.g., single 16GB RAM GPU).



The repository includes code for fine-tuning a Large Language Model (based on [BERT](https://huggingface.co/docs/transformers/model_doc/bert) and [LLaMA](https://ai.meta.com/blog/large-language-model-llama-meta-ai/)) to solve NLP tasks, such as the ones proposed in [EVALITA 2023](https://www.evalita.it/campaigns/evalita-2023/). 


## Code

### Lab 1: Training BERT-based models in few lines of code

This is a Pytorch (+ **Huggingface** transformers) implementation of a "simple" text classifier defined using BERT-based models. 
In this lab we will see how it is simple to use BERT for a sentence classification task, obtaining state-of-the-art results in few lines of python code.

The python book is available at this [**LINK**](BISS-2024_LAB-1_Training_BERT_based_models_in_few_lines_of_code.ipynb).

### Lab 2: Fine-tune a LLaMA-based model to all tasks from EVALITA 2023

At the end, this tutorial shows how to encode data from different tasks into specific prompts and fine-tune the LLM using [Q-LoRA](https://arxiv.org/abs/2305.14314). The code can be also used in Google Colab using an Nvidia-T4 GPU with 15GB memory.

The code is heavily based on the one used in ExtremITA system participating to EVALITA 2023:

* [ExtremITA Paper](https://ceur-ws.org/Vol-3473/paper13.pdf)
* [ExtremITA Github Code](https://github.com/crux82/ExtremITA)


The overall process is divided in four steps:

* [**Step 1 - Encoding the data**](BISS-2024_LAB-2.1_ExtremITA_data_encoder.ipynb): it shows how to encode data from an EVALITA task to generate prompts for the LLM
* [**Step 2 - Fine-tuning the LLaMA model**](BISS-2024_LAB-2.2_ExtremITA_train.ipynb): it shows how to fine-tune the LLMS given the prompts 
* [**Step 3 - Inference: generating answers**](BISS-2024_LAB-2.3_ExtremITA_data_decoder.ipynb): it shows how to use the fined-tuned model
* [**Step 4 - Deconding the data**](BISS-2024_LAB-2.4_ExtremITA_inference.ipynb): it shows how to conver the data to be evaluated in the EVALTA challenge

## Slides

The repository also features **tutorial slides** ([LINK](BISS_2024_slides.pdf)).

## Contacts

For queries or suggestions, raise an Issue in this repository or email  [croce@info.uniroma2.it](mailto:croce@info.uniroma2.it)


