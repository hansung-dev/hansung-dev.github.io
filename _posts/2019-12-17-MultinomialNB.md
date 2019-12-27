---
layout: post
title: "MultinomialNB : Naive Bayes classifier for multinomial models"
date: 2019-12-27
categories: NLP
tags: [sklearn]
image:
---

Naive Bayes classifier for multinomial models

The multinomial Naive Bayes classifier is suitable for classification with discrete features (e.g., word counts for text classification). The multinomial distribution normally requires integer feature counts. However, in practice, fractional counts such as tf-idf may also work.

Read more in the User Guide.

MultinomialNB
http://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html

BernoulliNB
https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.BernoulliNB.html

> class sklearn.naive_bayes.MultinomialNB(alpha=1.0, fit_prior=True, class_prior=None)

'''python
>>> import numpy as np
>>> rng = np.random.RandomState(1)
>>> X = rng.randint(5, size=(6, 100))
>>> y = np.array([1, 2, 3, 4, 5, 6])
>>> from sklearn.naive_bayes import MultinomialNB
>>> clf = MultinomialNB()
>>> clf.fit(X, y)
MultinomialNB()
>>> print(clf.predict(X[2:3]))
[3]
'''
