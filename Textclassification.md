
# TEXT-CLASSIFICATION

## Colab Notebook

You can view and run the code in this project's Colab notebook by clicking the following link:

- [![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/120nwST4xFwt3Xxj2eoBjQEtcyUY3i1Vd?authuser=1#scrollTo=LZAYq5aktHJR)


## Description

This code is designed for text classification using the Hugging Face Transformers library and the "go_emotions" dataset. It includes the following functionality:

1. Installation of necessary Python packages using pip.
2. Loading the "go_emotions" dataset with a simplified configuration.
3. Extracting information about the dataset, such as available labels.
4. Preparing target labels for classification tasks.
5. Initializing a text classification pipeline using the "SamLowe/roberta-base-go_emotions" model.
6. Performing text classification on a sample input ("i hate you").

## Prerequisites

Before running this code, make sure you have the following prerequisites:

- Python installed (Python 3.6 or higher).
- Pip package manager installed.
- An understanding of text classification and the Hugging Face Transformers library.

## Installation

To install the required Python packages, you can run the following command:

```bash
pip install datasets transformers pandas matplotlib tqdm --upgrade --quiet
```

## Usage

To use this code, follow these steps:

1. Run the code in your Python environment.

2. The code will install the necessary packages and load the "go_emotions" dataset.

3. It will display information about the labels available in the dataset.

4. It prepares target labels for text classification tasks.

5. The code initializes a text classification pipeline using the "SamLowe/roberta-base-go_emotions" model.

6. You can then use the `classifier` to perform text classification on your input text.

   Example:
   ```python
   model_outputs = classifier("Where are you now? ")
   print(model_outputs[0][0]['label'])
   ```

   Replace `"where are you now?"` with your own text for classification.


