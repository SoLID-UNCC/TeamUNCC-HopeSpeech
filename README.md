 [![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/teamuncc-lt-edi-eacl2021-hope-speech/hope-speech-detection-for-english-on-hopeedi)](https://paperswithcode.com/sota/hope-speech-detection-for-english-on-hopeedi?p=teamuncc-lt-edi-eacl2021-hope-speech) [![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/teamuncc-lt-edi-eacl2021-hope-speech/hope-speech-detection-for-tamil-on-hopeedi)](https://paperswithcode.com/sota/hope-speech-detection-for-tamil-on-hopeedi?p=teamuncc-lt-edi-eacl2021-hope-speech) [![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/teamuncc-lt-edi-eacl2021-hope-speech/hope-speech-detection-for-malayalam-on)](https://paperswithcode.com/sota/hope-speech-detection-for-malayalam-on?p=teamuncc-lt-edi-eacl2021-hope-speech)
 
# TeamUNCC-HopeSpeech

 ## Overview
The repository contains our submission for Task  2:    Hope  Speech  Detection  for  Equality,  Diversity  and  Inclusion at  [LT-EDI-2021@EACL2021](https://sites.google.com/view/lt-edi-2021). The  goal  of this  task  is  to  predict  the  presence  of  hopespeech,  along  with  the  presence  of  samples that  do  not  belong  to  the  same  language  in the dataset. Our approach  fine-tunes  RoBERTa  for  Hope  Speech  detection in  English  and we fine-tune XLM-RoBERTa for Hope Speech detection in Tamil  and  Malayalam,  two  low  resource  Indic  languages. We  demonstrate  the  perfor-mance  of  our  approach  on  classifying  text into hope-speech, non-hope and not-language.  Amongst around 31 teams, our approach ranked 1st in English (F1 = 0.93), 1st in Tamil (F1 = 0.61) and 3rd in Malayalam (F1 = 0.83).

**UPDATE:** Our paper is published in LT-EDI-2021@EACL2021! You can view our paper here: [https://www.aclweb.org/anthology/2021.ltedi-1.20.pdf](https://www.aclweb.org/anthology/2021.ltedi-1.20.pdf)

## Setup Instructions

Clone the repository using the following command ``git clone https://github.com/SoLID-UNCC/TeamUNCC-HopeSpeech.git``

Next, download the following datasets from the organizers [website](https://competitions.codalab.org/competitions/27653#participate-get-data):
 - English Train Data
 - English Dev Data
 - English Test Data
 - Malayalam Train Data
 - Malayalam Dev Data
 - Malayalam Test Data
 - Tamil Train Data
 - Tamil Dev Data
 - Tamil Test Data


To replicate the results from scratch, run the Jupyter notebook ``TeamUNCC_Hopespeech_Detection.ipynb`` and it should install the dependencies for you. Follow the prompt for user inputs to select the dataset and whether to include class weights or not. 

We also provide our fine-tuned weights for our experiments here: [https://drive.google.com/drive/folders/1LzOjFLfrxe8u2VujUy8NptCf-MHQMCb6?usp=sharing](https://drive.google.com/drive/folders/1LzOjFLfrxe8u2VujUy8NptCf-MHQMCb6?usp=sharing). Create a folder called `outputs`  in the repo home directory. Next, download and extract the folders into the outputs folder you created.  Run the cells in the Jupyter notebook starting from the *Test Set Predictions* section in the notebook. Change the variable `lang` in the cell below to the downloaded folder name of choice. The folders include all of our experiments reported in the paper including:
 - English with class weights
 - English with out class weights
 - Malayalam with class weights
 - Malayalam without class weights
 - Tamil with class weights
 - Tamil without class weights


To run our analytical approach, please run the ``Qualitative evaluation - UMAP clustering with sentence embeddings.ipynb`` Jupyter notebook.






## Citations

Please consider citing our paper:
####

```
@inproceedings{mahajan-etal-2021-teamuncc,
    title = "{T}eam{UNCC}@{LT}-{EDI}-{EACL}2021: Hope Speech Detection using Transfer Learning with Transformers",
    author = "Mahajan, Khyati  and
      Al-Hossami, Erfan  and
      Shaikh, Samira",
    booktitle = "Proceedings of the First Workshop on Language Technology for Equality, Diversity and Inclusion",
    month = apr,
    year = "2021",
    address = "Kyiv",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2021.ltedi-1.20",
    pages = "136--142",
    abstract = "In this paper, we describe our approach towards utilizing pre-trained models for the task of hope speech detection. We participated in Task 2: Hope Speech Detection for Equality, Diversity and Inclusion at LT-EDI-2021 @ EACL2021. The goal of this task is to predict the presence of hope speech, along with the presence of samples that do not belong to the same language in the dataset. We describe our approach to fine-tuning RoBERTa for Hope Speech detection in English and our approach to fine-tuning XLM-RoBERTa for Hope Speech detection in Tamil and Malayalam, two low resource Indic languages. We demonstrate the performance of our approach on classifying text into hope-speech, non-hope and not-language. Our approach ranked 1st in English (F1 = 0.93), 1st in Tamil (F1 = 0.61) and 3rd in Malayalam (F1 = 0.83).",
}
```


### Dataset

To cite the dataset use the following:

```
@inproceedings{chakravarthi-2020-hopeedi,
title = "{H}ope{EDI}: A Multilingual Hope Speech Detection Dataset for Equality, Diversity, and Inclusion",
author = "Chakravarthi, Bharathi Raja",
booktitle = "Proceedings of the Third Workshop on Computational Modeling of People's Opinions, Personality, and Emotion's in Social Media",
month = dec,
year = "2020",
address = "Barcelona, Spain (Online)",
publisher = "Association for Computational Linguistics",
url = "https://www.aclweb.org/anthology/2020.peoples-1.5",
pages = "41--53",
abstract = "Over the past few years, systems have been developed to control online content and eliminate abusive, offensive or hate speech content. However, people in power sometimes misuse this form of censorship to obstruct the democratic right of freedom of speech. Therefore, it is imperative that research should take a positive reinforcement approach towards online content that is encouraging, positive and supportive contents. Until now, most studies have focused on solving this problem of negativity in the English language, though the problem is much more than just harmful content. Furthermore, it is multilingual as well. Thus, we have constructed a Hope Speech dataset for Equality, Diversity and Inclusion (HopeEDI) containing user-generated comments from the social media platform YouTube with 28,451, 20,198 and 10,705 comments in English, Tamil and Malayalam, respectively, manually labelled as containing hope speech or not. To our knowledge, this is the first research of its kind to annotate hope speech for equality, diversity and inclusion in a multilingual setting. We determined that the inter-annotator agreement of our dataset using Krippendorff{'}s alpha. Further, we created several baselines to benchmark the resulting dataset and the results have been expressed using precision, recall and F1-score. The dataset is publicly available for the research community. We hope that this resource will spur further research on encouraging inclusive and responsive speech that reinforces positiveness.",
}
```

```
@inproceedings{dravidianhopespeech-eacl,
title={Findings of the Shared Task on {H}ope {S}peech {D}etection for {E}quality, {D}iversity, and {I}nclusion},
author={Chakravarthi, Bharathi Raja and
Muralidaran, Vigneshwaran},
booktitle = "Proceedings of the First Workshop on Language Technology for Equality, Diversity and Inclusion",
month = April,
year = "2021",
publisher = "Association for Computational Linguistics",
year={2021}
```

## Contact

If you have any questions please contact kmahaja2@uncc.edu or ealhossa@uncc.edu!
