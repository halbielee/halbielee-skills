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

## Skill 구조

```
skills/
└── code-review/
    └── SKILL.md
```

각 skill은 `skills/<name>/SKILL.md`에 위치. 필요시 `scripts/`, `references/`, `assets/` 추가 가능.

## 새 Skill 추가

```bash
mkdir skills/new-skill-name
# skills/new-skill-name/SKILL.md 작성 후 push
```

## License

MIT
