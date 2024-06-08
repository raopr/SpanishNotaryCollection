# Model Usage Guideline
This will walk you through the steps to use the model and tokenizer that we have provided.

## Requirements

1. Python 3.x
2. Pytorch
3. Pytorch Lightning
4. Transformes Library from Hugging Face

## Installation

Install the required libraries using pip:

    pip install torch
    pip install pytorch-lightning
    pip install transformers

## Usage for Masked Language Model 

1. **Download the Model Files**:

   Download the fine-tuned model's weights and tokenizer configuration files. 

2. **Instantiate the Tokenizer and Model**:

   In your Python script or notebook, import the required modules and instantiate the tokenizer and model using the downloaded files:

   ```python
   from transformers import AutoTokenizer, AutoModelForSequenceClassification
   
   # Replace 'path_to_model_directory' with the path where you downloaded the model files.
   tokenizer = AutoTokenizer.from_pretrained('path_to_model_directory')
   model = AutoModelForSequenceClassification.from_pretrained('path_to_model_directory')

2. **Feed Tokenizer Input to the Model**:

    ```python
    with torch.no_grad():
        outputs = model(**tokenizer_input)

## Usage for Classification Model 

1. **Instantiate the Lightning Module**:

   In your python script or notebook, import required modules and define a Lightning Module for the fine-tuned model:


   ```python
   import torch
   import pytorch_lightning as pl
   from transformers import AutoModelForSequenceClassification

   class YourModel(pl.LightningModule):
    def __init__(self):
      super().__init__()
      self.model = AutoModelForSequenceClassification.from_pretrained('path_to_model_directory')

    def forward(self, input_data):
        return self.model(input_data)


2. **Run Inference**:

    Create an instance of the Lightning Module abd feed the input data to it to inference:
   
    ```python
    input_data = ...  # Your input data
    model = YourModel.load_from_checkpoint('path_to_checkpoint')
    output = model(input_data)

    print(output)

