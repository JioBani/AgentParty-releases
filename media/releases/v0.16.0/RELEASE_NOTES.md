## 주요 변경

### Jev로 분류와 판정을 바로 요청할 수 있습니다

AgentParty가 보관한 OpenRouter 키로 **Jev Decisions**를 호출하는 로컬 API가 생겼습니다. 공고의 직렬을 고르거나, 특정 경력으로 지원할 수 있는지 판단하거나, 요구 경력 수준을 평가하는 작업에 사용할 수 있습니다. 하나의 자료에 대해 여러 질문을 한 번에 보낼 수 있으며, 결과와 사용량을 구조화된 응답으로 받습니다.

`POST /api/jev/decisions`는 호출할 때마다 Jev에 한 번 요청합니다. 자료를 읽고 여러 건을 처리하는 흐름은 원하는 스크립트에서 구성할 수 있습니다.

### 멤버에게 Jev 도구를 선택적으로 제공합니다

**에이전트 → Message Gate** 화면에서 Jev MCP 도구를 켜고 기본 제공자를 고를 수 있습니다. 멤버는 제공자 목록 확인, 기본 제공자 변경, Jev 판정 요청, 결과를 JSON 파일로 저장하는 도구를 사용할 수 있습니다. 파일 저장 도구는 멤버가 실행되는 컴퓨터의 지정한 절대 경로에 결과를 남깁니다. MCP 도구를 끈 상태에서도 로컬 API와 Message Gate의 Jev 기능은 사용할 수 있습니다.

![에이전트 설정에서 Jev MCP 도구와 기본 제공자를 선택하는 화면](https://raw.githubusercontent.com/JioBani/AgentParty-releases/main/media/releases/v0.16.0/jev-settings.png)

*Jev 도구 공개 여부와 기본 제공자를 설정하는 화면입니다.*

### Message Gate에서 Jev를 별도로 선택합니다

일반 모델 목록과 분리된 **메시지 게이트에 Jev 사용하기** 스위치가 생겼습니다. 파티 전체 또는 개별 멤버의 발신·수신 규칙에 적용하고 Jev 제공자를 선택할 수 있습니다. 심사 결과는 **통과·반려·판정 불가**로 구분됩니다. 판정 불가인 메시지는 전송하며, 그 사실을 기록과 알림에 표시합니다.

![파티 Message Gate에서 Jev와 OpenRouter 제공자를 선택하는 화면](https://raw.githubusercontent.com/JioBani/AgentParty-releases/main/media/releases/v0.16.0/jev-party-gate.png)

*예시 파티의 발신 게이트 설정입니다. 화면의 규칙과 메시지는 테스트용입니다.*

### 사용 비용을 함께 확인할 수 있습니다

직접 요청한 Jev 판정과 Message Gate 심사의 제공자 보고 사용량·비용이 앱의 사용 내역과 합계에 반영됩니다.

## 업데이트 안내

현재 Jev 제공자는 **OpenRouter**입니다. 기존 파티·세션·설정 데이터의 마이그레이션은 필요하지 않습니다. Jev MCP 도구는 기본적으로 꺼져 있으며, 설정을 변경한 뒤 새로 시작하는 멤버 세션부터 도구 목록에 반영됩니다.

## 설치

- 자동 업데이트를 사용하려면 `AgentParty-Setup-0.16.0.exe`를 설치하세요.
- `AgentParty-0.16.0.exe`는 설치 없이 실행하는 포터블 버전이며 자동 업데이트를 지원하지 않습니다.
