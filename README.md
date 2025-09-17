# 2025_SEASONTHON_TEAM_2_BE
[2025 kakao X groom 시즌톤] 2팀 [ Everflow ] 백엔드 레포지토리

가족과 함꼐, 

<img width="7680" height="4320" alt="에버플로우_아키텍쳐맵" src="https://github.com/user-attachments/assets/752430aa-aa51-47e9-8764-f21266954c02" />

"이거 어떻게 버려야 하지?" 헷갈리는 분리배출, 이제 그만!
분리특공대는 복잡한 쓰레기 배출 정보를 한눈에 알려주고, 우리 동네 배출일에 맞춰 알림을 보내주는 똑똑한 분리배출 가이드 서비스입니다.
📌 기본 설명
목표
사용자 위치(기본 자치구/동) 기반으로 품목별 올바른 분리배출 방법을 안내
자주 검색되는 항목을 3시간 단위 랭킹으로 보여주어 트렌드를 제공
잘못 버리기 쉬운 주의 품목을 별도 안내(예: 음식물 타입이지만 실제로는 일반쓰레기)
⚙️ Bakcend 기술 스택
Gradle project
Spring Boot 3.x
Java 21
MySQL 8.x
Spring Data JPA
Spring Security + OAuth2 Client
jdbc template
☁️ 인프라 기술 스택
AWS EC2 + Docker
AWS RDS MySQL
AWS S3
Docker Hub
GitHub Actions (CI/CD)
🚀 주요 기능
인증/회원
카카오 OAuth2 로그인
JWT 발급/재발급, 로그아웃
지역 관리
시/도, 시/군/구, 읍/면/동 검색 및 기본 자치구 설정
분리배출 가이드
이미지 분석을 통해 쓰레기 분리 배출 방법 제공
품목 키워드 검색 → 지역별 배출 규칙 반환
주의 품목(redirect 타입) 처리
랭킹/트렌드
검색 로그 집계 → 3시간 단위 랭킹 갱신
공지/이력
Revision을 통한 제도 변경/공지 제공








<details>
<summary><h2>🤝 개발자 간 협업 방법(코드컨벤션, 브랜치 전략 등)</h2></summary>

## 🌿 Git 브랜치 전략
기능 개발 - feat 브랜치에서 작업 후, main 브랜치로 Pull Request.
<br>
버그 수정 - hotfix 브랜치에서 작업 후, main 브랜치로 Pull Request.
<br>
머지 전략 - 2명 이상의 BE 개발자 코드 리뷰 시 main 브랜치로 머지 가능.
<br>
간단한 기능은 1명 이상 승인 시 머지 가능.
<br>
PR올린지 24시간 경과시 승인이 없어도 CI가 안깨지면 머지 가능
<br>
CI가 깨지면, 머지 무조건 불가능
<br>

## 📝 커밋 메시지 컨벤션 (브랜치 전략 네이밍도 동일)
타입	설명
<br>
feat#이슈번호	새로운 기능 추가
<br>
hotfix#이슈번호	버그 수정
<br>
chore#이슈번호	빌드 작업, 환경 설정
<br>
refactor#이슈번호	코드 리팩토링 (기능 변경 없음)
<br>
docs#이슈번호	문서 수정
<br>

## 🔍 메서드 네이밍 컨벤션
생성 : create
<br>
수정 : update
<br>
삭제 : delete
<br>
조회 : find
<br>

## 💡 코드 컨벤션
클래스 선언부 아래 필드 작성 시 한 칸 띄우기
<br>
메서드 길이는 15줄 이하 (SRP 원칙 준수)
<br>
의미 없는 개행 제거, 개행 규칙 준수
<br>
블록 들여쓰기는 1단계로 제한
<br>
블록 띄어쓰기는 4칸, LF(Line Feed) 사용
<br>
블록 아래는 한 칸 띄우고 작성
<br>
else 사용 지양
stream 사용 시 .stream() 뒤에 줄바꿈
<br>

</details>
