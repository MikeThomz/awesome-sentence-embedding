# awesome-sentence-embedding
A curated list of awesome sentence embedding models

## Table of Contents


* **[General Framework](#general-framework)**
* **[Word Embeddings](#word-embeddings)**
* **[OOV Handling](#oov-handling)**
* **[Contextualized Word Embeddings](#contextualized-word-embeddings)**
* **[Pooling Methods](#pooling-methods)**
* **[Encoders](#encoders)**
* **[Surveys](#surveys)**
* **[Evaluation](#evaluation)**
* **[Multilingual Word Embeddings](#multilingual-word-embeddings)**
* **[Articles](#articles)**

## General Framework

* Almost all the sentence embeddings work like this: given some sort of word embeddings and an optional encoder (for example an LSTM) they obtain the contextualized word embeddings and then they define some sort of pooling (it can be as simple as last pooling) and then based on that they either use it directly for the supervised classification task (like infersent) or generate the target sequence (like skip-thought) so in general we have many sentence embeddings that you have never heard of, you can simply do mean-pooling over any word embedding and it's a sentence embedding!

## Word Embeddings

|paper|code|pretrained models|
|---|---|---|
|[GloVe: Global Vectors for Word Representation](https://nlp.stanford.edu/pubs/glove.pdf)|[C++](https://github.com/stanfordnlp/GloVe)(official)|[GloVe](https://nlp.stanford.edu/projects/glove/)|
|[Efficient Estimation of Word Representations in Vector Space](http://arxiv.org/pdf/1301.3781.pdf)|[C++](https://code.google.com/archive/p/word2vec/)(official)|[Word2Vec](https://code.google.com/archive/p/word2vec/)|
|[Enriching Word Vectors with Subword Information](https://arxiv.org/abs/1607.04606)|[C++](https://github.com/facebookresearch/fastText)(official)|[fastText](https://fasttext.cc/docs/en/english-vectors.html)|
|[BPEmb: Tokenization-free Pre-trained Subword Embeddings in 275 Languages](https://arxiv.org/pdf/1710.02187.pdf)|[Python](https://github.com/bheinzerling/bpemb)(official)|[bpemb](https://github.com/bheinzerling/bpemb#downloads-for-each-language)|
|[ConceptNet 5.5: An Open Multilingual Graph of General Knowledge](https://arxiv.org/pdf/1612.03975.pdf)|[Python](https://github.com/commonsense/conceptnet-numberbatch)(official)|[Numberbatch](https://github.com/commonsense/conceptnet-numberbatch#downloads)|
|[A Joint Many-Task Model: Growing a Neural Network for Multiple NLP Tasks](https://arxiv.org/pdf/1611.01587.pdf)|<ul><li>[C++](https://github.com/hassyGo/charNgram2vec)(Official)</li><li>[Pytorch](https://github.com/hassyGo/pytorch-playground/tree/master/jmt)</li></ul>|[charNgram2vec](http://www.logos.t.u-tokyo.ac.jp/~hassy/publications/arxiv2016jmt/jmt_pre-trained_embeddings.tar.gz)|
|[Matrix Factorization using Window Sampling and Negative Sampling for Improved Word Representations](http://anthology.aclweb.org/P16-2068)|[GO](https://github.com/alexandres/lexvec)(official)|[lexvec](https://github.com/alexandres/lexvec#pre-trained-vectors)|
|[Hash Embeddings for Efficient Word Representations](https://arxiv.org/pdf/1709.03933.pdf)|<ul><li>[Keras](https://github.com/dsv77/hashembedding)(official)</li><li>[Pytorch](https://github.com/YannDubs/Hash-Embeddings)</li></ul>|-|
|[Dependency-Based Word Embeddings](http://www.aclweb.org/anthology/P14-2050)|<ul><li>[C++](https://bitbucket.org/yoavgo/word2vecf/src/default/)(official)</li><li>[DL4J](https://github.com/IsaacChanghau/Word2VecfJava)</li></ul>|[word2vecf](https://levyomer.wordpress.com/2014/04/25/dependency-based-word-embeddings/)|
|[Learning Word Meta-Embeddings](http://www.aclweb.org/anthology/P16-1128)|-|[Meta-Emb](http://cistern.cis.lmu.de/meta-emb/)(broken)|
|[Dict2vec : Learning Word Embeddings using Lexical Dictionaries](http://aclweb.org/anthology/D17-1024)|[C++](https://github.com/tca19/dict2vec)(official)|[Dict2vec](https://github.com/tca19/dict2vec#download-pre-trained-vectors)|
|[Semantic Specialisation of Distributional Word Vector Spaces using Monolingual and Cross-Lingual Constraints](https://arxiv.org/pdf/1706.00374)|[TF](https://github.com/nmrksic/attract-repel)(official)|[Attract-Repel](https://github.com/nmrksic/attract-repel#available-word-vector-spaces)(bilingual)|
|[Siamese CBOW: Optimizing Word Embeddings for Sentence Representations](https://arxiv.org/pdf/1606.04640)|<ul><li>[Theano](https://bitbucket.org/TomKenter/siamese-cbow/src/master/)(official)</li><li>[TF](https://github.com/raphael-sch/SiameseCBOW)</li></ul>|[Siamese CBOW](https://bitbucket.org/TomKenter/siamese-cbow/src/master/)|
|[Offline bilingual word vectors, orthogonal transformations and the inverted softmax](https://arxiv.org/pdf/1702.03859)|[Python](https://github.com/Babylonpartners/fastText_multilingual)(official)|-|

## OOV Handling
* Drop OOV words!
* One OOV vector(unk vector)
* [A La Carte Embedding: Cheap but Effective Induction of Semantic Feature Vectors](http://aclweb.org/anthology/P18-1002): [ALaCarte](github.com/NLPrinceton/ALaCarte)
* [Mimicking Word Embeddings using Subword RNNs](http://www.aclweb.org/anthology/D17-1010): [Mimick](https://github.com/yuvalpinter/Mimick)
