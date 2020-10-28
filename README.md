# COUGH: A Challenge Dataset and Models for COVID-19 FAQ Retrieval 

## Introduction
This repository contains the dataset for paper ["COUGH: A Challenge Dataset and Models for COVID-19 FAQ Retrieval"](https://arxiv.org/abs/2010.12800).

In this work, we present a large challenging dataset, **COUGH**, for COVID-19 FAQ retrieval. Specifically, similar to a standard FAQ dataset, **COUGH** consists of three parts: FAQ Bank, User Query Bank and Annotated Relevance Set. FAQ Bank contains ~16K FAQ items scraped from 55 credible websites (e.g., CDC and WHO). For evaluation, we introduce User Query Bank and Annotated Relevance Set, where the former contains 1201 human-paraphrased queries while the latter contains ~32 human-annotated FAQ items for each query.

Examples from **COUGH** dataset are shown below:
<p align="center">
<img src="COUGH_Examples.png" alt="COUGH Examples" title="COUGH Examples" width="800"/>
</p>

## Dataset
**COUGH** can be freely accessed and downloaded under ```data``` directory of this repo (Delimiter used in following csv files: comma (,))

- ```data/FAQ_Bank.csv``` is the full FAQ Bank containing a total number of 15919 FAQ items.

- ```data/FAQ_Bank_eval.csv``` is the FAQ Bank specifically used for evaluation purpose, containing a total number of 7117 English non-Forum FAQ items.

- ```data/User_Query_Bank.csv``` is the User Query Bank containing a total number of 1236 user queries (including 35 unanswerable user queries). 

- ```data/Annotated_Relevance_Set``` is the Annotated Relevance Set containing a total number of 39760 annotated <User Query, FAQ item> tuples.

*Note that, to replicate results as reported in paper, please use ```data/FAQ_Bank_eval.csv```.*

## Useful Codes
You can refer to this [package](https://pypi.org/project/rank-bm25/) for an easy-to-use BM25 search engine.

You can refer to this [repository](https://github.com/UKPLab/sentence-transformers) for handy SentenceBERT models.

Please counsult our paper at Section 5 (Experiment) for more information about how we set up experiments and deploy baseline models.

## Citation
Please kindly cite our paper if you use the **COUGH** dataset from this repo:
```
@article{zhang2020cough,
      title={COUGH: A Challenge Dataset and Models for COVID-19 FAQ Retrieval}, 
      author={Xinliang (Frederick) Zhang and Heming Sun and Xiang Yue and Emmett Jesrani and Simon Lin and Huan Sun},
      journal={arXiv preprint arXiv:2010.12800},
      year={2020}
}  
```

## Disclaimer
The views, information, or opinions expressed in **COUGH** dataset are solely those of the Websites where FAQ items were scrapped and Annotators who paraphrase the queries and judge the relevance, and do not necessarily represent those of the authors of this paper. The primary purpose of releasing **COUGH** is to aid the development of COVID-19 FAQ retrieval systems.
