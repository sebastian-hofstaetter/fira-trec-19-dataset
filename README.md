# FiRA: Fine-grained Relevance Annotations for TREC-DL'19

*Fine-Grained Relevance Annotations for Multi-Task Document Ranking and Question Answering*
Sebastian Hofstätter, Markus Zlabinger, Mete Sertkan, Michael Schröder and Allan Hanbury. CIKM 2020 (Resource Track)

https://arxiv.org/abs/2008.05363

**tl;dr** We present FiRA: a novel dataset of Fine-Grained Relevance Annotations 🔍. We extend the ranked retrieval annotations of the [Deep Learning Document Track of TREC 2019](https://github.com/microsoft/TREC-2019-Deep-Learning) with passage and word level graded relevance annotations for all relevant documents.
 
We split the documents into snippets and displayed query \& document snippet pairs to annotators. In the following Figure, we show an example of an annotated document-snippet. We ensure a high quality by employing at least 3-way majority voting for every candidate and continuous monitoring of quality parameters during our annotation campaign, such as the time spent per annotation. Furthermore, by requiring annotators to select relevant text spans, we reduce the probability of false-positive retrieval relevance labels.

![](figures/single-page-screenshot.png)


Furthermore, we selected 10 pairs to be annotated by all our annotators, so that we can study their subjectivity with a dense distribution, as shown in the following Figure: 

![](figures/full-judge-example-text.png)
*Comparison of two completely judged document snippets. The background heatmap for each word displays the number of times this word was part of a relevant region selection. The darker the green the more often annotators selected this word as being relevant.*

With FiRA annotations we can observe a distribution of relevance inside long documents. The following Figure shows, the bias towards earlier regions of the documents, however our results also highlight a significant amount of relevant snippets can be found later in the documents.

![](figures/in-document-pos-bias.png)


**Please cite us as:**
````
@inproceedings{Hofstaetter2020_fira,
 author = {Hofst{\"a}tter, Sebastian and Zlabinger, Markus and Sertkan, Mete and Schr{\"o}der, Michael and Hanbury, Allan},
 title = {Fine-Grained Relevance Annotations for Multi-Task Document Ranking and Question Answering},
 booktitle = {Proc. of CIKM},
 year = {2020},
}
````

## Usage Scenarios

The FiRA-TREC'19 dataset can be utilized for every approach concerned with long document ranking and the selection of snippets or answers from these documents.

As an example we used it to better understand and evaluate our [TKL document ranking model](https://github.com/sebastian-hofstaetter/transformer-kernel-ranking).

## Dataset

The FiRA dataset contains **24,199** query \& document-snippet pairs of all **1,990** relevant documents for the **43** queries of TREC-DL. 

The dataset folder contains:
 - Our processed document-snippets and annotation task list
 - Raw (anonymized) annotations
 - Majority voted judgements for document-snippet and document levels


## Acknowledgements

We want to thank our students of the Advanced Information Retrieval course in the summer term of 2020 for annotating the data and being so patient and motivated in the process. 
