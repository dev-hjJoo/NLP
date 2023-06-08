# Dictionary
* 학습하면서 몰랐던 용어들을 정리해두자.
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
