# Perch 시작하기

## 내 기기에 맞는 버튼 하나만 누르세요

**[Mac 설치 파일 받기](https://github.com/moonweave/perch-releases/releases/download/v0.1.18/Perch-0.1.18-macOS-universal.dmg)** · **[Windows 설치 파일 받기](https://github.com/moonweave/perch-releases/releases/download/v0.1.18/Perch-0.1.18-windows-x64-setup.exe)**

Mac은 macOS 14 이상(Intel·Apple Silicon), Windows는 Windows 11 x64용이에요. 설치에는 내 기기에 맞는 설치 파일 하나면 돼요. `.sha256` 파일은 원할 때 파일이 바뀌지 않았는지 확인하는 용도예요. Source code 압축 파일과 문서·고지 파일은 설치할 필요가 없어요.

순서는 **다운로드 → 설치 → Perch에서 연결 → 첫 알림 확인**이에요. 설치 파일을 확인하고 싶다면 체크섬 비교를 추가하면 돼요. Codex나 Claude Code는 먼저 설치되어 있어야 해요. 일반 Claude 채팅이 아니라 이 기기에서 실행하는 개발 세션을 관찰해요. Perch는 무료이고 Codex·Claude 이용 조건과 비용은 별개예요.

## 명령어가 낯설면 AI와 같이 설치해요

화면에 뜬 안내를 이미 쓰는 Codex나 Claude에 보여 주고 다음 클릭을 물어보세요. 설치 파일 확인도 부탁하려면 AI가 실제 파일을 읽고 비교할 수 있어야 해요. 그게 안 되는 환경이면 파일을 확인했다고 말하지 말고 직접 하는 방법을 안내해 달라고 요청하세요. 새 유료 도구를 살 필요는 없지만 AI 사용량은 소모될 수 있어요.

- 설치나 설정을 바꾸기 전에는 AI가 먼저 어떤 변경인지 설명하도록 해요. 보안 경고 허용, Codex 훅 신뢰, 연결 설정은 내용을 확인한 뒤 직접 결정하세요.

화면을 공유할 때는 계정 정보, 경로, 요청·응답 내용부터 가려 주세요.

```text
Perch 무료 베타 설치를 도와줘. 터미널과 PowerShell은 낯설어.
공식 안내: https://github.com/moonweave/perch-releases/blob/main/START-HERE.md
공식 파일: https://github.com/moonweave/perch-releases/releases/tag/v0.1.18

내 운영체제부터 확인하고 맞는 설치 파일 하나를 골라줘.
설치 파일을 확인하고 싶다면 같은 릴리스의 체크섬과 실제 파일을 비교해. 파일을 읽거나 명령을 실행할 수 없는 환경이면 확인했다고 말하지 말고 내가 직접 할 순서를 알려줘.
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

1. 위의 내 기기용 설치 파일을 받아요. 원하면 같은 릴리스에서 체크섬 파일도 받아요: [Mac 체크섬](https://github.com/moonweave/perch-releases/releases/download/v0.1.18/Perch-0.1.18-macOS-universal.dmg.sha256) · [Windows 체크섬](https://github.com/moonweave/perch-releases/releases/download/v0.1.18/Perch-0.1.18-windows-x64-setup.exe.sha256).
2. 필요하면 [Mac 상세 안내](INSTALL.md#2-파일-확인) / [Windows 상세 안내](INSTALL-WINDOWS.md#2-파일-확인)에 따라 파일을 확인해요. 체크섬은 파일이 바뀌었는지 확인할 뿐 게시자를 인증하지 않아요.
3. Mac은 DMG를 열고 Perch를 Applications로 옮겨요. Windows는 설치 파일을 열어 현재 계정에 설치해요.
4. 현재 베타는 macOS Developer ID 서명·공증과 Windows 코드 서명이 없어 운영체제 경고가 나올 수 있어요. 공식 릴리스에서 받은 파일인지 확인하고, 계속할지 직접 판단하세요. Smart App Control이나 관리 정책이 차단하면 멈춰요. 보안 기능을 끄지 마세요.
5. Perch를 열고 **설정 → 연결 → 훅 연결 → 허용하고 연결**. Codex는 **Codex 설정 열기 → 코딩 → Hook**에서 Perch 훅을 신뢰해요. 목록이 없으면 프로젝트 폴더를 먼저 열어요.
6. 프로젝트에서 “확인만 출력하는 명령을 실행해줘. 파일은 수정하지 마.” 같은 요청 하나를 보내요. 작업함에 새 요청·응답이 보이면 연결을 확인한 거예요. 응답 도착은 테스트·배포 성공이라는 뜻이 아니에요.

Windows는 직접 실행한 개발 세션만 관찰하고 WSL은 지원하지 않아요. Windows에서 Claude Code를 쓰려면 [Git for Windows](https://gitforwindows.org/)도 설치해 두세요.

## 캐릭터 고르기

캐릭터 우클릭 → **캐릭터 바꾸기** → **설정 → 화면 → 캐릭터 팩**에서 골라요. 젠 카피바라·모찌 냥이·미니멀 고스트·ORB 에디션 4종이 들어 있으니 별도 팩은 필요 없어요.

화면 공유 전에는 **말풍선에 작업 내용 표시**를 끄세요. Perch는 짧은 작업 요약을 이 기기에 보관하고 인터넷으로 보내지 않지만, 내가 AI에게 공유하는 화면·파일에는 해당 AI의 데이터 처리 조건이 적용돼요.

## 막혔을 때

[Mac 문제 해결](RECOVERY.md) · [Windows 문제 해결](RECOVERY-WINDOWS.md). 설정 변경 경고만 남고 새 이벤트가 들어온다면 다시 연결할 필요는 없어요. 기록을 지우려면 **연결 해제 → 원하면 기록 삭제 → 앱 제거** 순서로 진행하세요.

## 기타 자료

[베타 이용 조건](BETA-EVALUATION-RIGHTS.md) · [전체 릴리스](https://github.com/moonweave/perch-releases/releases) · [버그 신고](https://github.com/moonweave/perch-releases/issues). 공개 이슈에는 개인정보나 작업 원문을 올리지 마세요.

확인 기준: v0.1.18 · 2026-10-02. 근거: [공식 릴리스](https://github.com/moonweave/perch-releases/releases/tag/v0.1.18), [Mac 설치 안내](INSTALL.md), [Windows 설치 안내](INSTALL-WINDOWS.md).
