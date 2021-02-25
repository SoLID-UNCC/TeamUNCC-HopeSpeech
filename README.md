# TeamUNCC-HopeSpeech
 
 ## Overview
The repository contains our submission for Task  2:    Hope  Speech  Detection  for  Equality,  Diversity  and  Inclusion at  (LT-EDI-2021@EACL2021)[https://sites.google.com/view/lt-edi-2021]. The  goal  of this  task  is  to  predict  the  presence  of  hopespeech,  along  with  the  presence  of  samples that  do  not  belong  to  the  same  language  in the dataset. Our approach  fine-tunes  RoBERTa  for  Hope  Speech  detection in  English  and we fine-tune XLM-RoBERTa for Hope Speech detection in Tamil  and  Malayalam,  two  low  resource  Indic  languages. We  demonstrate  the  perfor-mance  of  our  approach  on  classifying  text into hope-speech, non-hope and not-language.   Our approach ranked 1st in English (F1 = 0.93), 1st in Tamil (F1 = 0.61) and 3rd in Malayalam (F1 = 0.83)

## Setup

Clone the repository using the following command ``git clone https://github.com/SoLID-UNCC/TeamUNCC-HopeSpeech.git``

Next, download the datasets from



## Citations

Please consider citing our paper
####

```
@inproceedings{mahajan2021TeamUNCC,
  title={TeamUNCC@LT-EDI-EACL2021:Hope Speech Detection using Transfer Learning with Transformers},
  author={Mahajan, Khyati and Al-Hossami, Erfan and Shaikh, Samira},
  booktitle={Proceedings of the First Workshop on Language Technology for Equality, Diversity and Inclusion},
  month = April,
  year={2021 (in press)},
  publisher="Association for Computational Linguistics"
}
```


#### Dataset

To cite the dataset use the following:
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
}
```
