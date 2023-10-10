
# Text Summarization with Hugging Face Transformers

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1ScT5B-DI1C01zxFGSSY6YHF62xVIWEv2?authuser=1#scrollTo=ZSB2BDs43RIx)

Use the above link to see how the code works.

## Description

This code snippet demonstrates how to perform text summarization using the Hugging Face Transformers library. It utilizes the "facebook/bart-large-cnn" model to summarize a given text.

## Prerequisites

Before running this code, make sure you have the following prerequisites:

- Python installed (Python 3.6 or higher).
- The Transformers library installed (`pip install transformers`).
- Familiarity with text summarization concepts.

## Usage

1. Install the necessary Python package:

   ```bash
   pip install transformers
   ```

2. Import the required modules:

   ```python
   from transformers import pipeline
   ```

3. Create a summarization pipeline using the "facebook/bart-large-cnn" model:

   ```python
   summarizer = pipeline("summarization", model="facebook/bart-large-cnn")
   ```

4. Provide the article or text you want to summarize:

   ```python
   ARTICLE = """
   [Your article text goes here]
   """
   ```

5. Use the `summarizer` to generate a summary:

   ```python
   summary = summarizer(ARTICLE, max_length=130, min_length=30, do_sample=False)
   ```

6. The `summary` variable will contain the generated summary. You can access it as follows:

   ```python
   print(summary[0]['summary_text'])
   ```

   Replace `[Your article text goes here]` with the text you want to summarize.

## Output

The code will provide a summary of the input text based on the specified parameters.
