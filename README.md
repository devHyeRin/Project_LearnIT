# 📘 Acorn_Project_LearnIT  
실습 중심 올인원 E-Learning 플랫폼

---

## 💡 프로젝트 개요

LearnIT(런잇)은  
강의 시청 · 코드 실습 · 퀴즈 · Q&A · 성장 분석을  
**하나의 화면에서 통합 제공하는 실습 중심 올인원 E-러닝 플랫폼**입니다.

기존 온라인 강의 플랫폼은  
강의를 시청한 뒤 → IDE를 실행해 실습하고 → 다시 강의 화면으로 돌아오는 과정에서  
**학습 흐름이 끊기고 몰입도가 저하되는 문제**가 있었습니다.

LearnIT은 이러한 문제를 해결하기 위해 “학습 흐름이 끊기지 않는 환경”과  
“데이터 기반으로 성장 과정을 확인할 수 있는 구조”를 핵심 가치로 기획되었습니다.

---

## ⏱️ 프로젝트 정보

- **프로젝트명** : LearnIT
- **프로젝트 기간** : 2025.12.02 ~ 2026.01.15 (6주)
- **프로젝트 유형** : 팀 프로젝트 (E-Learning 플랫폼)
- **팀 구성** : 5인

---

## 🎯 프로젝트 목표

### 1️⃣ 몰입형 학습 환경 제공
- 강의 재생, 코드 작성·실행, Q&A, 퀴즈를 하나의 화면에 통합
- 불필요한 화면 전환 없이 학습에 집중할 수 있는 구조 설계

### 2️⃣ 데이터 기반 성장 관리
- GitHub 계정 연동을 통해 커밋 수, 사용 언어 분석
- 개인별 학습 성과를 육각형 스킬 차트로 시각화

### 3️⃣ 능동적인 학습 유도
- 챕터별·파이널 퀴즈 제공
- 단순 시청 중심이 아닌 **참여형 학습 구조** 구현

---

## 🚀 주요 기능

### 01. 올인원 강의 시스템 (통합 학습 플레이어)
- 강의 영상, 코드 에디터(인터프리터), 실행 결과, Q&A, 퀴즈를 하나의 화면에서 제공
- Java, Python 등 다국어 실시간 코드 실행 환경 지원
- 별도 IDE 설치 없이 웹에서 즉시 실습 가능

### 02. 챕터별 / 파이널 퀴즈
- 각 챕터 학습 후 즉각적인 이해도 점검
- 파이널 퀴즈를 통한 전체 학습 내용 종합 평가

### 03. GitHub 기반 역량 분석
- GitHub 계정 연동을 통한 커밋 수, 주 사용 언어 분석
- 분석 결과를 육각형 스킬 차트로 시각화하여 성장 지표 제공

### 04. 사용자 대시보드
- 수강 강의 진도율 관리
- 학습 현황 및 개인화 일정(To-Do) 관리

---

## 🎯 담당 영역 및 기여 내용 (이혜린)

본 프로젝트에서 **결제 도메인을 중심으로 백엔드 핵심 기능과 시스템 구조 설계에 기여**했습니다.

### 💳 결제 도메인 전담
- PortOne · 카카오페이 API 연동
- 외부 PG 연동 시 **중복 요청 및 네트워크 오류 가능성**을 고려하여  
  결제 승인 단계를 서버 기준으로 검증하는 흐름 설계

### 🔄 결제 트랜잭션 구조 설계
- 결제 승인 → 수강 권한 부여 → 결제 이력 저장 흐름 설계
- 중간 단계 실패 시 데이터 불일치 가능성을 인지
- 전 과정을 **단일 트랜잭션으로 처리**하여 결제 상태와 수강 권한 간 정합성 확보

### 🔗 백엔드 API 설계 참여
- AI 챗봇 연동을 위한 강의 데이터 제공 API 설계
- 챕터 단위 강의 · 퀴즈 · 학습 이력 조회 구조 정의

### 🧱 시스템 구조 및 협업 개선
- Git 충돌 및 유지보수 리스크를 사전에 인지
- Fragment 기반 UI 모듈화 구조 제안 및 적용
- WBS 및 API 명세서 작성을 통해 역할 범위와 변경 이력 관리

### 🐳 개발 환경 표준화
- Docker 기반 개발 환경 표준화 도입 제안 및 구성 참여
- 실행 환경 차이로 인한 오류 감소 및 협업 효율 개선

---

## 🧱 기술 스택 및 개발 환경

### Frontend
- HTML, CSS, JavaScript
- Thymeleaf
- Ajax, jQuery

### Backend
- Java, Spring Boot
- Spring Security, JPA, MyBatis
- REST API

### Database
- MySQL

### AI
- Python
- FastAPI
- OpenAI REST API

### DevOps / Cloud
- Docker, Docker Compose
- Nginx, Gradle
- AWS (EC2, S3, Lambda, ECR, EventBridge, SES, IAM, CloudWatch)

### Tools & Collaboration
- Git, GitHub
- IntelliJ IDEA
- Figma
- Notion, Slack

### Environment
- Windows, Ubuntu
- Git 기반 형상 관리

---



## 결제 기능 주의사항
본 프로젝트의 결제 기능은 **PG 연동 테스트 환경 기준**으로 구현되었습니다.
실제 운영 환경 적용 전 아래 사항에 대한 수정 및 보완이 필요합니다.


### 1️⃣ 일반 카드 결제 테스트 금액 처리
- 테스트 목적상 실제 주문 금액이 아닌 고정 테스트 금액(100원)으로 결제 처리
- 운영 환경 전환 시 실제 주문 금액 계산 로직으로 변경 필요

```java
int testAmount = 100; // 테스트 실결제 금액
```

### 2️⃣ 카카오페이 결제 취소 처리
- 카카오페이 API 정책상 결제 승인 API 사용 시 취소 API 설정이 필수
- 형식상 결제 취소 컨트롤러만 구현
- 실제 취소 요청 시 결제 취소 대신 결제 실패 페이지로 리다이렉트 처리

```java
@GetMapping("/payments/kakao/cancel")
public String kakaoPayCancel(@RequestParam("orderNo") String orderNo) {
    paymentKakaoService.cancel(orderNo);
    return "redirect:/payment/fail";
}

```

## 🚀 실행 방법
```bash
# 프로젝트 클론
git clone https://github.com/devHyeRin/Project_LearnIT.git
cd Project_LearnIT

# 실행
./gradlew bootRun
```

## 실행 환경
- Java 17 이상
- Gradle
-MySQL (로컬 또는 Docker)
- Git

> ⚠️ 본 프로젝트는 로컬 개발 환경 기준으로 실행됩니다. 외부 API Key(OpenAI, GitHub, PG 등)는 보안상 저장소에 포함되어 있지 않습니다.

## 접속 정보
> 메인 페이지 http://localhost:8080
> 관리자 페이지 http://localhost:8080/admin

## 👩‍💻 개발자

- 이혜린
- GitHub : https://github.com/devHyeRin

---

