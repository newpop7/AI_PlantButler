# AI_PlantButler
식물의 전반적인 성장과정을 도와주는 서비스

---

## 주요 기능
1. **식물 생육 캘린더**
   - 매일 식물 사진 업로드 시 캘린더에 저장
   - 자동 분석 후 피드백 제공
2. **질병 분석 서비스**
   - 카메라를 통한 식물 사진 수집
   - 이미지 분석
   - AI 챗봇을 통한 문제 확인 및 해결책 제공
3. **이상 환경 감지 서비스**
   - 기상청 날씨 변화에 따라 관리해야 할 식물 알림

---

## 팀 구성 및 역할 (웹 제외)

| 역할 | 담당 기능/업무 | 비고 |
|------|----------------|------|
| 송진호 | 안드로이드 앱 개발, UI/UX 디자인 | 캘린더 화면, 사진 업로드, 분석 결과 표시 |
| 김민석 | 안드로이드 기능 보조 및 UI 개선 | 앱 내 알림, 사진 업로드 로직, UX 개선 |
| 권대연 / AI1 | 서버 개발, API 구축, DB 설계 | 사용자 관리, 사진 저장, 분석 요청 처리, Push 알림 |
| 유병연 / AI2 | AI 모델 개발 및 통합 | Azure AI 모델 연동, 이미지 전처리, 질병 분석, 챗봇 연동 |

---

## 개발 환경 및 도구
- **버전 관리**: GitHub (Private Repository, 브랜치 전략 사용)
- **프로젝트 관리**: Trello / Notion
- **커뮤니케이션**: Slack / Discord
- **개발 환경**
  - 안드로이드: Android Studio, Kotlin
  - 백엔드/AI: Python, Azure AI API, Flask/FastAPI 등

---

## 프로젝트 진행 단계 (5일 버전)

| 일차 | 주요 작업 | 담당/비고 |
|------|-----------|-----------|
| **1일차** | 기획 및 환경 세팅<br>- 핵심 기능 확정 (캘린더, 질병 분석, AI 피드백)<br>- UI/UX 목업 제작<br>- GitHub 레포 생성, 브랜치 전략 설정<br>- 개발 환경 세팅 | 팀 전체 |
| **2일차** | 기능 개발 시작 (병렬)<br>- 안드로이드: 캘린더 화면, 사진 업로드<br>- 백엔드: 서버 API, DB 구조 설계<br>- AI: 이미지 전처리 및 Azure AI 연결 테스트 | 팀원별 역할 분리 |
| **3일차** | 핵심 기능 개발 마무리<br>- 안드로이드: 사진 업로드 → API 연동<br>- AI 모델: 질병 분석 결과 반환<br>- 백엔드: Push 알림 / 챗봇 기본 로직 | 팀원별 역할 조정, 병합 시작 |
| **4일차** | 통합 테스트 및 버그 수정<br>- 전체 플로우 테스트 (사진 업로드 → 분석 → 피드백)<br>- UI/UX 개선<br>- 버그/충돌 해결 | 팀 전체 |
| **5일차** | 배포 및 최종 점검<br>- 안드로이드: Internal Testing 또는 APK 배포<br>- 백엔드: Azure App Service 배포<br>- 최종 README/문서 정리, 발표 자료 준비 | 팀 전체 |

---

## 팀원별 역할 체크리스트

### 송진호 (Android UI/UX 담당)
- [ ] 캘린더 화면 개발
- [ ] 사진 업로드 화면 구현
- [ ] 분석 결과 표시 UI 구현
- [ ] 앱 내 알림 기능 구현

### 김민석 (Android 기능 보조)
- [ ] 사진 업로드 로직 구현
- [ ] 앱 내 알림 로직 보조
- [ ] UX 개선 및 피드백 반영

### 권대연 / AI1 (서버/백엔드 담당)
- [ ] FastAPI 서버 구축
- [ ] API 엔드포인트 구현
- [ ] DB 설계 및 사진 저장 기능 구현
- [ ] Push 알림 처리
- [ ] 챗봇 기본 로직 구현

### 유병연 / AI2 (AI 모델 담당)
- [ ] Azure AI 모델 연동
- [ ] 이미지 전처리 / 분석 로직 구현
- [ ] 질병 판별 결과 생성
- [ ] 챗봇 연동 로직 구현


---

## 협업 전략
1. **Git 브랜치 전략**
   - main: 안정화 코드
   - feature-XXX: 기능 단위 브랜치
   - Pull Request(PR) → 코드 리뷰 후 merge
2. **데이터 관리**
   - 사진, AI 모델 파일은 `.gitignore` 처리 + 별도 스토리지(Azure Blob Storage) 사용
   - 환경변수, API Key는 `.env`에 저장

---

## 기타
- `.gitignore` 설정 예시: Android + Python 통합
- 프로젝트 관련 자료는 Trello/Notion을 통해 관리

- !!!!!주의!!!!

  실행이 안될시
  
  필수 프로그램 설치 확인 (Android Studio SDK Manager)
가장 먼저, 새 컴퓨터의 안드로이드 스튜디오에 프로젝트에 필요한 부품들이 모두 설치되었는지 확인해야 합니다.

새 컴퓨터에서 안드로이드 스튜디오를 엽니다.

오른쪽 위 File > Settings (macOS는 Android Studio > Settings)로 들어갑니다.

Languages & Frameworks > Android SDK 메뉴로 이동합니다.

SDK Platforms 탭에서, 우리 프로젝트의 compileSdk 버전에 맞는 Android API 34 (또는 그 이상)가 설치(Installed)되어 있는지 확인합니다. 없다면 체크해서 설치해주세요.

SDK Tools 탭으로 이동하여 아래 항목들이 반드시 체크 및 설치되어 있는지 확인합니다.

Android SDK Build-Tools

Android SDK Command-line Tools

Android Emulator

Android SDK Platform-Tools


