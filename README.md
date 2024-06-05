# SANR (17th Century American Spanish Notary Dataset)

Large language models have gained tremendous popularity in domains such as ecommerce, finance, healthcare, and education. Finetuning is a common approach to customize an LLM on a domainspecific dataset for a desired downstream task. In this paper, we
present a valuable resource for fine-tuning LLMs developed for the Spanish language to perform a variety of tasks such as classification, masked language modeling, clustering, and others. Our resource is a collection of handwritten notary records from the
seventeenth century obtained from the National Archives of Argentina. This collection contains a combination of original images
and transcribed text (and metadata) of 160+ pages that were handwritten by two notaries, namely, Estenban Agreda de Vergara and
Nicolas de Valdivia y Brisuela nearly 400 years ago. Through empirical evaluation, we demonstrate that our collection can be used to
fine-tune Spanish LLMs for tasks such as classification and masked language modeling. 

# Table of Contents 

1. [Dataset](#dataset)
2. [Model](#model)
3. [Acknowledgements](#acknowledgement)
4. [Contact](#contact)

# Dataset 

SANRlite had 162 pages containing 900+ sentences. Each sentence (or a group of sentences) was assigned one or more class labels and extended class labels. Extended class labels provide fined-grained representation. There are 33 class labels and 154 extended class labels that were assigned to the sentences. To semantically enrich the JSON metadata, for each class label, we searched Wikidata [31], a popular free and open knowledge base, to extract the uniform resource identifier (URI) for the class labels to precisely denote their meaning. The JSON metadata also includes the notary name, the year when the notary record was written, and the Rollo/image number. To download the dataset and utilize it, please follow the guideline given in [dataset_readme.md](dataset/dataset-README.md)

# Model
 We used SANR to do two down-stream task of language models using bert base language model. One is sentence classification and another is masked language model. We used bert base pretrained model to perform these tasks. For classification task, we used Multilingual BERT model, which is trained on text from multiple language along with Spanish. For MLM task, we used BETO: Spanish bert model, which is specifically trained on Spanish text. 

## Download

|              |                  Model                   |                  Tokenizer                  |
|:------------:|:--------------------------------------------------------------:|
| SANR Classification Model | [Model](https://mailmissouri-my.sharepoint.com/:f:/g/personal/sscx3_umsystem_edu/Em6J8fzd4KxLtVMo4YtoPywBn8OcPcG4NW1upggdcIJ5Cw?e=Gkud58) | [Tokenizer](https://mailmissouri-my.sharepoint.com/:f:/g/personal/sscx3_umsystem_edu/EkFVNqwHpDVOuFYT3hrxEEgBsG7ItzPm2NiMlbF5C1TxEQ?e=TZgkUC) |
| SANR Masked Language Model | [Model](https://mailmissouri-my.sharepoint.com/:f:/g/personal/sscx3_umsystem_edu/El2jWbHfDs1Jtb0-bLA4BGgBCbBL_xAJ4ro65JCsCsILPg?e=j1efVP)  | [Tokenizer](https://mailmissouri-my.sharepoint.com/:f:/g/personal/sscx3_umsystem_edu/EhVwk6WAcudGsvaATfGAakEB3ccN6K4DMjl8e6Mew1zBSg?e=lYlCtY) |

If you wish to download and use the model and tokenizer, please follow the steps mentioned in the [model_readme.md](model/model-README.md).


# Acknowlegdement
This work was supported by the National Endowments for the Humanities Grant No. HAA-287903-22.

