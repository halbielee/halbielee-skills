# halbielee-skills

Claude Code용 개인 Skills 모음.  
AI가 작성한 코드를 효율적으로 리뷰하고, 제조 AI/ML 워크플로우를 지원하는 스킬들.

## 설치

### Plugin Marketplace (추천)

```bash
# Claude Code에서 최초 1회 — marketplace 등록
/plugin marketplace add halbielee/halbielee-skills

# 개별 skill 설치
/plugin install code-review@halbielee-skills
```

### 수동 설치

```bash
git clone https://github.com/halbielee/halbielee-skills.git
cp -r halbielee-skills/skills/code-review ~/.claude/skills/
```

## Skills

| Skill | 설명 | 버전 |
|---|---|---|
| **code-review** | AI 생성 코드 리뷰 & 이해 워크플로우 (Understand → Feedback → Plan) | v0.1 |

## Marketplace 구조

```
halbielee-skills/
├── .claude-plugin/
│   └── marketplace.json      ← marketplace 메타데이터
├── code-review/
│   └── .claude-plugin/
│       └── plugin.json       ← 플러그인 메타데이터
│   └── skills/
│       └── code-review/
│           └── SKILL.md
└── README.md
```

각 플러그인은 독립 디렉토리에 자체 `.claude-plugin/plugin.json`과 `skills/` 폴더를 가진다.

## 새 Plugin 추가

```bash
mkdir -p new-plugin/.claude-plugin new-plugin/skills/new-plugin
# new-plugin/.claude-plugin/plugin.json 작성
# new-plugin/skills/new-plugin/SKILL.md 작성
# .claude-plugin/marketplace.json의 plugins 배열에 추가
```

## License

MIT
