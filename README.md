# AgentParty — Releases

AgentParty 데스크톱 앱의 **배포 전용** 저장소입니다. 소스 코드는 여기에 없습니다.

## 설치

[Releases](https://github.com/JioBani/AgentParty-releases/releases) 에서 최신
`AgentParty-Setup-<version>.exe` 를 받아 실행하세요.

서명하지 않은 빌드라 Windows SmartScreen 경고가 뜰 수 있습니다 —
**추가 정보 → 실행** 으로 진행하면 됩니다.

설치본으로 한 번 설치해두면, 이후 새 버전은 앱이 직접 알려주고 앱 안에서
받아 설치할 수 있습니다. 포터블 `AgentParty-<version>.exe` 는 설치 없이
실행되지만 자동 업데이트를 지원하지 않습니다.

## 이 저장소에 올라오는 것

| 파일 | 용도 |
| --- | --- |
| `AgentParty-Setup-<version>.exe` | 설치본(NSIS). 자동 업데이트는 이 파일을 받습니다 |
| `AgentParty-Setup-<version>.exe.blockmap` | 차등 다운로드용 |
| `latest.yml` | 앱이 최신 버전을 판별하는 메타데이터 — **없으면 업데이트 확인이 실패합니다** |
| `AgentParty-<version>.exe` | 포터블 실행본 |
