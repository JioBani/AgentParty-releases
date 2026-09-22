# AgentParty

> 여러 AI 코딩 에이전트를 한 화면에서 운영하는 Windows 데스크톱 워크스페이스

[![Latest release](https://img.shields.io/github/v/release/JioBani/AgentParty-releases?display_name=tag&style=flat-square)](https://github.com/JioBani/AgentParty-releases/releases/latest)
[![Windows](https://img.shields.io/badge/platform-Windows-2563eb?style=flat-square&logo=windows11&logoColor=white)](https://github.com/JioBani/AgentParty-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/JioBani/AgentParty-releases/total?style=flat-square)](https://github.com/JioBani/AgentParty-releases/releases)

Claude Code, Codex, Cursor와 여러 모델을 각각의 **멤버**로 실행하고, 하나의 **파티** 안에서 역할을 나눠 동시에 작업하세요. 대화, 승인, 도구 실행과 결과를 오가며 확인할 수 있어 터미널 여러 개를 직접 관리할 필요가 없습니다.

**[최신 버전 다운로드](https://github.com/JioBani/AgentParty-releases/releases/latest)** · **[소스 코드 보기](https://github.com/JioBani/AgentParty-source)**

---

## 이런 작업에 잘 맞습니다

- 구현, 리뷰, 테스트처럼 역할이 다른 에이전트를 동시에 운영할 때
- 긴 작업을 멤버별 대화와 상태로 나눠 한눈에 관리할 때
- 에이전트끼리 메시지를 주고받고 작업을 위임하게 만들 때
- Windows, WSL 또는 등록한 SSH 서버의 작업을 한 앱에서 이어갈 때
- 모델 구독과 API 키 기반 공급자를 한 워크스페이스에서 함께 사용할 때

## 주요 기능

| 기능 | 설명 |
| --- | --- |
| 멀티 에이전트 워크벤치 | 여러 멤버의 대화를 탭과 분할 패널로 나란히 배치합니다. |
| 파티 협업 | 멤버가 서로 메시지를 보내고, 중단하고, 작업을 위임할 수 있습니다. |
| 다양한 실행 환경 | Claude Code, Codex, Cursor 등 지원 CLI를 계정 구독 그대로 연결합니다. |
| Message Gate | 멤버 간 메시지를 전달하기 전에 규칙 기반 검토를 적용할 수 있습니다. |
| 원격 작업 | 로컬 Windows뿐 아니라 WSL과 등록된 SSH 서버에서도 멤버를 실행합니다. |
| 자동화 API | 사용자 기능을 로컬 HTTP API로 제공해 에이전트와 E2E 도구가 앱을 직접 제어합니다. |
| 자동 업데이트 | 설치본은 새 버전을 앱 안에서 확인하고 내려받을 수 있습니다. |

## 시작하기

1. [최신 Releases 페이지](https://github.com/JioBani/AgentParty-releases/releases/latest)를 엽니다.
2. `AgentParty-Setup-<version>.exe`를 내려받아 설치합니다.
3. 앱의 **인증** 메뉴에서 사용할 Claude, Codex, Cursor 또는 API 공급자를 연결합니다.
4. 작업 폴더를 선택하고 파티와 멤버를 만들어 역할을 나눕니다.

현재 배포본은 Windows용입니다. 코드 서명을 적용하기 전까지 Windows SmartScreen이 경고할 수 있으며, 이 경우 **추가 정보 → 실행**을 선택하면 됩니다.

### 설치본과 포터블 버전

| 파일 | 용도 |
| --- | --- |
| `AgentParty-Setup-<version>.exe` | 권장 설치본. 앱 내 자동 업데이트를 지원합니다. |
| `AgentParty-<version>.exe` | 설치 없이 실행하는 포터블 버전. 자동 업데이트는 지원하지 않습니다. |
| `AgentParty-Setup-<version>.exe.blockmap` | 설치본의 차등 업데이트 데이터입니다. |
| `latest.yml` | 앱이 최신 버전과 설치 파일을 확인하는 메타데이터입니다. |

## 모델 카탈로그

AgentParty의 모델 목록은 앱 업데이트와 별도로 갱신됩니다. 새 모델이 공개되면 이 저장소의 `modelCatalog.json`을 통해 기존 설치에서도 받아볼 수 있습니다. 실제 사용 가능 여부는 연결한 계정, 공급자 및 해당 CLI 버전에 따라 달라질 수 있습니다.

## 저장소 안내

이 저장소는 Windows 설치 파일, 포터블 실행 파일, 자동 업데이트 메타데이터와 공개 모델 카탈로그를 제공하는 **배포 전용 저장소**입니다. 애플리케이션 소스는 [AgentParty-source](https://github.com/JioBani/AgentParty-source)에서 확인할 수 있습니다.

문제나 개선 제안은 각 릴리스의 안내 채널 또는 소스 저장소의 이슈를 이용해 주세요.
