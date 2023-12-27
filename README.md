# Summary U.S. Bills
Example of text summarization task using LLM

## Synopsis
Text summarization automatically creates a summary of information from the original text. Though there are several Large Language Models (LLM) available for text summarization task, those LLMs has been trained on generic dataset. All AI/ML models are data-dependent, and running summarization task from the off-the-shelf pretrained LLM on those speciicalized text may not yield desirable performance. As such, if we want to summarize specialized text (e.g., medical texts, scientific articles, and legal documents), it will also train LLMs on those specialized texts using task-specific examples. This process is called instruction fine tuning. One of the challenges in training LLM is size of the models, often requiring high-end compute servers to train the models. Thus, it is not feasible to train the whole LLM using common PC. Another challege is catestrophic forgetting, which means reductions in ability on other tasks than the task trained for. One approach to overcome such high computational demand and catestrophic forgetting related to fine tuning is Parameter Efficient Fine Tuning (PEFT).

In this project, I will demonstrate improved performance of LLMs for U.S. Bills (proposed laws) which are specialized and structured document, utilizing PEFT from my personal computer with a single GPU. Current progress of PEFT results yielded approximately 50% improved performance on ROUGE scores over pretrained LLM model.

## Goal
Develop an LLM model to summarize U.S. Bills. Use LoRA and QLoRA as PEFT techniques.

* Foundation model: Flan-T5 base model 
  * Reference: Scaling Instruction-Finetuned Language Models [https://arxiv.org/pdf/2210.11416.pdf].
  * Sequence-to-sequence model.
  * Instruction prefix. 

* Data source    
    * Bill Summary: https://huggingface.co/datasets/dreamproit/bill_summary_us

* Metric: ROUGE Score

## Note: this work is in progress
* Currently implemented generate text summarization using pretrained model and LORA.
* The plan is to fine tune foundation model specific to U.S. Bill summary data using QLORA.
* Current version incorporates all helper functions in notebooks. Future plan is to develop a python library and 
to move the helper functions to the python library. 

## Structure of repo
* notebooks
    * 01_raw_data.ipynb: Download raw data and split dataset for preprocessing.
    * 02_preprocessing.ipynb: Preprocessing data.
    * 03a_modeling_pretrained.ipynb: Generate text summary using pretrained model.
    * 03b_modeling_lora.ipynb: Fine-tune LLM using LORA, and generate text summary using fine-tuned model.
* src: helper functions: currently all helper functions are in the notebooks. Move them to `src` folder in the future.
* data: folder for data. Not uploaded to Git due to large size.
* models: models and generated summary. Not uploaded to Git due to large size.

## License
MIT License
