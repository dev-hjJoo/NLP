# QA (Question-Answering)
<img src="https://github.com/dev-hjJoo/NLP/assets/33647482/ef56e9ed-48d4-4456-8ec9-5fa755a5a532" width=60%>

*이미지는 Slideshare에 게시된 LG CNS AI 연구팀(SeungyoungLim님)의 슬라이드를 차용하였으며, 해당 링크는 본 페이지 최하단 6번에 기재되어 있습니다*

* 질의 응답(Question-Answering)이란, 사용자로부터 받은 질문에 대하여 답을 구하는 기술이다.
* 자연어(Natural language)로 질문을 받고 자연어로 답변을 한다.
* 기계 독해 기반의 Question Answering이란, <u>기계의 독해 능력(MRC, Machine Reading Comprehension)</u>을 기반으로 질문에 대한 답을 구하는 것(Question-Answering)을 의미한다.
---
# Tasks
## 🔵 1. MRC (Machine Reading Comprehension)
* 기계가 사람처럼 문서를 읽고 이해할 수 있는 기술이다.
* 기존의 질의응답 시스템과 달리 FAQ 리스트 없이 새로운 질문에도 자유롭게 대답할 수 있다는 장점이 있다.
### Dataset
1. KorQuAD (Korean Question Answering Dataset)
2. **KLUE-MRC**
    * Summary
        * Context와 Context에 대한 질문, 답변, Context 안에서 답변의 위치 등이 포함된 데이터셋이다.
    * Type
        1. Paraphrase
        2. Multi-Sentence
        3. Unanswerable
    * Evaluation metrics
        1. EM (Exact Match)
        2. ROUGE (Character-level ROUGE-W)
### Code
1. KoBERT 기반의 MRC
2. BERT 기반의 MRC




---
# Digression
1. BERT와 같은 인코더 전용 모델은 사실적인 질문(factoid questions)에 대한 답변을 추출하는 데 우수함, 반면 개방형 질문(open-ended questions)는 제대로 처리되지 않는 경향이 있다.


---
# Reference
``` 내용을 공부하면서 참고한 문서를 모두 포함하고 있습니다. ```
1. 질의 응답 (위키백과): https://ko.wikipedia.org/wiki/질의_응답
2. Question Answering (Hugging Face): https://huggingface.co/tasks/question-answering

3. 6.질의 응답(위키독스, Transformers): https://wikidocs.net/166845

4. 복잡한 표도 이해하는 똑똑한 QA 모델 (SAMSUNG SDS): https://www.samsungsds.com/kr/insights/techtoolkit_2021_qa.html

5. LG AI연구원의 MRC 프로젝트, 어디까지 왔나(LG AI연구원): https://www.lgresearch.ai/blog/view/?seq=140

6. KorQuAD introduction (LG CNS/ Slideshare):  https://www.slideshare.net/SeungyoungLim/korquad-introduction