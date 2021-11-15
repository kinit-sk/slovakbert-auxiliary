# SlovakBERT Auxiliary Repository
Auxiliary files for [SlovakBERT](https://github.com/gerulata/slovakbert) release providing additional data related to
the [released paper](https://arxiv.org/abs/2109.15254).

## Sentiment test sets

Section 4.4 in the paper evaluates various models on sentiment analysis task. One of the dataset we use is a
manually annotated dataset of reviews from various domains. `sentiment_reviews` contains the test sets we created.
It contains reviews from 6 domains (accomodation, books, cars, games, mobiles, movies), as well as one test set
with sentences that stress tests the basic linguistic capabilities of the model (e.g. negation). All the samples
are labeled on `-1, 0, 1` scale.