# 17th Century American Spanish Notary Dataset

This repository contains a dataset of images from 17th century American Spanish notary documents. The dataset is organized into one directory: `images`. And a JSON file `Labeled Data` which is in JSON formate. The `images`, directory contains the actual images of the documents and the annotations for the images, and the JSON file contians all information related to the images with the contents and classes which is annotated and extracted using the labelImg software.

## Dataset Structure

- `images/`: Contains the scanned images and the xml files of 17th century American Spanish notary documents.
- `Labeled Data`: This JSON file contians all information related to the images with the contents and classes.

## Viewing Annotations

To view the annotations, you can use the labelImg software. Follow these steps to load the dataset and view the annotations:

1. Download and install [LabelImg](https://github.com/HumanSignal/labelImg).
2. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/raopr/SpanishNotaryCollection.git

3.To view the annotations in the LabelImg software, make sure that the scanned images and their corresponding XML files are in the same directory, as organized in the images directory. The annotations will looks like this:


<img width="958" alt="LabelImg" src="https://github.com/raopr/SpanishNotaryCollection/assets/58792703/a19ab82d-e06e-4844-b965-965f0c85dae0">

