# bRinGIToN
ASR and MT for Romagnol (rgn).

In this repository, you can find the code used to establish new benchmarks for **Automatic Speech Recognition (ASR)** and **Machine Translation (MT)**  for a low-resource regional language spoken in Romagna, Italy, i.e. **Romagnol** (rgn). <br>
The speech and text data in Romagnol and Italian that we collected for this project and with which we built the Romagnol corpus (encompassing a monolingual and a parallel (rgn-ita) subcorpus), is not being released yet.  

1. *asr_rgn_pipeline.ipynb*: the Jupyter Notebook for zero-shot ASR and fine-tuning of six pre-trained models all relying on Whisper architecture, three of which are generic multilingual models (*Whisper Large*, *Whisper Medium*, and *Whisper Small*) and three are Italian-adapted models (*BuzzASR*, *Litus-ai*, *Sandiago21*). 
2. *mt_rgn_ita_pipeline.ipynb*: the Jupyter Notebook for translation out of the box from Romagnol into Italian and from Italian into Romagnol using two distilled NLLB-200 models (*NLLB-200-600M* and *NLLB-200-1.3B*) and to fine-tune them using Low-rank Adaptation (LoRA).

Additionally, we share:
- fine-tuned weights of the best-performing models?
- Tables with ASR and MT baseline and fine-tuned results?
- a UI demo that implements Romagnol speech recognition (transcription) and translation (rgn2ita and ita2rgn) in real time (coming soon).

The other resources shared in this repository are:
1. *pre-processing_pipeline.ipynb*: the Jupyter Notebook used for pre-processing (normalize, align and segment, partition) the speech and text data in the Romagnol corpus.
2. *transfer_effects_ita.ipynb*: the Jupyter Notebook used to test whether transfer learning can happen from Romagnol to Italian with ASR models.
3. *environment.yml*: a .yml doc with all the specific CODA and pip dependencies of the environment where ASR and MT experiments were run.


References:

https://openai.com/index/whisper/ <br>
https://huggingface.co/openai/whisper-large-v3 <br>
https://huggingface.co/openai/whisper-medium <br>
https://huggingface.co/openai/whisper-small <br>
https://huggingface.co/BuzzASR/italian?library=transformers <br>
https://huggingface.co/Sandiago21/whisper-large-v2-italian <br>
https://huggingface.co/litus-ai/whisper-small-ita <br>
https://huggingface.co/facebook/nllb-200-distilled-600M <br>
https://huggingface.co/facebook/nllb-200-distilled-1.3B <br>
