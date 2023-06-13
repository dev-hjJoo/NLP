# Dictionary
* 학습하면서 몰랐던 용어들을 정리해두자.
---
## Terms
### 1. DTM (Document-Term Matrix, 문서 단어 행렬)
* 서로 다른 문서들에서 도출된 BoW(Bag of Words)

### 2. BoW (Bag of Words)
* 정의: 한국어로 하면 단어 집합으로, 단어 출현 빈도수(frequency) 기반의 단어 표현 방법이다. 
* 특징: 집합의 순서를 고려하지 않는 성질 그대로 단어의 등장 순서를 고려하지 않는다. 

### 3. Matrix
* SVD 등 행렬 연산에서 사용되는 용어들이다.
1. 직교 행렬(Orthogonal matrix): 자신과 전치 행렬의 곱(반대도 성립)의 결과가 단위 행렬이되는 행렬로, 직교 행렬의 역행렬은 전치행렬임.
2. 전치 행렬(Transpose matrix): 원래의 행렬에서 행과 열을 변환한 행렬
3. 단위 행렬(Identify matrix): 주대각선의 원소가 모두 1이며 원소는 모두 0인 **정사각** 행렬
4. 대각 행렬(Diagonal matrix): 주대각선을 제외한 곳의 원소가 모두 0인 행렬 (정사각 행렬이 아닐 수도 있음)


### References
1. [딥 러닝을 이용한 자연어 처리 입문 / 04-03 문서 단어 행렬(Document-Term Matrix, DTM)](https://wikidocs.net/24559)
2. [딥 러닝을 이용한 자연어 처리 입문 / 04-02 Bag of Words(BoW)](https://wikidocs.net/22650)


---
## Evaluation Metrics
### 1. EM (Exact Match)
* QA 분야에서 가장 일반적으로 사용하는 평가 척도이다.
* 정답과 예측된 답변, 두 문자열이 얼마나 같은지를 평가한다.
### 2. ROUGE
* 모델이 정확하게 예측하지 못하더라도 부분 점수를 부여한다.
* LCCS(Longest Common Continuous Subsequence) 기반의 F1 score를 계산하여 평가한다.
* 의미는 같지만 변형에 의하여 다른 답변이 도출되는 경우(예: TV, Television)를 반영하여 평가할 수 있다.
### 3. Character-level F1 score
* 순서와 관계없이 문자 중첩을 측정하는 방법이다.
* 한국어 MRC Dataset에서 주된 척도로 사용하기에는 무리가 있는 것으로 판단된다.
    * 예: '한국의 위인들'과 '국한된 범위' 라는 단어를 볼 때, 낮은 점수로 평가되어야 하지만, {'한', '국', '위'}가 겹치는 것으로 판단되어 54.55점으로 평가한다. (ROUGE의 경우 15.38점)
### References
1. [KLUE-MRC - 기계 독해](https://klue-benchmark.com/tasks/72/overview/evaluation)

---
## Dataset
### 1. KorQuAD(Korean Question Answering Dataset) 2.0 
* Summary
    * SQuAD와 유사하며, 한글 Wikipedia 문서들을 크라우드소싱하여 만든 데이터 세트
    * KorQuAD 2.0의 경우, 데이터셋이 KorQuAD 1.0과 달리 Table 구조로 구성되어 아래의 장점을 가지고 있다.
        1. 여러 문장(혹은 문단)을 종합적으로 활용하여 에서 답을 도출할 수 있다.
        2. 테이블 형태로 문서를 구조화하기 때문에, 행과 열간의 관계를 추가로 학습할 수 있어 답변을 추론하는 데에 효과적이다.
* Reference Links
    * [Slideshare/ KorQuAD v2.0 소개](https://www.slideshare.net/LGCNSairesearch/korquad-v20?ref=https://www.slideshare.net/LGCNSairesearch/slideshelf)
    * [Slideshare/ KorQuAD introduction](https://www.slideshare.net/SeungyoungLim/korquad-introduction)
### 2. KLUE (Korean Language Understanding Evaluation)
* Summary
    * 한국어를 위한 NLP 분야에서 8가지 task를 평가하기 위해 생성된 데이터셋
* Tasks - dataset
    * TC (Topic Classification) - ynat
    * STS (Semantic Textual Similarity) - sts
    * NLI (Natural Language Inference) - nli
    * NER (Named Entity Recognition) - ner
    * RE (Relation Extraction) - re
    * DP (Dependency Parsing) - dp
    * MRC (Machine Reading Comprehension) - mrc
    * DST (Dialogue State Tracking) - wos
* Reference Links
    * [KLUE Website](https://klue-benchmark.com/)
    * [Hugging Face - Datasets: klue](https://huggingface.co/datasets/klue)
### 3. KLUE-MRC
* Summary
    * Context와 Context에 대한 질문, 답변, Context 안에서 답변의 위치 등이 포함된 데이터셋이다.
* Question types
    1. Paraphrase
    2. Multi-Sentence
    3. Unanswerable
* Evaluation metrics
    1. EM (Exact Match)
    2. ROUGE (Character-level ROUGE-W)
### 