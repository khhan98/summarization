# Summary U.S. Bills
Example of text summarization task using LLM

## Goal
Develop an LLM model to summarize U.S. Bills

* Foundation model: Flan-T5 base model 
  * Reference: Scaling Instruction-Finetuned Language Models [https://arxiv.org/pdf/2210.11416.pdf].
  * Sequence-to-sequence model.
  * Instruction prefix. 

* Data source    
    * Bill Summary: https://huggingface.co/datasets/dreamproit/bill_summary_us

* Metric: ROUGE Score

## Note: this work is under development
* The plan is to fine tune foundation model specific to U.S. Bill summary data using QLORA.
* Current version uses the pretrained model to summarize the U.S. Bills.
* Current version incorporates all helper functions in notebooks. Future plan is to develop a python library and 
to move the helper functions to the python library. 

## License
MIT License
