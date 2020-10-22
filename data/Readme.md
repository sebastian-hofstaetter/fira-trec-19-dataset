# FiRA Data

We provide the following annotation data:

- **fira-trec19-raw-judgements.tsv** The full judgement file with individual annotator results 

- **fira-trec19-qrels-snippets.txt** QRELs per snippet, labels aggregated via majority voting

- **fira-trec19-notrec-qrels-docs-max.txt** QRELs of only the FiRA anotated documents, per document (max of snippet labels), labels aggregated via majority voting
- **fira-trec19-notrec-qrels-docs-sum.txt** QRELs of only the FiRA anotated documents, per document (sum of snippet labels), labels aggregated via majority voting

- **fira-trec19-qrels-docs-max.txt** QRELs of FiRA anotated documents + TREC-DL'19 qrels of the rest , FiRA per document (max of snippet labels), labels aggregated via majority voting
- **fira-trec19-qrels-docs-sum.txt** QRELs of FiRA anotated documents + TREC-DL'19 qrels of the rest, FiRA per document (sum of snippet labels), labels aggregated via majority voting

The qrels have been created from the raw judgements with the script: scripts/generate_qrels.py

The initial input data including the text for queries and document snippets is loacted in the input folder