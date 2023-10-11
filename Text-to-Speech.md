# Bark Text-to-Speech (TTS) with Semantic Generation

This repository contains a Python script that demonstrates the usage of the Bark Text-to-Speech (TTS) library for generating human-like speech from text. The code showcases how to use Bark to convert text into high-quality audio and includes an example of generating speech from a given script.

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1j1zLLM9jyUK_z6FnWaIVDyPRObYOtYhj?usp=sharing)
Use the above link to access the colab file.


## Prerequisites

Before running the code, ensure you have the following dependencies installed:

1. Python
2. The `bark` library - You can install it using pip with `!pip install git+https://github.com/suno-ai/bark.git -q`.
3. NLTK (Natural Language Toolkit) - You can install it using pip with `!pip install nltk`.

## Usage

1. Open a Python environment or Jupyter Notebook.
2. Copy the code provided in this repository into your Python environment or Jupyter Notebook.
3. Execute the code cell by cell.

The code is divided into the following components:

1. Installation of the Bark TTS library.
2. Preloading of TTS models and setting up the environment.
3. Generation of audio from a given script.
4. Playing the generated audio.

## Generating Audio

The script contains a text passage that you want to convert into speech. In this example, we use the provided script, which is an excerpt from a famous poem. You can replace the script with your own text to generate audio from your content.

The script is divided into sentences, and for each sentence, Bark generates high-quality audio. You can customize the text, speakers, and other parameters as needed.

## Playing the Generated Audio

The generated audio is played using IPython's `Audio` module, which allows you to listen to the speech generated from your text.
