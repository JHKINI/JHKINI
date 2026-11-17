# AI Web Developer | Java · Spring Boot · Python · React

Java / Spring Boot / Python(FastAPI) / React / SQL

단순히 기능을 구현하는 것보다, 사용자의 문제를 어떤 기능과 데이터 구조로 풀 것인지 먼저 고민합니다.

막연한 고민을 실행 단위로 쪼개 주는 서비스(한걸음), 틀린 문제를 기록하고 반복 오답을 분석하는 서비스(RepeatCut), 창업 지원사업 공고를 관리하는 게시판(공고 Tracker)을 직접 기획하고 만들었습니다. 소형 LLM을 로컬에서 돌려 전문 용어를 일관되게 번역하는 용어집 번역기도 실험해 보았습니다.

---

## Tech Stack

### Main

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=databricks&logoColor=white)

### Web & Backend

![Spring MVC](https://img.shields.io/badge/Spring_MVC-6DB33F?style=flat-square&logo=spring&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API-005571?style=flat-square)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)

### Database

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white)

### AI

![Gemini](https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)

### Tools

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ_IDEA-000000?style=flat-square&logo=intellijidea&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)

---

## Main Projects

### [한걸음 (One-Step)](https://github.com/JHKINI/one-step)

React / Spring Boot / MySQL / Flyway / LLM

해야 할 일을 앞두고 고민만 길어져 시간을 보낸 경험에서 출발한 서비스입니다. LLM과 대화하며 막연한 고민을 바로 실행할 수 있는 작은 단위로 쪼개 주어 실행력을 높입니다. 프로젝트, 공부, 시험, 운동, 습관, 정리, 취업 준비 등 어떤 종류의 일에도 사용할 수 있습니다.

**주요 구현 및 경험**

- React 멀티페이지 화면 구성
- LLM 대화 기반 추천과 실행 단위 쪼개기
- Spring Boot 백엔드와 MySQL 연동
- Flyway를 이용한 DB 버전 관리와 완료 기록 저장
- 로그인 없이 기기 UUID로 사용자를 구분하는 구조

**중점적으로 고민한 부분**

- 막연한 입력을 실행 가능한 단위로 바꾸는 대화 흐름
- 로그인 부담 없이 기록을 이어 가는 사용자 구분 방식
- 특정 목적에 한정되지 않는 범용적인 서비스 범위

---

### [RepeatCut - 반복 오답 분석 서비스](https://github.com/JHKINI/RepeatCut)

React / FastAPI / SQLite / Gemini API

자격증·기출 시험에서 틀린 문제를 이미지와 함께 기록하고, 키워드·오답 이유·문제지별로 반복 오답을 분석해 학습 방법까지 추천하는 서비스입니다.

**주요 구현 및 경험**

- 이메일 회원가입·로그인과 회원별 데이터 분리
- 7개 테이블 설계, `PRAGMA user_version` 기반 DB 마이그레이션
- 시험 이름 → 유형 → 회차 순으로 고르는 선택형 입력으로 반복 입력 최소화
- 같은 문제를 다시 틀리면 새로 등록하지 않고 시도 이력으로 누적
- 키워드·오답 이유별 통계와 추이 그래프
- Gemini API로 통계 기반 학습 방법 추천 (실패 시 규칙 기반 추천으로 대체)
- 문제 이미지 파일 저장 구조 분리 (로컬 / S3 호환)
- pytest 34개 테스트

**중점적으로 고민한 부분**

- 같은 문제를 판단하는 기준(문제지 + 문제 번호)과 중복 방지
- 이미지 파일과 데이터베이스의 역할 분리
- 회원별 데이터 분리를 SQL 조건 한 곳에서 관리하는 구조
- AI 호출 실패 시에도 동작하는 안정적인 추천 기능

---

### [공고 Tracker - 창업 지원사업 공고 게시판](https://github.com/JHKINI/startup-notice-tracker)

Java / Spring Boot / Thymeleaf / MySQL

창업 지원사업 공고를 모아 보고 관리하는 CRUD 중심의 웹 게시판입니다. 단순한 관심 공고·마감일순 조회에서 더 나아가, 지원 진행 상태를 관리하는 기능을 더했습니다.

**주요 구현 및 학습 내용**

- Spring Boot 기반 웹 애플리케이션 구성
- Controller / Service / 데이터 접근 계층의 역할 분리
- Thymeleaf 화면과 MySQL 연동
- 공고 등록·조회·수정·삭제 (CRUD)
- 지원 상태 관리 (관심 → 준비중 → 제출완료)

**중점적으로 고민한 부분**

- 단순 조회와 차별화되는 "지원 관리" 중심의 기능 설계
- 계층별 책임 구분과 유지보수를 고려한 코드 구조
- 데이터베이스와 객체 간 매핑

---

### [로컬 LLM 용어집 번역기](https://github.com/JHKINI/local-llm-glossary-translator)

Python / FastAPI / React / Ollama (qwen3.5:4b)

소형 LLM이 전문 용어를 매번 다르게 번역하는 문제를, 번역할 때 반도체 용어집을 프롬프트에 넣어 해결해 본 프로토타입입니다. 번역 품질을 증명하는 것이 아니라 작은 실험으로 효과를 확인하는 데 목적을 두었습니다.

**주요 구현 및 경험**

- Ollama 로컬 LLM 연동 (RTX 3080 10GB, temperature 0)
- 입력 문장에 실제로 등장한 용어만 골라 프롬프트에 주입하는 용어집 필터
- 번역문에서 적용된 용어를 강조하고, 용어별 적용 여부 표시
- 한국어 ↔ 영어 번역 화면, 사용자 용어 추가, 서버·Ollama 연결 상태와 원인별 오류 메시지
- FastAPI + Pydantic 요청 검증, React + Vite 반응형 화면

**실험 결과**

- 문장 15개(용어 포함 10, 비교용 5)를 용어집 없음 / 전체 용어집 / 해당 용어만 주입, 3가지 조건으로 비교
- 용어 정확도 2/10 → 10/10으로 상승
- 전체 용어집을 넣으면 용어 없는 문장 5개 중 4개가 바뀌었고, 해당 용어만 넣으면 5개 모두 유지
- 표본이 작고 모델·실행 횟수가 1회씩이라는 한계를 README에 함께 정리

**중점적으로 고민한 부분**

- 불필요한 용어를 넣어 원래 번역이 흔들리지 않게 하는 필터링 방식
- 한국어 조사를 고려한 용어 매칭
- 결과의 한계를 숨기지 않는 실험 기록

---

## Other Projects

- [Weather Data Pipeline & Web Dashboard](https://github.com/JHKINI/kma-weather-data-pipeline) : 기상청 관측 데이터 수집, 전처리, 적재, 품질 확인, 시각화
- [Data Quality Diagnosis Project](https://github.com/JHKINI/Data_quality_project) : 데이터 품질 진단 기준 설계와 Streamlit 프로토타입
- [Vehicle License Plate Detection](https://github.com/JHKINI/nextframe_opencv) : OpenCV 번호판 검출 팀 프로젝트 (팀장)

---

## Development Focus

- **Backend Development** : Java, Spring Boot, FastAPI 기반 웹서비스 개발
- **Database Design** : 테이블 관계 설계, 마이그레이션, 회원별 데이터 분리
- **API Integration** : 서버와 화면, 외부 AI API 간 데이터 통신
- **Service Planning** : 사용자 요구사항을 기능과 데이터 구조로 구체화
- **Problem Solving** : 오류 원인 분석, 테스트와 검증, 개선
- **Collaboration** : Git 기반 형상 관리와 프로젝트 통합

기능을 구현하는 데서 끝나지 않고, 서비스가 왜 필요한지와 데이터가 흐르는 구조를 함께 이해하는 개발자가 되고자 합니다.

---

## Contact

- GitHub: https://github.com/JHKINI
- Email: 38633@naver.com
