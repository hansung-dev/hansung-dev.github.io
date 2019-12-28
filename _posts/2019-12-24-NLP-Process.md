---
layout: post
title: "NLP Process"
date: 2019-12-24
categories: NLP
tags: [NLP]
image:
---

1. 말뭉치
2. 한국어 전처리
    * 순수 텍스트 파일 변환 : 토큰 생성 (tokenizing), ...
    * 형태소 분석 : 어간 추출(stemming), 원형 복원(lemmatizing), 품사 부착(Part-Of-Speech tagging)
3. 카운트 기반 단어표현 - Bow, N-Gram
4. 임베딩
    * 단어 수준 임베딩 - NPLM, Word2Vec, FastText, 잠재 의미 분석, GloVe, Swivel
    * 문장 수준 임베딩 - 잠재 의미 분석, Doc2Vec, 잠재 디리클레 할당, ELMo, 트랜스포머 네트워크, BERT
5. 임베딩 파인 튜닝


## 1. 말뭉치 (corpus)
* * *
1. 한국어 위키백과
2. KorQuAD (한국어 기계 독해 - LG CNS)
3. 네이버 영화 리뷰 말뭉치
4. NLTK - corpus 서브패키지
5. KoNLPy- 헌법 말뭉치인 kolaw와 국회법안 말뭉치인 kobill

## 2. 한국어 전처리
* * *
### 1. 순수 텍스트 파일로 변환
1. 토큰화(Tokenization)
    1. 단어 토큰화(Word Tokenization)
    2. 문장 토큰화(Sentence Tokenization)
2. 정제(Cleaning)
3. 정규화(Normalization)
4. 어간 추출(Stemming)
5. 표제어 추출(Lemmatization)
6. 불용어(Stopword)
7. 정규 표현식(Regular Expression)
8. ~~정수 인코딩(Integer Encoding)~~
9. ~~원-핫 인코딩(One-hot encoding)~~
10. 단어 분리(Subword Segmentation)
11. 데이터의 분리(Splitting Data)

### 2. 형태소 분석 방법
1. 지도학습
     1. KoNLPy (오픈소스 형태기 분석기, 은전한닙/꼬꼬마/한나눔/OKT)
     2. Khaiii (카카오 오픈소스 한국어 형태소 분석기, 2018/12/13)
2. 비지도 학습
     1. soynlp (파이썬 기반 한국어 자연어 처리 패키지)
     2. 구글 센텐스피스 (BPE 기본원리)

- KoNLPy
***
  - Hannanum: 한나눔. KAIST Semantic Web Research Center 개발. http://semanticweb.kaist.ac.kr/hannanum/
  - Kkma: 꼬꼬마. 서울대학교 IDS(Intelligent Data Systems) 연구실 개발. http://kkma.snu.ac.kr/
  - Komoran: 코모란. Shineware에서 개발. https://github.com/shin285/KOMORAN
  - Mecab: 메카브. 일본어용 형태소 분석기를 한국어를 사용할 수 있도록 수정. https://bitbucket.org/eunjeon/mecab-ko
  - Open Korean Text: 오픈 소스 한국어 분석기. 과거 트위터 형태소 분석기. https://github.com/open-korean-text/open-korean-text

## 3. 카운트 기반의 단어 표현(Count based word Representation)
***
1. Bag of Words(BoW)
  - DictVectorizer : 각 단어의 수를 세어놓은 사전에서 BOW 벡터를 만든다.
  - CountVectorizer : 문서 집합에서 단어 토큰을 생성하고 각 단어의 수를 세어 BOW 인코딩한 벡터를 만든다.
    1. 문서를 토큰 리스트로 변환한다.
    2. 각 문서에서 토큰의 출현 빈도를 센다.
    3. 각 문서를 BOW 인코딩 벡터로 변환한다.
  - HashingVectorizer : 해시 함수(hash function)을 사용하여 적은 메모리와 빠른 속도로 BOW 벡터를 만든다.
2. TF-IDF(Term Frequency – Inverse Document Frequency)
  - TfidfVectorizer : CountVectorizer와 비슷하지만 TF-IDF 방식으로 단어의 가중치를 조정한 BOW 벡터를 만든다.

## 4. 임베딩
***
### 1. 단어 수준 임베딩
1. NPLM
2. *Word2Vec*
3. *FastText*
4. 잠재 의미 분석
5. *GloVe*
6. *Swivel*

### 2. 문장 수준 임베딩
1. 잠재 의미 분석
2. Doc2Vec
3. 잠재 디리클레 할당
4. *ELMo*
5. 트랜스포머 네트워크
6. BERT, KoBERT

## 5. 임베딩 파인 튜닝
***
1. 내용입력


## 참고.
***
- NLTK 자연어 처리 패키지 : https://datascienceschool.net/view-notebook/8895b16a141749a9bb381007d52721c1/
- KoNLPy 한국어 처리 패키지 : https://datascienceschool.net/view-notebook/a0237ff8f13a454c96072f868c01bc30/
- Scikit-Learn의 문서 전처리 기능 : https://datascienceschool.net/view-notebook/3e7aadbf88ed4f0d87a76f9ddc925d69/
