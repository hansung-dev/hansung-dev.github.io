---
layout: post
title: "Tokenization"
date: 2019-12-31
categories: NLP
tags: [NLP]
image:
---

자연어 토크라이징 도구

1. 영어 토크나이징 라이브러리
  * nltk : 단어/문장 단위 토크나이징 함수 구분
  * spacy : 단어/문장 단위 토크나이징 함수 구분
2.한글 토크나이징 라이브러리
  * KoNLPY : 형태소 / 구문 분석 단위

## KoNLPY
1. 형태소 단위 토크나이징
2. 형태소 분석 및 품사 태깅

### KoNLPY > OKT()
* okt.morphs() : norm / stem option
* okt.nouns()
* okt.phrases()
* okt.pos() : join option


### KoNLPY data
* kolaw : 한국 법률 말뭉치
* kobill : 대한민국 국회 의안 말뭉치
