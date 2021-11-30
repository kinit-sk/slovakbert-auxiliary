# SlovakBERT Auxiliary Repository
Auxiliary files for [SlovakBERT](https://github.com/gerulata/slovakbert) release providing additional data related to
the [released paper](https://arxiv.org/abs/2109.15254).

## Released fine-tuned models

We published following fine-tuned models mentioned in the paper:

- [POS tagger](https://huggingface.co/kinit/slovakbert-pos) trained on _Universal Dependencies_ dataset.
- [Semantic textual similarity (STS) model](https://huggingface.co/kinit/slovakbert-sts-stsb) trained on
  machine-translated STSbenchmark. 
- [Sentiment analysis model](https://huggingface.co/kinit/slovakbert-sentiment-twitter) trained on multilingual twitter
  dataset.

## Sentiment test sets

Section 4.4 in the paper evaluates various models on sentiment analysis task. One of the dataset we use is a
manually annotated dataset of reviews from various domains. `sentiment_reviews` contains the test sets we created.
It contains reviews from 6 domains (accomodation, books, cars, games, mobiles, movies), as well as one test set
with sentences that stress tests the basic linguistic capabilities of the model (e.g. negation). All the samples
are labeled on `-1, 0, 1` scale.

## STSbenchmark translations

Section 4.3 in the paper uses [STSbenchmark](http://ixa2.si.ehu.eus/stswiki/index.php/STSbenchmark) for STS evaluation.
We used machine translation to generate Slovak sentences from the original English dataset. Here we publish the
translations we use in the paper. `stsb_translations` contains three files:

- `stsb_en_sentences.txt` - Each line is an English sentence from the original STSb dataset.
- `stsb_sk_sentences_m2m100.txt` - Each line is a Slovak sentence translated using M2M100 machine translation tool. N-th
  line in the English file corresponds to the N-th line here.
- `stsb_sk_sentences_marianmt.txt` - The same as above, but we used MarinaMT machine translation. These translations are
  generally worse than M2M100.
  
For labels, you need to download the original dataset from [their site](http://ixa2.si.ehu.eus/stswiki/index.php/STSbenchmark).