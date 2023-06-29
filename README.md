## LG_Recommend_Content_7th

대회 URL: https://www.upstage.ai/newsroom/upstage-lguplus-ai-ground-2022

주최/주관 : LG U+ / Upstage

진행 기간 : 2022.11.17 ~ 2022.12.02

대회설명:
  * LG U+ 아이들나라 시청 데이터를 이용하여 고객에게 컨텐츠 추천 모델 개발 (Recommendation)
  
대회 목표:
  * 청 시작, 종료, 구매 이력, 프로필 정보 등 총 8개로 나눠진 데이터를 이용하여 고객이 선호할 만한 컨텐츠를 추천해주는 AI 모델 개발

대회 결과 :
  * NCF 모델과 간단한 기법을 통하여 추천 AI 모델 개발
  * 🏆대회 최종 7등 달성
 * * *
 ## 대회 진행 환경 & 역할
 프로젝트 진행 환경 : Google Colab Pro
 
 팀구성 : 3명
 
 역할 :
  * 모델링 및 테스트
    * GNN 모델 Link Prediction Task 시도
    * 모델 테스팅
* * *
## 진행 상세 과정
1.데이터 분석
  * EDA 분석 결과
    * 연속재생이 많음 > 좋아하는 컨텐츠를 한번 틀고 연속적으로 소비
    * 처음 소비한 컨텐츠는 고객의 선호도를 반영할 수 있다고 가정.
    * 컨텐츠 소비시간 비율이 50% 이상인 데이터만 사용
    * “Session_id가 추천에 도움이 될것이다” 결론
  
2.모델링
  * NCF(Neural Collaborative Filtering) 특징
    * NCF(Neural Collaborative Filtering) 특징
    * DL을 이용해 Matrix Factorization을 수행하여 User-Item Interaction 에 적용
    * Point-wise Loss + Negative Sampling 사용
    * GMF와 MLP의 장점을 모두 살린 네트워크 구조
    
3.모델 테스트
  * 데이터 분석을 통해 얻은 정보를 바탕으로 테스트
    * Session_id를 기준으로 전처리한 결과 성능 향상
    * Negative_ratio 비율값 조정 후 테스트
    * 데이터 feature를 embedding하여 추가 후 테스트
  
4.성능 향상 방법
  * K-fold를 사용하여 결과물 일반화 및 성능 향상
    * 기존보다 약 10% 향상된 성능 달성 
