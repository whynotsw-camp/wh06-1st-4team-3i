# 프로젝트 기획서

## 📌 프로젝트 개요
- 프로젝트 주제: **리뷰로 시작하는 컨텐츠: REVIEW.I**
- 프로젝트 목표: **IT/전자제품을 리뷰하고, 추천해주는 리뷰어,블로거의 수가 증가함에 따라 해당 리뷰어의 컨텐츠 제작시간 단축과 필터링 된 리뷰를 참조하여 구매 결정에 도움을 줄 수 있다.**
- 주요 타겟층: **IT/전자제품을 리뷰하는 리뷰어, 블로거**

### 기대 효과
- 리뷰어, 블로거의 상품 리뷰 조사 시간 단축
- 광고, 재구매, 키워드 분석을 통한 신뢰도 높은 리뷰를 필터링할 수 있다
- 필터링 된 리뷰를 토대로 OPENAI API를 이용해 리뷰와 관련된 컨텐츠의 초안을 얻을 수 있어 컨텐츠 제작에 도움을 받을 수 있음

### 팀 구성
- 김명재(팀장)
- 서세빈
- 서정원

### 서비스 플로우
![Image](https://github.com/user-attachments/assets/10ae1b2b-4de2-4625-9f5c-574707318dc3)

## 🗓️ 프로젝트 일정
![Image](https://github.com/user-attachments/assets/7ad77921-0720-43cd-a4c5-06e3a916e9ed)

  ------------------------------

# 작업 분할 구조 (WBS)

## 단계별 작업 구성

## 📋 기획 
### 🔍 문제 정의
- 리뷰의 성격을 광고성, 재구매성, 가성비 키워드, 긍정/부정 키워드 4가지 형태로 나눠 리뷰의 퀄리티 판단
- 수 많은 리뷰 데이터중 높은 퀄리티의 리뷰의 필터링의 필요성
- 목표 설정: 리뷰어/블로거의 상품 리뷰 조사 시간 단축, 컨텐츠 제작 도움

### 📊 데이터 요구사항 정의 
- 필요한 데이터 항목: 이커머스 사이트의 IT/전자제품 리뷰 이력
- 데이터 유형 정의: 정형 데이터
- 데이터 수집 방법 및 출처 선정

### 💾 데이터 수집 및 준비
- 필요한 데이터 수집: 이커머스 사이트 IT/전자제품 리뷰 이력
- 데이터 저장소 설계: 데이터베이스 또는 클라우드 저장소 선정
- 데이터 수집 크롤링 및 전처리를 위한 SQL 시스템 구축

### 📑 결과 도출
- 광고성, 재구매성, 가성비 키워드, 긍정/부정 키워드 4가지로 리뷰 요약 및 결과 분석
- 필터링된 리뷰들을 토대로 OPEN AI API 요청했을 때 나오는 결과 분석

  ------------------------------

# 화면 구성
![Image](https://github.com/user-attachments/assets/15efdb4b-81e0-4726-ad98-b97c44baa7f1)

  ------------------------------

# 요구사항 정의서
# 📌 요구사항 정의서 (기능 명세 표 형식)

| 기능명                      | 설명                                                                 |
|---------------------------|----------------------------------------------------------------------|
| 상품 정보 입력             | 사용자가 상품명 또는 URL을 입력할 수 있는 인터페이스 제공              |
| 입력값 유효성 검사         | 잘못된 URL, 오타 등 예외 처리 및 유효성 검증                          |
| 리뷰 수집 (크롤링)         | DB에 리뷰 없을 경우 Selenium을 통해 리뷰 자동 수집                    |
| 리뷰 전처리                | 수집된 리뷰에서 불필요한 요소 제거, 텍스트 정제                       |
| 광고성 리뷰 분류 모델 적용 | BERT 기반 모델로 광고/협찬 리뷰 판별                                 |
| 재구매 리뷰 탐지           | “재구매”, “두 번째 구매” 등의 표현 탐지 (정규표현식 기반)              |
| 가성비 키워드 분석         | “가성비”, “가격 대비 만족” 등의 키워드를 탐지하고 감성 분석 수행       |
| 분석 결과 요약 제공        | 광고성 비율, 재구매 비율, 키워드 클라우드, 신뢰도 점수 시각화 제공      |
| 대표 리뷰 추천             | 분석 기반으로 대표 리뷰 3~5개 추출하여 요약                          |
| 콘텐츠 초안 생성           | 블로그/유튜브용 콘텐츠 초안 자동 생성 (문체 및 분량 선택 가능)         |
| 콘텐츠 활용 기능           | 결과 복사, PDF/txt 다운로드, 노션/Docs 공유 기능 제공                 |
| 사용자 피드백 수집         | 초안 품질에 대한 별점 및 의견 수집                                    |
| 리뷰 수 부족 예외 처리     | 리뷰 수가 기준 이하일 경우 메시지 표시 및 유사 상품 추천               |


# 프로젝트 설계서

## 💻 시스템 아키텍쳐
![Image](https://github.com/user-attachments/assets/f91c64df-895a-487a-aa61-f442dca7d3a6)

## 🗂️ 데이터 설계
![Image](https://github.com/user-attachments/assets/c8b5cf78-d7df-4fc3-bb66-015d0b6a8f76)

# 📘 데이터 정의서

<details>
<summary>📁 테이블 1: category (카테고리)</summary>

### 테이블 정보

| 항목        | 설명                          |
|-------------|-------------------------------|
| 테이블 명   | category                         |
| 설명        | 상품의 카테고리를 분류 테이블  |
| 비고        | -                             |

### 컬럼 정의

| 컬럼명     | 데이터 타입 | 길이 | PK | NN | FK | 기본값           | 설명           |
|------------|-------------|------|----|----|----|------------------|----------------|
| id         | INT         | -    | O  | O  | O   | AUTO_INCREMENT   | 카테고리 ID       |
| name   | VARCHAR     | 100   |    | O  |    |                  | 카테고리 명    |

</details>

---

<details>
<summary>📦 테이블 1: Product (상품)</summary>

### 테이블 정보

| 항목        | 설명                     |
|-------------|--------------------------|
| 테이블 명   | Product                  |
| 설명        | 상품 정보를 저장하는 테이블 |
| 비고        | 카테고리와 외래키로 연결됨 |

### 컬럼 정의

| 컬럼명        | 데이터 타입 | 길이 | PK | NN | FK | 기본값           | 설명                       |
|----------------|-------------|------|----|----|----|------------------|----------------------------|
| id             | INT         | -    | O  | O  |    | AUTO_INCREMENT   | 상품 ID (기본키)           |
| name           | VARCHAR     | 255  |    | O  |    |                  | 상품명                     |
| brand          | VARCHAR     | 100  |    |    |    |                  | 브랜드명                   |
| model_number   | VARCHAR     | 100  |    |    |    |                  | 모델 번호                  |
| release_date   | DATE        | -    |    |    |    |                  | 출시일                     |
| category_id    | INT         | -    |    |    | O  |                  | 카테고리 ID (외래키)       |
| created_at     | TIMESTAMP   | -    |    |    |    | CURRENT_TIMESTAMP| 생성일시                   |

</details>

---

<details>
<summary>📦 테이블 2: Review (리뷰)</summary>

### 테이블 정보

| 항목        | 설명                       |
|-------------|----------------------------|
| 테이블 명   | Review                     |
| 설명        | 사용자 리뷰 정보를 저장     |
| 비고        | 상품과 외래키로 연결됨      |

### 컬럼 정의

| 컬럼명       | 데이터 타입 | 길이 | PK | NN | FK | 기본값           | 설명                    |
|--------------|-------------|------|----|----|----|------------------|-------------------------|
| id           | INT         | -    | O  | O  |    | AUTO_INCREMENT   | 리뷰 ID (기본키)        |
| product_id   | INT         | -    |    | O  | O  |                  | 연결된 상품 ID (외래키) |
| reviewer_id  | VARCHAR     | 100  |    |    |    |                  | 리뷰 작성자 ID           |
| source_url   | TEXT        | -    |    |    |    |                  | 리뷰 원문 URL            |
| content_raw  | TEXT        | -    |    |    |    |                  | 원문 텍스트              |
| rating       | DECIMAL     | 2,1  |    |    |    |                  | 리뷰 평점                |
| review_date  | DATE        | -    |    |    |    |                  | 리뷰 작성일              |

</details>

---

<details>
<summary>📦 테이블 3: Review_repurchase_analysis (재구매 분석)</summary>

### 테이블 정보

| 항목        | 설명                         |
|-------------|------------------------------|
| 테이블 명   | Review_repurchase_analysis   |
| 설명        | 리뷰에서 재구매 언급 분석     |

### 컬럼 정의

| 컬럼명              | 데이터 타입 | 길이 | PK | NN | FK | 기본값         | 설명                        |
|---------------------|-------------|------|----|----|----|----------------|-----------------------------|
| id                  | INT         | -    | O  | O  |    | AUTO_INCREMENT | 고유 ID                     |
| review_id           | INT         | -    |    | O  | O  |                | 연결된 리뷰 ID (외래키)     |
| mentions_repurchase | BOOLEAN     | -    |    |    |    |                | 재구매 언급 여부             |
| repurchase_score    | FLOAT       | -    |    |    |    |                | 재구매 점수                 |
| repurchase_phrases  | TEXT        | -    |    |    |    |                | 재구매 관련 구문             |

</details>

---

<details>
<summary>📦 테이블 4: Review_sentiment_keywords (감성 키워드 분석)</summary>

### 테이블 정보

| 항목        | 설명                       |
|-------------|----------------------------|
| 테이블 명   | Review_sentiment_keywords |
| 설명        | 긍정/부정 키워드 및 감성 점수 분석 |

### 컬럼 정의

| 컬럼명               | 데이터 타입 | 길이 | PK | NN | FK | 기본값         | 설명                      |
|----------------------|-------------|------|----|----|----|----------------|---------------------------|
| id                   | INT         | -    | O  | O  |    | AUTO_INCREMENT | 고유 ID                   |
| review_id            | INT         | -    |    | O  | O  |                | 연결된 리뷰 ID (외래키)   |
| positive_keywords    | TEXT        | -    |    |    |    |                | 긍정 키워드                |
| negative_keywords    | TEXT        | -    |    |    |    |                | 부정 키워드                |
| sentiment_balance_score | FLOAT    | -    |    |    |    |                | 감성 균형 점수             |

</details>

---

<details>
<summary>📦 테이블 5: Review_value_keywords (가성비 분석)</summary>

### 테이블 정보

| 항목        | 설명                         |
|-------------|------------------------------|
| 테이블 명   | Review_value_keywords        |
| 설명        | 가격/기능 키워드와 가성비 분석 |

### 컬럼 정의

| 컬럼명             | 데이터 타입 | 길이 | PK | NN | FK | 기본값         | 설명                     |
|--------------------|-------------|------|----|----|----|----------------|--------------------------|
| id                 | INT         | -    | O  | O  |    | AUTO_INCREMENT | 고유 ID                  |
| review_id          | INT         | -    |    | O  | O  |                | 연결된 리뷰 ID (외래키)  |
| price_keywords     | TEXT        | -    |    |    |    |                | 가격 관련 키워드          |
| feature_keywords   | TEXT        | -    |    |    |    |                | 기능 관련 키워드          |
| value_for_money_score | FLOAT    | -    |    |    |    |                | 가성비 점수               |

</details>

---

<details>
<summary>📦 테이블 6: Review_ad_analysis (광고성 여부 분석)</summary>

### 테이블 정보

| 항목        | 설명                        |
|-------------|-----------------------------|
| 테이블 명   | Review_ad_analysis          |
| 설명        | 리뷰 광고성 여부 분석        |

### 컬럼 정의

| 컬럼명             | 데이터 타입 | 길이 | PK | NN | FK | 기본값         | 설명                      |
|--------------------|-------------|------|----|----|----|----------------|---------------------------|
| id                 | INT         | -    | O  | O  |    | AUTO_INCREMENT | 고유 ID                   |
| review_id          | INT         | -    |    | O  | O  |                | 연결된 리뷰 ID (외래키)   |
| is_ad              | BOOLEAN     | -    |    |    |    |                | 광고 여부                 |
| ad_suspicion_score | FLOAT       | -    |    |    |    |                | 광고 의심 점수             |
| evidence_phrases   | TEXT        | -    |    |    |    |                | 광고 근거 구문             |

</details>

---

<details>
<summary>📦 테이블 7: generated_drafts (OpenAI 초안 생성)</summary>

### 테이블 정보

| 항목        | 설명                          |
|-------------|-------------------------------|
| 테이블 명   | generated_drafts              |
| 설명        | 리뷰 기반 생성된 초안 저장 테이블 |

### 컬럼 정의

| 컬럼명       | 데이터 타입 | 길이 | PK | NN | FK | 기본값              | 설명                            |
|--------------|-------------|------|----|----|----|---------------------|---------------------------------|
| id           | INT         | -    | O  | O  |    | AUTO_INCREMENT      | 고유 ID                         |
| review_id    | INT         | -    |    | O  | O  |                     | 연결된 리뷰 ID (외래키)         |
| source_url   | TEXT        | -    |    |    |    |                     | 리뷰 원문 URL                   |
| content_draft| TEXT        | -    |    |    |    |                     | 생성된 초안 텍스트              |
| model_used   | VARCHAR     | 20   |    |    |    |                     | 사용된 OpenAI 모델              |
| is_saved     | BOOLEAN     | -    |    |    |    | FALSE               | 사용자가 저장했는지 여부        |
| created_at   | TIMESTAMP   | -    |    |    |    |

## 📚 기술 스택

<div align=center>
    <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
    <img src="https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white">
    <img src="https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white">
    <img src="https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white">
    <img src="https://img.shields.io/badge/openai-412991?style=for-the-badge&logo=openai&logoColor=black">
    <img src="https://img.shields.io/badge/Amazon%20EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=black">
    <img src="https://img.shields.io/badge/Amazon%20S3-FF9900?style=for-the-badge&logo=amazons3&logoColor=white">
    <img src="https://img.shields.io/badge/Amazon%20RDS-527FFF?style=for-the-badge&logo=amazonrds&logoColor=black">
    <img src="https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white">
    <img src="https://img.shields.io/badge/-selenium-%43B02A?style=for-the-badge&logo=selenium&logoColor=white">
    <img src="https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white">
</div>

## ⚠️ 예상 문제 및 해결 방안
- **문제**: 리뷰가 일정 갯수 이하인 경우 필터링 된 리뷰의 신뢰도 하락
- **해결 방안**: 리뷰가 특정 갯수 이상인 상품에 대한 리뷰만 필터링하여 출력