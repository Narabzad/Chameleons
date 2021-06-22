# Baseline Rankers Configuration 

**BM25**: For BM25, we used [Anserini implementation of BM25for MS MARCO Passage Ranking](https://github.com/castorini/anserini/blob/master/docs/experiments-msmarco-passage.md#anserini-bm25-baselines-for-ms-marco-passage-ranking)


**DocT5Query**:For DocT5Query we used the default DocTTTTTQuery implementation in their [Github.](https://github.com/castorini/docTTTTTquery)

**DeepCT:** To implement DeepCT, we used the [predicted weighted documents](http://boston.lti.cs.cmu.edu/appendices/arXiv2019-DeepCT-Zhuyun-Dai/weighted_documents/sqrt_sample_100_jsonl.zip) in the [original paper](https://arxiv.org/abs/1910.10687). Then, we indexed the predicted weighted documents using [anserini](https://github.com/castorini/anserini/blob/master/docs/experiments-msmarco-passage.md#anserini-bm25-baselines-for-ms-marco-passage-ranking) and we run BM25 with K1 =9 and b =0.9 as per [instructed here](https://github.com/AdeDZY/DeepCT/issues/2). 

**RepBert**: We employed the implementation from [RepBert Github](https://github.com/jingtaozhan/RepBERT-Index)

**ANCE**:  We employed the implementation from [RepBert Github](https://github.com/microsoft/ANCE). Inferencing approximately takes 9 hours on two RTX3090 GPUS with 24GB memmory. 

 **TCT-ColBert** : We utilized [pyserini](https://github.com/castorini/pyserini) implmenetation of tct-colbert to run this baseline. Since we needed to compute the query embeddings on the fly, we preferred to select [Dense retrieval with TCT-ColBERT, brute-force index](https://github.com/castorini/pyserini/blob/master/docs/experiments-tct_colbert.md#dense-retrieval):

