# 프로젝트 기획서

## 📌 프로젝트 개요
- 프로젝트 주제: **리뷰로 시작하는 컨텐츠: 오픈 리뷰 아이**
- 프로젝트 목표: **IT/전자제품을 리뷰하고, 추천해주는 리뷰어,블로거의 수가 증가함에 따라 해당 리뷰어의 컨텐츠 제작시간 단축과 필터링 된 리뷰를 참조하여 구매 결정에 도움을 줄 수 있다.**
- 주요 타겟층: IT/전자제품을 리뷰하는 리뷰어, 블로거

### 기대 효과:
- 리뷰어, 블로거의 상품 리뷰 조사 시간 단축
- 해당 상품에 대한 컨텐츠 제작에 도움

### 팀 구성
- 김명재(팀장)
- 서세빈
- 서정원

### 서비스 흐름도
![Image](https://github.com/user-attachments/assets/5755e2b9-bee2-43b3-bd83-455866f837a2)

## 📖 프로젝트 일정 (Gantt 차트)
- 간트 차트 이미지

### 1~2주
- 프로젝트 기획 및 주제 선정
- 데이터 수집 및 크롤링

### 3~4주
- 데이터 전처리
- 데이터 모델링

### 5~7주
- 데이터 시각화 및 웹서비스 구현

### 8주
- 문서화 및 발표 자료 작성

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

### 3. 데이터 분석 및 모델링
- 데이터 탐색 및 시각화
- 모델 선택 및 학습
- 성능 평가

### 4. 결과 도출 및 보고
- 결과 요약

  ------------------------------

# 요구사항 정의서

# 프로젝트 설계서

## 1. 시스템 아키텍쳐
- image

## 2. 데이터 설계
![Image](https://github.com/user-attachments/assets/52543e0e-e6e6-45f8-b014-92a1dcf8bbe0)
<!-- - **데이터 흐름**: 데이터 -> 전처리 -> 분석 -> 결과
- **주요 데이터 속성**
    - 속성 이름
    - 데이터 유형: 정량 -->

## 📚 기술 스택

<div align=center>
    <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=black">
    <img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=black">
    <img src="https://img.shields.io/badge/flask-000000?style=for-the-badge&logo=flask&logoColor=white">
    <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
    <img src="https://img.shields.io/badge/openai-412991?style=for-the-badge&logo=openai&logoColor=black">
    <img src="https://img.shields.io/badge/Amazon%20EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=black">
    <img src="https://img.shields.io/badge/Amazon%20S3-FF9900?style=for-the-badge&logo=amazons3&logoColor=white">
    <img src="https://img.shields.io/badge/Amazon%20RDS-527FFF?style=for-the-badge&logo=amazonrds&logoColor=black">
    <img src="https://img.shields.io/badge/nginx-009639?style=for-the-badge&logo=nginx&logoColor=black">
    <img src="https://img.shields.io/badge/selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=black">
</div>

## 4. 예상 문제 및 해결 방안
- **문제**: 리뷰가 일정 갯수 이하인 경우 필터링 된 리뷰의 신뢰도 하락
- **해결 방안**: 리뷰가 특정 갯수 이상인 상품에 대해서만 결과 도출