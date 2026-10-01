# Perch 시작하기

## 내 기기에 맞는 버튼 하나만 누르세요

**[Mac 다운로드](https://github.com/moonweave/perch-releases/releases/download/v0.1.15/Perch-0.1.15-macOS-universal.dmg)** · **[Windows 다운로드](https://github.com/moonweave/perch-releases/releases/download/v0.1.15/Perch-0.1.15-windows-x64-setup.exe)**

v0.1.15 공개 기준. Mac은 macOS 14 이상(Intel·Apple Silicon), Windows는 Windows 11 x64용이에요. Source code, README, 고지 문서는 설치 파일이 아니에요. 아직 v0.1.15가 공개되지 않았다면 [최신 릴리스](https://github.com/moonweave/perch-releases/releases/latest)에서 받을 수 있는 버전을 확인하세요.

기본 흐름은 **다운로드 → 파일 확인 → 설치 → Perch 설정에서 연결 → 첫 요청 확인**입니다. Codex나 Claude Code는 먼저 설치되어 있어야 해요. 일반 Claude 채팅이 아니라 이 기기에서 실행하는 개발 세션을 관찰해요. Perch는 무료이고 Codex·Claude 이용 조건과 비용은 별개예요.

## 명령어가 낯설면 AI와 같이 설치해요

이미 쓰는 Codex나 Claude에 아래 요청문을 복사해 보내세요. 새 유료 도구를 살 필요는 없지만 AI 사용량은 소모될 수 있어요.

- **화면 안내:** AI에게 아래 요청문을 보내고 현재 화면에 보이는 내용을 알려 주면 다음 단계를 물어볼 수 있어요.
- **파일 확인:** 설치 파일과 `.sha256` 파일을 직접 비교한 경우에만 확인이 끝난 거예요. AI가 실제로 두 파일을 대조하지 않았다면 검증됐다고 볼 수 없어요.

화면을 공유할 때는 계정 정보, 경로, 요청·응답 내용부터 가려 주세요.

```text
Perch 무료 베타 설치를 도와줘. 터미널과 PowerShell은 낯설어.
공식 안내: https://github.com/moonweave/perch-releases/blob/main/START-HERE.md
공식 파일: https://github.com/moonweave/perch-releases/releases/tag/v0.1.15

내 운영체제부터 확인하고 맞는 설치 파일 하나를 골라줘.
설치 파일과 체크섬 파일을 실제로 비교할 수 있으면 결과를 알려줘. 비교할 수 없다면 직접 확인했다고 말하지 말고 내가 할 클릭을 한 단계씩 안내해줘.
설치와 설정 변경 전에는 바뀌는 내용을 설명하고 내 확인을 받아줘.
보안 경고와 Codex 훅 신뢰는 내가 직접 판단할게.
보안 기능 해제, 격리 속성 제거, 관리자 권한 우회, 유료 결제, 알 수 없는 스크립트 실행은 하지 마.
기존 설정과 다른 훅을 보존해. prepare --apply나 설정 전체 덮어쓰기로 복구하지 마.
Perch 설정 → 연결에서 연결하고, Codex는 코딩 → Hook에서 Perch 훅만 검토하도록 안내해줘.
내가 읽기 전용 요청을 보낸 뒤 작업함에 요청·응답이 들어오는지 확인해줘.
막히면 변경을 멈추고 원인과 선택지를 알려줘. 비밀값·대화 원문·개인 경로를 외부에 보내지 마.
```

AI가 설치를 끝냈다고 말해도, Perch가 실제로 열리고 새 작업이 기록되는지 확인해야 해요. 체크섬은 파일 변경 여부만 확인하지 게시자나 안전성을 인증하지는 않아요.

## 혼자 설치하려면

1. 위의 내 기기용 버튼으로 설치 파일을 받아요. 확인용 파일도 함께 받아요: [Mac 체크섬](https://github.com/moonweave/perch-releases/releases/download/v0.1.15/Perch-0.1.15-macOS-universal.dmg.sha256) · [Windows 체크섬](https://github.com/moonweave/perch-releases/releases/download/v0.1.15/Perch-0.1.15-windows-x64-setup.exe.sha256).
2. AI에게 다음 단계를 물어보거나 [Mac 상세 안내](INSTALL.md#2-파일-확인) / [Windows 상세 안내](INSTALL-WINDOWS.md#2-파일-확인)에 따라 직접 확인해요. 파일을 실제로 비교하지 않았다면 검증이 끝난 게 아니에요.
3. Mac은 DMG를 열고 Perch를 Applications로 옮겨요. Windows는 설치 파일을 열어 현재 계정에 설치해요.
4. 현재 베타는 서명·공증이 없어 OS 경고가 나올 수 있어요. 설치하기로 했다면 상세 안내를 따라 직접 판단하세요. 스마트 앱 컨트롤이나 관리 정책이 차단하면 멈춰 주세요. 보안 기능을 끄지 마세요.
5. Perch를 열고 **설정 → 연결 → 훅 연결 → 허용하고 연결**. Codex는 **Codex 설정 열기 → 코딩 → Hook**에서 Perch 훅을 신뢰해요. 목록이 없으면 프로젝트 폴더를 먼저 열어요.
6. 프로젝트에서 “확인만 출력하는 명령을 실행해줘. 파일은 수정하지 마.” 같은 요청 하나를 보내요. 작업함에 새 요청·응답이 보이면 연결을 확인한 거예요. 응답 도착은 테스트·배포 성공이라는 뜻이 아니에요.

Windows는 직접 실행한 개발 세션만 관찰하고 WSL은 지원하지 않아요. 현재 Perch 버전에서 Claude Code 훅을 쓰려면 [Git for Windows](https://gitforwindows.org/)도 설치해 두세요.

## 캐릭터 고르기

캐릭터 우클릭 → **캐릭터 바꾸기** → **설정 → 화면 → 캐릭터 팩**에서 골라요. 젠 카피바라·모찌 냥이·미니멀 고스트·ORB 에디션 4종이 들어 있으니 별도 팩은 필요 없어요.

화면 공유 전에는 **말풍선에 작업 내용 표시**를 끄세요. Perch는 짧은 작업 요약을 이 기기에 보관하고 인터넷으로 보내지 않지만, 내가 AI에게 공유하는 화면·파일에는 해당 AI의 데이터 처리 조건이 적용돼요.

## 막혔을 때

[Mac 문제 해결](RECOVERY.md) · [Windows 문제 해결](RECOVERY-WINDOWS.md). 설정 변경 경고만 남고 새 이벤트가 들어온다면 다시 연결할 필요는 없어요. 기록을 지우려면 **연결 해제 → 원하면 기록 삭제 → 앱 제거** 순서로 진행하세요.

## 기타 자료

[베타 이용 조건](BETA-EVALUATION-RIGHTS.md) · [전체 릴리스](https://github.com/moonweave/perch-releases/releases) · [버그 신고](https://github.com/moonweave/perch-releases/issues). 공개 이슈에는 개인정보나 작업 원문을 올리지 마세요.

확인 기준: v0.1.15 · 2026-10-01. 근거: [공식 릴리스](https://github.com/moonweave/perch-releases/releases/tag/v0.1.15), [Mac 설치 안내](INSTALL.md), [Windows 설치 안내](INSTALL-WINDOWS.md).
