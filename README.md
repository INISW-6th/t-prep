# T-prep

고려대학교 지능정보 SW아카데미 6기 7조 최종 프로젝트
<!--
- 아이디어 경진대회 **우수상**(한국경제신문사장상)
-->
## Project Description

T-prep(Teacher's Preparation)은 초등 및 중등 사회교과 교사들이 역사 수업을 준비하는 데 있어 LLM을 쉽게 활용해 수업 자료를 생성하기 위한 서비스입니다. Modular RAG를 활용해 별도의 프롬프트를 입력하지 않아도 수업을 진행하는 데 필요한 지도자료를 교과서와 지도서 기반으로 생성하고, 추가자료를 사료로부터 가져와 정리해주도록 합니다. 또한, 학생들이 흥미를 가지고 수업에 참여할 수 있는 스토리텔링 콘텐츠를 생성하는 멀티모달 모델 기반의 서비스를 제작해 초등 및 중학생 대상으로 한 교육적 효과를 제고합니다.

### 문제 발견
1. 대부분의 교사가 AI 서비스를 인식하고 있지만, 수업을 위해 사용하고 있지 않음.[1]
2. 맞춤형 수업 콘텐츠 제작을 위해 수많은 프롬프트 입력 요구, 교사들에게 높은 진입장벽.
3. 인공지능을 활용한 수업 준비 시간의 부담, 교수 학습 자료의 부족, 인공지능 융합 수업 설계의 전문성 부족.[2]

### 문제 정의 및 솔루션
1. 교사들이 생성형 AI를 안전하고 쉽게 사용할 수 있도록 사용성을 개선한 수업 준비 보조 시스템.
2. 교과서 및 지도서 기반으로 수업자료 및 지도법 정리, 사료를 이용한 추가자료 생성.
3. 학생들이 몰입할 수 있는 스토리텔링 콘텐츠를 생성하고, 교사가 내용을 검토 및 수정 가능하도록 설정.

## 플로우차트
![](/src/pipeline.png)

## 데이터
[**데이터 수집 및 전처리 과정**](https://github.com/INISW-6th/data-preprocessing)
1. 미래엔 중학교 2학년 역사 교과서(교사용)
2. 미래엔 중학교 2학년 역사 지도서
3. 한국학중앙연구회 한국민족문화대백과사전([링크](https://encykorea.aks.ac.kr/))

## LangChain 구성
[**LangChain 구성 및 최적화**](https://github.com/INISW-6th/langchain-sys)
1. 메타데이터 기반의 데이터를 활용하는 Modular RAG 구성
2. 각 단계에 Prompt Engineering과 Modular RAG 내 Embedding/VectorDB/Reranker/LLM 평가
3. 각 단계에 최적화된 Prompt와 모델 설정

## 설치 가이드
### 라이브러리 버전
- `python 3.11.13`
- `langchain 0.3.25`
- `langchain-community 0.3.25`
- `langchain-huggingface 0.3.0`
- `sentence-transformers 4.1.0`
- `transformers 4.52.4`
- `chromadb 1.0.12`
- `faiss 1.11.0`

## 데이터
데이터 수집 및 전처리 과정은 [다음](https://github.com/INISW-6th/data-preprocessing)을 참고하세요.
1. 미래엔 중학교 2학년 역사 교과서(교사용)
2. 미래엔 중학교 2학년 역사 지도서
3. 한국학중앙연구회 한국민족문화대백과사전([링크](https://encykorea.aks.ac.kr/))

## LangChain 구성
LangChain 구성 및 최적화 과정은 [다음](https://github.com/INISW-6th/langchain-sys)을 참고하세요.
1. 메타데이터 기반의 데이터를 활용하는 Modular RAG 구성
2. 각 단계에 Prompt Engineering과 Modular RAG 내 Embedding/VectorDB/Reranker/LLM 평가
3. 각 단계에 최적화된 Prompt와 모델 설정

## Web System
백엔드 코드는 [다음](https://github.com/INISW-6th/t-prep-back), 프론트엔드 코드는 [다음](https://github.com/INISW-6th/t-prep-front)을 참고하세요.

## 참고문헌
- [1] 한정윤(2024), AI 기반 맞춤형 교육에 대한 교사의 인식과 경험, 한국교육개발원.
- [2] 강신천 외(2024), 중학교 교원의 인공지능융합교육 연수 인식 분석 및 활성화 방안, 컴퓨터교육학회.
