# 수노 한국어 작사 스킬 (suno-lyrics-skill) v3.0

Suno로 노래를 만들 때 **부를 수 있는 한국어 가사**와 **Style·Exclude·Title 입력**을 함께 설계하는 Claude 에이전트 스킬입니다.
특정 아티스트나 장르에 맞춘 템플릿이 아닙니다. 사연형 발라드부터 랩·트로트·댄스·R&B·록·재즈·뮤지컬·전자음악까지, 장르에 맞게 규칙을 켜고 끄도록 만든 범용 작사 지침입니다.

- 이 스킬을 바탕으로 쓴 해설 시리즈: https://moket.kr/series/suno-prompt-master

## 들어 있는 것

```
suno-lyrics-skill/
├── SKILL.md                     # 스킬 본문 (§0~§36)
└── templates/
    ├── song-brief.md            # 쓰기 전: Song Brief (§5)
    ├── final-output.md          # 넘길 때: 출력 양식 (§34)
    └── pre-delivery-audit.md    # 넘기기 직전: 납품 전 점검표 (§31)
```

템플릿 세 개는 SKILL.md의 해당 절을 그대로 옮긴 것이라, 스킬 없이 사람이 복사해 써도 됩니다.

## 설치

### Claude.ai (웹·앱)
1. [Releases](../../releases)에서 `suno-lyrics-skill.zip`을 받습니다. zip을 열면 맨 위에 `suno-lyrics-skill` 폴더가 있어야 합니다. 저장소를 받았다면 그 폴더를 직접 zip으로 묶어도 됩니다.
2. 코드 실행(code execution)이 켜져 있어야 합니다. 개인 요금제는 **Settings → Capabilities**의 "Code execution and file creation"에서 켭니다.
3. **Customize → Skills**(https://claude.ai/customize/skills)로 갑니다.
4. **+** 버튼 → **+ Create skill** → **Upload a skill**을 누릅니다.
5. zip 파일을 올립니다.

Pro·Max·Team·Enterprise 요금제에서 쓸 수 있습니다. 출처: [Use Skills in Claude (Claude 도움말)](https://support.claude.com/en/articles/12512180-use-skills-in-claude)

### Claude Code
`suno-lyrics-skill` 폴더를 아래 두 곳 중 한 곳에 복사합니다.

```bash
# 내 모든 프로젝트에서 쓰기
cp -r suno-lyrics-skill ~/.claude/skills/

# 이 프로젝트에서만 쓰기
mkdir -p .claude/skills && cp -r suno-lyrics-skill .claude/skills/
```

설치한 뒤에는 작사를 부탁하면 Claude가 알아서 스킬을 불러옵니다. 이름을 직접 불러도 됩니다: `/suno-lyrics-skill`

## 예시

> 이별 3년 뒤, 옛 동네 버스 정류장에서 문득 그 사람을 떠올리는 노래를 만들고 싶어. 미디엄 템포 발라드, 3분 30초 안쪽. Suno에 넣을 가사랑 Style·Exclude·Title까지 줘.

스킬은 먼저 창작 모드와 Song Brief를 정합니다. 모르는 칸이 있으면 가설을 세워 진행하고, 중요한 가설만 짧게 밝힙니다. 그다음 가사를 쓰고 납품 전 점검을 거친 뒤 출력 양식(Lyrics → Style → Exclude → Title)으로 넘깁니다.

## 라이선스

[CC BY 4.0](LICENSE). 사용·수정·재배포 모두 자유이며, 상업적 이용도 됩니다. 쓰실 때 저작자를 이렇게 표기해 주세요.

> 저작자: **PrevitLAB (MOHOHA)** — https://moket.kr/series/suno-prompt-master

---

## English

**suno-lyrics-skill** is a Claude Agent Skill that helps you write singable Korean lyrics, together with the Style, Exclude and Title fields Suno needs. It is genre-adaptive rather than a template for one artist. It covers ballad, rap, trot, K-pop/dance, R&B, rock, jazz, musical and electronic.

**Install**
- **Claude.ai:** download `suno-lyrics-skill.zip` from Releases. The zip must have the `suno-lyrics-skill` folder at its top level. Make sure code execution is enabled (personal plans: Settings → Capabilities → "Code execution and file creation"). Go to **Customize → Skills** (https://claude.ai/customize/skills), click **+** → **+ Create skill** → **Upload a skill**, then upload the zip. Available on Pro, Max, Team and Enterprise plans. Source: [Use Skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
- **Claude Code:** copy the `suno-lyrics-skill` folder into `~/.claude/skills/` (personal) or `.claude/skills/` (project).

**Example:** "Write a mid-tempo Korean ballad about remembering someone at an old bus stop three years after a breakup, with Suno Style, Exclude and Title."

**Companion series (Korean):** https://moket.kr/series/suno-prompt-master

**License:** [CC BY 4.0](LICENSE). Attribution: **PrevitLAB (MOHOHA)**.
