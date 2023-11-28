# summarization
Example of text summarization

* Model: Sequence-to-sequence model
    * decode-only model needs examples: one shot or few shot.
    * Potential baseline model: the first three sentences.
    * T5 or Flan T5?
        * it has prefix: `summarize:`, `document:`, versatile, https://huggingface.co/docs/transformers/model_doc/t5
        * https://huggingface.co/docs/transformers/model_doc/flan-t5
* Data source
    * Longform Article summarization: https://huggingface.co/datasets/vgoldberg/longform_article_summarization?row=0 (too long)
    * CNN daily mail: https://huggingface.co/datasets/cnn_dailymail average token 781, summary: 56 tokens, download last months: 94k
    * Bill Summary: https://huggingface.co/datasets/dreamproit/bill_summary_us , text: 4,687 chars, summary: 640 chars, download: 3
    * Medical meadow: https://huggingface.co/datasets/medalpaca/medical_meadow_cord19, from abstract to title, download: 127 (sometimes: non-english)
    * Chemical summary: https://huggingface.co/datasets/griffin/ChemSum, from abstract to title, download: 122
    * Selected Bill Summary data
* Data Analysis: the number of tokens
* Metrics: ROUGE score
* instruction fine tuning with QLORA
* Data Loading: dataset or iterable dataset: https://huggingface.co/docs/datasets/about_mapstyle_vs_iterable