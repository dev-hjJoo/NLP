# Topic Modeling
* 
---
# Algorithms
## LSA (Latent Semantic Analysis, 잠재 의미 분석)
* 정의: Truncated SVD로 차원 축소를 통해 단어의 잠재적 의미를 도출하는 방법이다.
* 배경: BoW, Tf-idf와 같이 단어의 빈도수를 기반으로 등장한 개념은 단어의 의미 정보를 고려하기 어려워 이를 개선하고자 등장하였다.
* 장점: 문서의 유사도 계산 시 좋은 성능을 보인다.
* 단점: 새로운 정보에 대한 업데이트가 어렵다. (이미 계산된 LSA에 새로운 데이터를 추가할 때 처음부터 계산해야 한다.)
* 단점 보완 방향: Word2Vec, 인공신경망 기반 방법론 등 새로운 벡터화 방법 사용
## LDA (Latent Dirichlet Allocation, 잠재 디리클레 할당)


---
# References
`내용을 공부하면서 참고한 문서를 모두 포함하고 있습니다.`
1. [딥 러닝을 이용한 자연어 처리 입문 / 19-01 잠재 의미 분석 (Latent Semantic Analysis)](https://wikidocs.net/24949)