---
layout: post
title: "Count based word Representation"
date: 2019-12-26
categories: NLP
tags: [Bow, TF-IDF]
image:
---

## 1. Bag of Words(BoW)
  - DictVectorizer : 각 단어의 수를 세어놓은 사전에서 BOW 벡터를 만든다.
  - CountVectorizer : 문서 집합에서 단어 토큰을 생성하고 각 단어의 수를 세어 BOW 인코딩한 벡터를 만든다.
    1. 문서를 토큰 리스트로 변환한다.
    2. 각 문서에서 토큰의 출현 빈도를 센다.
    3. 각 문서를 BOW 인코딩 벡터로 변환한다.
  - HashingVectorizer : 해시 함수(hash function)을 사용하여 적은 메모리와 빠른 속도로 BOW 벡터를 만든다.
## 2. TF-IDF(Term Frequency – Inverse Document Frequency)
  - TfidfVectorizer : CountVectorizer와 비슷하지만 TF-IDF 방식으로 단어의 가중치를 조정한 BOW 벡터를 만든다.

## CountVectorizer
***
* stop_words : 문자열 {‘english’}, 리스트 또는 None (디폴트)
  * stop words 목록.‘english’이면 영어용 스탑 워드 사용.
* analyzer : 문자열 {‘word’, ‘char’, ‘char_wb’} 또는 함수
  * 단어 n-그램, 문자 n-그램, 단어 내의 문자 n-그램
* token_pattern : string
  * 토큰 정의용 정규 표현식
* tokenizer : 함수 또는 None (디폴트)
  * 토큰 생성 함수 .
* ngram_range : (min_n, max_n) 튜플
  * n-그램 범위
* max_df : 정수 또는 [0.0, 1.0] 사이의 실수. 디폴트 1
  * 단어장에 포함되기 위한 최대 빈도
* min_df : 정수 또는 [0.0, 1.0] 사이의 실수. 디폴트 1
  * 단어장에 포함되기 위한 최소 빈도

## 참고
***
1. Bow (Bag of Words)
  - https://www.kaggle.com/c/word2vec-nlp-tutorial/overview/part-1-for-beginners-bag-of-words
  - https://github.com/corazzon/KaggleStruggle/blob/master/word2vec-nlp-tutorial/tutorial-part-1.ipynb
  - https://www.youtube.com/watch?v=5D9742ID4XI&list=PLaTc2c6yEwmo4hpZKEGi05UFN0tpwHVG1&index=10

2. TF-IDF(Term Frequency-Inverse Document Frequency)
  - https://www.kaggle.com/c/word2vec-nlp-tutorial/overview/part-2-word-vectors
  - https://wikidocs.net/31698

## 참고 캐글 대회
***
- Bag of Words Meets Bags of Popcorn : https://www.kaggle.com/c/word2vec-nlp-tutorial
