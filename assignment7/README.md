# Audio Translator by NeMo

For this assignment, we decided to try an audio translator from NeMo, which is a repo by NVIDIA. This translator includes various steps with ASR, language models, translation and TTS, but is ultimately simple to use and works quite well.

## Content
In this folder you will find:
- **audio_translation_demo.ipynb** A notebook containing all the necessary code and explanation to do your own audio translation.

For GPU purposes, this notebook works best as a Google Colab notebook with a recording that is under 1 minute. You can find the notebook [here](https://colab.research.google.com/drive/1nSxiTzLYxA9_PPsEK9VU-JIW9orPkVQ1?usp=sharing). 

## About the repo

NVIDIA NeMo is a conversational AI toolkit built for researchers working on automatic speech recognition (ASR), natural language processing (NLP), and text-to-speech synthesis (TTS). The primary objective of NeMo is to help researchers from industry and academia to reuse prior work (code and pretrained models and make it easier to create new conversational AI models.

**How to install**

In the notebook in this folder **audio_translation_demo.ipynb**, you will find the instructions for doing your own audio translation in Google Colab.
If you would like to try it on another platform, you can use the following installation mode if you want the latest released version of the NeMo toolkit (in a Linux environment).

```sh
apt-get update && apt-get install -y libsndfile1 ffmpeg
pip install Cython
pip install nemo_toolkit['all']
```

## How does it work?
The audio translator:

*   Converts audio to written text using ASR
*   Translates the written text to the target language
*   Creates a TTS audio file in the target language from the translated text
  
## Challenges
We first tried this demo on a Chinese recording of the 'North wind'. We saw that the transcription was pretty accurate, but the translations wasn't so great (Google Translate did better). Beyond that, such a long recording being transcribed without punctuation made the TTS recording quite long and hard to listen to. 

After the Chinese recording, we tried running this model on a recording of the 'north wind' in Spanish. It seemed however that this was too large, so we tried a smaller file and then it worked. 

