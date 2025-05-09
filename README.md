# 프로젝트 기획서

## 📌 프로젝트 개요
- 프로젝트 주제: **리뷰로 시작하는 컨텐츠: 오픈 리뷰 아이**
- 프로젝트 목표: **IT/전자제품을 리뷰하고, 추천해주는 리뷰어,블로거의 수가 증가함에 따라 해당 리뷰어의 컨텐츠 제작시간 단축과 필터링 된 리뷰를 참조하여 구매 결정에 도움을 줄 수 있다.**
- 주요 타겟층: **IT/전자제품을 리뷰하는 리뷰어, 블로거**

### 기대 효과
- 리뷰어, 블로거의 상품 리뷰 조사 시간 단축
- 리뷰어, 블로거의 상품 컨텐츠 제작에 도움
- 광고, 재구매, 키워드 분석을 통한 신뢰도 있는 리뷰 추출

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
![Image](https://github.com/user-attachments/assets/63967d17-334e-4e92-b620-938a6114feaa)

  ------------------------------

# 프로젝트 설계서

## 💻 시스템 아키텍쳐
![Image](https://github.com/user-attachments/assets/f91c64df-895a-487a-aa61-f442dca7d3a6)

## 🗂️ 데이터 설계
![Image](https://github.com/user-attachments/assets/fcf80654-e71a-4488-9d46-59d628c0c173)

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
- **해결 방안**: 리뷰가 특정 갯수 이상인 상품에 대해서만 결과 도출