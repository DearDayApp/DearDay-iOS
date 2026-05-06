# 🌙 DearDay iOS

> 나를 더 이해하고 돌보는, 소중한 하루

---

## Overview

DearDay는 나만의 예외 상황까지 이해하는 프라이빗 주기 메이트입니다.  
불규칙한 주기, 피임약 복용, 예외 상황까지 — 나를 가장 잘 아는 앱을 목표로 합니다.

---

## Tech Stack

| 분류 | 기술 |
|------|------|
| UI | SwiftUI |
| 아키텍처 | TCA (The Composable Architecture) |
| 반응형 | RxSwift / Combine |
| 비동기 | Swift Concurrency (async/await) |
| 로컬 저장 | SwiftData |
| 암호화 | CryptoKit (AES-256-GCM) |
| 의존성 관리 | Swift Package Manager (SPM) |

---

## Architecture

```
┌─────────────────────────────────┐
│          SwiftUI View           │
├─────────────────────────────────┤
│   TCA (The Composable Arch.)    │
│       상태관리 / 사이드이펙트    │
├─────────────────────────────────┤
│       Combine / RxSwift         │
│         데이터 바인딩            │
├─────────────────────────────────┤
│      Swift Concurrency          │
│    네트워크 / 암호화 / DB        │
├─────────────────────────────────┤
│         Repository              │
│  SwiftData │ Keychain │ Network │
└─────────────────────────────────┘
```

---

## Features

> 🚧 세부 기능은 기획 확정 후 업데이트 예정

- 🗓️ 생리주기 기록 및 캘린더
- 🔮 배란일 · 가임기 예측
- 💊 피임약 모드
- 🔄 예외 주기 처리
- 🔔 스마트 지연 케어 알림 (Interactive Push)
- 📱 홈화면 · 잠금화면 위젯 (WidgetKit)
- 🏝️ Live Activity / Dynamic Island
- ⌚ Apple Watch 연동
- ❤️ HealthKit 연동
- 🔒 E2E 암호화 저장 (CryptoKit)

---

## Targets

| 타겟 | 설명 |
|------|------|
| DearDay | 메인 iOS 앱 |
| DearDayWidget | 홈화면 · 잠금화면 위젯 |
| DearDayWatch | Apple Watch 앱 |
| DearDayLiveActivity | Live Activity |

---

## Requirements

- iOS 16.0+
- watchOS 9.0+
- Xcode 15.0+
- Swift 5.9+

---

## Getting Started

```bash
# 레포 클론
git clone https://github.com/DearDayApp/DearDay-iOS.git

# 프로젝트 열기
cd DearDay-iOS
open DearDay.xcodeproj
```

> 의존성은 SPM으로 관리되어 Xcode 실행 시 자동으로 설치됩니다.

---

## Security

- 모든 생리 데이터는 **CryptoKit AES-256-GCM** 으로 암호화
- 암호화 키는 **Keychain** 에만 저장, 서버 전송 없음
- 서버에는 암호화된 데이터만 저장 (서버 관리자도 열람 불가)
- 기기 변경 시 암호화 데이터 복원 지원

---

## Branch Strategy

```
env/live      → 배포 브랜치
env/dev       → 개발 통합 브랜치
feature/*     → 기능 개발
fix/*         → 버그 수정
release/*     → 배포 준비
```

---

## Convention

### Branch
```
feat/#11-calendar-view
fix/#11-calendar-bug
```

### Commit
```
feat: 캘린더 뷰 구현
fix: 캘린더 날짜 오류 수정
chore: 개발 환경 세팅
design: 캘린더 UI 수정
docs: README 업데이트
refactor: 캘린더 뷰 리팩토링
```

### Issue / PR
```
[Feat] 캘린더 뷰 구현
[Fix] 캘린더 날짜 오류 수정
[Chore] 개발 환경 세팅
[Design] 캘린더 UI 수정
[Docs] README 업데이트
[Refactor] 캘린더 뷰 리팩토링
```

---

## iOS Team

| <img src="https://github.com/user-attachments/assets/0c39d778-617a-461a-b06a-dc0c47d7b209" width="100" height="100"> | <img src="https://github.com/user-attachments/assets/ba8bb80e-1b2d-4ac7-96e7-bf58ce9bedb9" width="100" height="100"> |
|:---|:---|
| **[유견희](https://github.com/YuGeonHui)** | **[엄재웅](https://github.com/woolnd)** |
| iOS Developer | iOS Developer |

---

## License

© 2025 DearDay. All rights reserved.
