# AI 에이전트 실습 폴더 (강원대 사범대학 교수 특강, 2026.11.12)

이 폴더를 통째로 내려받아 **Claude 데스크톱 앱 → Code 탭 → 폴더 선택**으로 엽니다.
각 하위 폴더의 `CLAUDE.md`가 에이전트가 먼저 읽는 지침입니다.

| 폴더 | 실습 | 도구 |
|---|---|---|
| `01_교육_면담정리/` | 가상 면담 메모를 표·후속 조치·메일 초안으로 정리 | Claude Code |
| `02_연구_브리핑/` | `관심주제.md`를 채우고 최근 논문 브리핑 받기 | Claude Code |
| `03_행정_할일/` | 학교 공지 페이지에서 할 일 표 만들기 | Aside (+Claude 구독 연결) |

## 다른 모델로 할 때
- **ChatGPT 이용권 → OpenAI Codex**: 아래 「부록: Codex로 하기」를 따릅니다.
- **Aside**: `Settings > Models > Providers`에서 ChatGPT 구독, GitHub Copilot, API 키(OpenAI·Google·xAI 등)도 연결할 수 있습니다.
- **일반 채팅만 있을 때**: `CLAUDE.md` 내용과 자료 파일 내용을 함께 붙여 넣고 같은 지시를 보내면 됩니다.

## 넣지 않을 것
학생 이름·학번·성적·실제 면담 내용, 미공개 연구 자료, 공개 범위가 정해지지 않은 학교 내부 문서.

## 부록: Codex로 하기 (ChatGPT 이용권)

Codex는 OpenAI의 에이전트로, 지금은 ChatGPT 데스크톱 앱 안에 들어 있습니다. ChatGPT Free·Go·Plus·Pro·Business·Edu·Enterprise 요금제에 포함되며 요금제마다 쓸 수 있는 양이 다릅니다.

1. **설치**: ChatGPT 데스크톱 앱을 설치합니다. Windows는 Microsoft Store에서 받습니다.
2. **로그인**: ChatGPT 계정으로 로그인합니다.
3. **폴더 열기**: 새 프로젝트를 만들거나 폴더를 열어 `01_교육_면담정리/`처럼 실습 하위 폴더를 고릅니다.
4. **권한**: 입력창 아래 권한을 `Ask for approval`로 둡니다. 작업 폴더 밖의 파일을 고치거나 인터넷을 쓰기 전에 매번 묻는 단계입니다.
5. **지침 파일**: 둘 중 하나를 고릅니다.
   - 폴더의 `CLAUDE.md`를 복사해 `AGENTS.md`로 저장합니다. (권장)
   - 또는 `~/.codex/config.toml`에 다음 한 줄을 넣어 `CLAUDE.md`를 그대로 읽게 합니다.
     ```toml
     project_doc_fallback_filenames = ["CLAUDE.md"]
     ```
6. **지시**: 슬라이드의 실습 지시를 그대로 보냅니다. 결과는 Claude Code 때와 같은 기준으로 확인합니다.

터미널이 익숙하면(macOS·Linux) CLI도 쓸 수 있습니다.
```sh
curl -fsSL https://chatgpt.com/codex/install.sh | sh
cd 01_교육_면담정리
codex   # 처음 실행 때 Sign in with ChatGPT
```

행정 실습(Aside)은 `Settings > Models > Providers > Connect > Subscription`에서 ChatGPT 구독을 연결하면 같은 방법으로 할 수 있습니다.

출처: OpenAI Codex 문서 learn.chatgpt.com/docs (2026.11.4 열람)
