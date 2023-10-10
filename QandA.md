
# Question Answering with Hugging Face Transformers

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/16rhSZtvo1Pn1YkSL4iyNSvBtHtVE7y1b?usp=sharing)
Use the above link to access the colab file.


## Description

This code snippet demonstrates how to use the Hugging Face Transformers library to perform question answering. It utilizes the "distilbert-base-cased-distilled-squad" model to extract answers from a given context based on a provided question.

## Prerequisites

Before running this code, make sure you have the following prerequisites:

- Python installed (Python 3.6 or higher).
- The Transformers library installed (`pip install transformers`).
- An understanding of question-answering concepts.

## Usage

1. Install the necessary Python package:

   ```bash
   pip install transformers
   ```

2. Import the required modules:

   ```python
   from transformers import pipeline
   ```

3. Create a question-answering pipeline using the "distilbert-base-cased-distilled-squad" model:

   ```python
   question_answerer = pipeline("question-answering", model='distilbert-base-cased-distilled-squad')
   ```

4. Provide the context and question you want to answer:

   ```python
   context = """
   [Your context text goes here]
   """

   question = "What is your question?"
   ```

   Replace `[Your context text goes here]` with the context text you want to use and specify your question.

5. Use the `question_answerer` to extract the answer:

   ```python
   result = question_answerer(question=question, context=context)
   ```

6. The `result` variable will contain the extracted answer and start/end positions of the answer in the context.

   ```python
   print(f"Answer: '{result['answer']}', start: {result['start']}, end: {result['end']}")
   ```

   The "start" and "end" positions represent where the answer begins and ends in the original context.

## Output

The code will provide the extracted answer to the provided question, along with the start and end positions of the answer in the context.
