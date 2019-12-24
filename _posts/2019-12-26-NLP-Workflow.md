---
category: NLP
path: '/stuff/:id'
title: 'NLP Process'
type: 'NLP'

layout: nil
---
# NLP Process

## 1. 말뭉치 (corpus)
    1. 한국어 위키백과
    2. KorQuAD (한국어 기계 독해 - LG CNS)
    3. 네이버 영화 리뷰 말뭉치
## 2. 한국어 전처리
    1. 순수 텍스트 파일로 변환
        * 토큰화(Tokenization)
            * 단어 토큰화(Word Tokenization)
            * 문장 토큰화(Sentence Tokenization)
        * 정제(Cleaning), 정규화(Normalization)
        * 어간 추출(Stemming), 표제어 추출(Lemmatization)
        * 불용어(Stopword)
        * 정규 표현식(Regular Expression)
        * ~~정수 인코딩(Integer Encoding)~~
        * ~~원-핫 인코딩(One-hot encoding)~~
        * 단어 분리(Subword Segmentation)
        * 데이터의 분리(Splitting Data)
    2. 형태소 분석 방법
        1. 지도학습
             1. 형태소 분석기
                1. KoNLPy (오픈소스 형태기 분석기)
                    * 은전한닙
                    * 꼬꼬마
                    * 한나눔
                    * Okt (트위터)
                2. Khaiii (카카오 오픈소스 한국어 형태소 분석기, 2018/12/13)
             2. 사용자 사전 추가하기
        2. 비지도 학습
             1. 형태소 분석기
                1. soynlp (파이썬 기반 한국어 자연어 처리 패키지)
                    * 뛰어쓰기 교정
                2. 구글 센텐스피스 (BPE 기본원리)
## 3. 카운트 기반의 단어 표현(Count based word Representation)
    1. Bag of Words(BoW)
    2. N-gram 언어 모델(N-gram Language Model) 
## 4. 임베딩
    1. 단어 수준 임베딩
        1. NPLM
        2. *Word2Vec*
        3. *FastText*
        4. 잠재 의미 분석
        5. *GloVe*
        6. *Swivel*
    2. 문장 수준 임베딩
        1. 잠재 의미 분석
        2. Doc2Vec
        3. 잠재 디리클레 할당
        4. *ELMo*
        5. 트랜스포머 네트워크
        6. BERT
## 5. 임베딩 파인 튜닝

