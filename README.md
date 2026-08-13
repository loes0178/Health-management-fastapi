# 🏥 Health Management FastAPI

FastAPI를 활용한 건강관리 웹 애플리케이션 실습 프로젝트입니다.

Python 보충수업에서 제공된 실습용 starter code를 기반으로 진행하며,
제공된 프론트엔드와 Water 기능을 참고하여 미완성된 백엔드 기능을 직접 구현합니다.

⸻

## 🛠 Tech Stack

### Backend

* Python
* FastAPI
* Pydantic

### Database

* SQLite
* Tortoise ORM

### Frontend

* Jinja2
* HTML / CSS / JavaScript

⸻

## 📌 주요 기능

건강 데이터를 기록하고 관리할 수 있는 웹 애플리케이션입니다.

* 💧 물 섭취 기록
* 🏃 운동 기록
* 🍽️ 식사 기록
* 😴 수면 기록
* 📊 건강 데이터 리포트

⸻

## 💻 구현 내용

### 제공된 기능

* 프론트엔드 UI (templates, static)
* Water 관련 ORM 및 라우팅
* 기본 프로젝트 구조

### 직접 구현

현재 실습을 진행하며 아래 기능을 구현할 예정입니다.

* Exercise 모델 및 ORM 구현
* Meal 모델 및 ORM 구현
* Sleep 모델 및 ORM 구현
* DB 모델 등록
* 페이지 라우팅 구현
* REST API 엔드포인트 구현

구현이 완료될 때마다 체크리스트와 프로젝트 내용을 업데이트할 예정입니다.

⸻

## 📂 프로젝트 구조
```
app/
├── main.py              # FastAPI 앱 진입점
├── db.py                # 데이터베이스 연결 설정
├── schemas.py           # Pydantic 데이터 검증 스키마
│
├── models/              # Tortoise ORM 모델
│   ├── user.py
│   ├── water.py
│   ├── exercise.py
│   ├── meal.py
│   └── sleep.py
│
├── routers/             # URL 및 API 라우팅
│   ├── pages.py
│   └── api.py
│
├── services/            # 비즈니스 로직
├── templates/           # Jinja2 HTML 템플릿
└── static/              # CSS / JavaScript / 이미지
```
⸻

## 🔄 요청 및 응답 흐름
```
Client
  ↓
Router
  ↓
Schema
  ↓
Service
  ↓
Model
  ↓
SQLite Database
```
* Router: HTTP 요청을 받아 적절한 로직으로 연결
* Schema: Pydantic을 이용해 요청 및 응답 데이터 검증
* Service: 비즈니스 로직 처리
* Model: Tortoise ORM을 이용해 데이터베이스와 통신
* Database: SQLite에 건강 데이터 저장

⸻

## ▶️ 실행 방법

### 1. 가상환경 생성

`python -m venv .venv`

### 2. 가상환경 활성화

macOS / Linux

`source .venv/bin/activate`

### 3. 패키지 설치

`python -m pip install -r requirements.txt`

### 4. FastAPI 서버 실행

`python -m uvicorn app.main:app --reload`

서버가 실행되면 브라우저에서 안내된 로컬 주소로 접속합니다.

⸻

## 📚 학습 목표

이 프로젝트를 통해 다음 내용을 학습합니다.

* FastAPI 프로젝트의 기본 구조 이해
* Router / Service / Model 레이어의 역할 이해
* REST API의 요청 및 응답 흐름 이해
* Pydantic을 활용한 데이터 검증
* Tortoise ORM을 활용한 데이터베이스 연동
* SQLite를 활용한 데이터 저장
* Jinja2를 활용한 HTML 렌더링
* Git / GitHub를 활용한 프로젝트 버전 관리

⸻

## 📝 프로젝트 출처

Python 보충수업에서 제공된 실습용 starter code를 기반으로 진행한 개인 학습 프로젝트입니다.

프론트엔드와 일부 예제 기능은 실습 자료로 제공되었으며, 미완성된 백엔드 영역을 직접 구현하며 FastAPI의 구조와 동작 방식을 학습하는 것을 목적으로 합니다.