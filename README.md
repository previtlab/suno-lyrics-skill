<p align="center">
  <img src="assets/banner.png" alt="suno-lyrics-skill — 부를 수 있는 한국어 가사를 쓰는 Claude 에이전트 스킬" width="100%">
</p>

<p align="center">
  <b>Suno에 넣을 부를 수 있는 한국어 가사와 Style·Exclude·Title을 함께 설계하는 Claude 에이전트 스킬</b>
</p>

<p align="center">
  <a href="https://github.com/previtlab/suno-lyrics-skill/releases/latest"><img src="https://img.shields.io/github/v/release/previtlab/suno-lyrics-skill?label=version" alt="version"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-CC%20BY%204.0-lightgrey" alt="license CC BY 4.0"></a>
</p>

<p align="center">
  <a href="#설치">설치</a> ·
  <a href="#예시">예시</a> ·
  <a href="#강의로-배우기">강의 영상</a> ·
  <a href="#이-스킬로-만든-노래">이 스킬로 만든 노래</a> ·
  <a href="#english">English</a>
</p>

특정 아티스트나 장르에 맞춘 템플릿이 아닙니다. 사연형 발라드부터 랩·트로트·댄스·R&B·록·재즈·뮤지컬·전자음악까지, 장르에 맞게 규칙을 켜고 끄도록 만든 범용 작사 지침입니다.

## 설치

**Claude.ai (웹·앱)**
1. [Releases](../../releases)에서 `suno-lyrics-skill.zip`을 받습니다.
2. **Customize → Skills**([claude.ai/customize/skills](https://claude.ai/customize/skills))에서 **+** → **+ Create skill** → **Upload a skill**을 누릅니다.
3. zip 파일을 올립니다.

**Claude Code**

```bash
cp -r suno-lyrics-skill ~/.claude/skills/
```

플러그인으로 받으려면 Claude Code에서 `/plugin marketplace add previtlab/suno-lyrics-skill` → `/plugin install suno-lyrics-skill@previtlab-suno`. 다른 에이전트 도구에서는 `npx skills add previtlab/suno-lyrics-skill`.

<details>
<summary>설치 자세히 보기 (코드 실행 설정·요금제·프로젝트 전용 설치)</summary>

### Claude.ai (웹·앱)
1. [Releases](../../releases)에서 `suno-lyrics-skill.zip`을 받습니다. zip을 열면 맨 위에 `suno-lyrics-skill` 폴더가 있어야 합니다. 저장소를 받았다면 그 폴더를 직접 zip으로 묶어도 됩니다.
2. 코드 실행(code execution)이 켜져 있어야 합니다. 개인 요금제는 **Settings → Capabilities**의 "Code execution and file creation"에서 켭니다.
3. **Customize → Skills**([claude.ai/customize/skills](https://claude.ai/customize/skills))로 갑니다.
4. **+** 버튼 → **+ Create skill** → **Upload a skill**을 누릅니다.
5. zip 파일을 올립니다.

Free·Pro·Max·Team·Enterprise 요금제에서 쓸 수 있습니다. Team·Enterprise는 조직 설정(**Organization settings → Plugins & skills**)에서 스킬이 켜져 있어야 합니다(조직 소유자가 관리). 출처: [Use Skills in Claude (Claude 도움말)](https://support.claude.com/en/articles/12512180-use-skills-in-claude)

### Claude Code
`suno-lyrics-skill` 폴더를 아래 두 곳 중 한 곳에 복사합니다.

```bash
# 내 모든 프로젝트에서 쓰기
cp -r suno-lyrics-skill ~/.claude/skills/

# 이 프로젝트에서만 쓰기
mkdir -p .claude/skills && cp -r suno-lyrics-skill .claude/skills/
```

설치한 뒤에는 작사를 부탁하면 Claude가 알아서 스킬을 불러옵니다. 이름을 직접 불러도 됩니다: `/suno-lyrics-skill`

</details>

## 예시

요청 한 줄:

> 이별 3년 뒤, 옛 동네 버스 정류장에서 문득 그 사람을 떠올리는 노래를 만들고 싶어. 미디엄 템포 발라드, 3분 30초 안쪽. Suno에 넣을 가사랑 Style·Exclude·Title까지 줘.

스킬이 실제로 돌려준 출력 일부:

```
[Chorus]
한 대만 더 보내고 가자
네가 늘 하던 말
문 열리고 닫히는 동안
우린 웃기만 했지
한 대만 더, 또 한 대만
오늘은 나 혼자 보내
```

```
Style
Korean medium-tempo ballad, 80 BPM, 4/4, warm upright piano and soft brushed drums,
clean electric guitar arpeggios, gentle bass, sparse intimate verses, chorus opens up
but stays restrained, light strings enter only in final chorus, warm mid-range vocal,
conversational diction, soft breathy tone, minimal vibrato, close-mic dry verses,
natural room reverb

Exclude
(첫 생성은 비워 두기를 권합니다)

Title
한 대만 더
```

스킬은 먼저 창작 모드와 Song Brief를 정합니다. 모르는 칸이 있으면 가설을 세워 진행하고, 중요한 가설만 짧게 밝힙니다. 그다음 가사를 쓰고 납품 전 점검을 거친 뒤 출력 양식(Lyrics → Style → Exclude → Title)으로 넘깁니다. 생성 결과에서 확인할 점도 함께 적어 줍니다.

## 이 스킬로 만든 노래

MOHOHA 채널에 올린 곡들입니다. 곡마다 가사가 어디서 시작했는지 한 줄씩 적었습니다. → [MOHOHA 유튜브 채널](https://www.youtube.com/@mohohamusic)

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://youtu.be/O0557LkaykY"><img src="https://img.youtube.com/vi/O0557LkaykY/maxresdefault.jpg" alt="취향은 왜 숨겨야 하나요" width="100%"></a><br>
      <b><a href="https://youtu.be/O0557LkaykY">취향은 왜 숨겨야 하나요</a></b> · 인디 록<br>
      덕질하다가 떠올라서 만든 곡입니다. 빠른 곡인데 줄을 짧게 끊어 숨 쉴 자리를 남겼습니다.
    </td>
    <td width="50%" valign="top">
      <a href="https://youtu.be/a66VUcNSmpM"><img src="https://img.youtube.com/vi/a66VUcNSmpM/maxresdefault.jpg" alt="Swipe tap" width="100%"></a><br>
      <b><a href="https://youtu.be/a66VUcNSmpM">Swipe tap</a></b> · K-POP / R&B<br>
      훅에서 시작: 쇼츠를 넘기던 손가락 움직임을 보다가 'Swipe tap' 두 단어가 먼저 떠올랐고, 그게 곡을 여는 반복이 됐습니다.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <a href="https://youtu.be/xUNtJR5DD5w"><img src="https://img.youtube.com/vi/xUNtJR5DD5w/maxresdefault.jpg" alt="냥냥 어퍼컷" width="100%"></a><br>
      <b><a href="https://youtu.be/xUNtJR5DD5w">냥냥 어퍼컷</a></b> · K-POP<br>
      캐릭터로 시작: 고양이 화자의 말투 '어디서 반말이냐구' 하나로 곡이 이어집니다.
    </td>
    <td width="50%" valign="top">
      <a href="https://youtu.be/2AFnZ79EVZM"><img src="https://img.youtube.com/vi/2AFnZ79EVZM/maxresdefault.jpg" alt="종로 밤거리" width="100%"></a><br>
      <b><a href="https://youtu.be/2AFnZ79EVZM">종로 밤거리</a></b> · 인디 록<br>
      사연에서 시작: 종로 고시원에서 침대 쪽 기둥 때문에 늘 다리를 구부리고 자던 경험이 '기둥이 침대를 반쯤 먹어서'가 됐습니다.
    </td>
  </tr>
</table>

## 강의로 배우기

이 스킬의 규칙을 한 편씩 풀어 쓴 강의 시리즈입니다.

- 📖 강의 글: [SUNO 작사의 모든 것](https://moket.kr/series/suno-lyrics-complete)
- ▶️ 0강 영상: [내 노래는 왜 이상할까? 수노로 돈 버는 작사법, 스킬까지 무료로 드려요](https://youtu.be/WdfmKrI3t0A) (모켓 Moket 채널)
- ▶️ 1강 영상: [Suno 가사, 습관처럼 사연부터 쓰면 어색해져요](https://youtu.be/w2twWvVdYRY) — 시작점 고르기: 말이 주인공 / 소리가 주인공 (모켓 Moket 채널)

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

## 라이선스

[CC BY 4.0](LICENSE). 사용·수정·재배포 모두 자유이며, 상업적 이용도 됩니다. 쓰실 때 저작자를 이렇게 표기해 주세요.

> 저작자: **PrevitLAB (MOKET)** — https://moket.kr/series/suno-lyrics-complete

---

## English

**suno-lyrics-skill** is a Claude Agent Skill that helps you write singable Korean lyrics, together with the Style, Exclude and Title fields Suno needs. It is genre-adaptive rather than a template for one artist. It covers ballad, rap, trot, K-pop/dance, R&B, rock, jazz, musical and electronic.

**Install**
- **Claude.ai:** download `suno-lyrics-skill.zip` from [Releases](../../releases), go to **Customize → Skills** (https://claude.ai/customize/skills), click **+** → **+ Create skill** → **Upload a skill**, and upload the zip.
- **Claude Code:** `cp -r suno-lyrics-skill ~/.claude/skills/`
  - as a plugin: `/plugin marketplace add previtlab/suno-lyrics-skill`, then `/plugin install suno-lyrics-skill@previtlab-suno`
  - other agents: `npx skills add previtlab/suno-lyrics-skill`

<details>
<summary>Install details</summary>

- **Claude.ai:** The zip must have the `suno-lyrics-skill` folder at its top level. Make sure code execution is enabled (personal plans: Settings → Capabilities → "Code execution and file creation"). Available on Free, Pro, Max, Team and Enterprise plans. On Team and Enterprise, skills must be enabled in **Organization settings → Plugins & skills** (managed by the organization owner). Source: [Use Skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
- **Claude Code:** copy the `suno-lyrics-skill` folder into `~/.claude/skills/` (personal) or `.claude/skills/` (project).

</details>

**Example:** "Write a mid-tempo Korean ballad about remembering someone at an old bus stop three years after a breakup, with Suno Style, Exclude and Title." The skill returns the full lyrics (chorus hook: 한 대만 더 보내고 가자, "let's let one more bus go"), a Style prompt such as `Korean medium-tempo ballad, 80 BPM, 4/4, warm upright piano and soft brushed drums, …`, an Exclude suggestion and the Title 한 대만 더, plus what to listen for in the generated song.

**Songs made with this skill:** [취향은 왜 숨겨야 하나요](https://youtu.be/O0557LkaykY) (indie rock, from fandom) · [Swipe tap](https://youtu.be/a66VUcNSmpM) (K-pop/R&B, hook-first: the two words came first) · [냥냥 어퍼컷](https://youtu.be/xUNtJR5DD5w) (K-pop, character-first) · [종로 밤거리](https://youtu.be/2AFnZ79EVZM) (indie rock, story-first) — [MOHOHA on YouTube](https://www.youtube.com/@mohohamusic)

**Learn (Korean):** [lecture series](https://moket.kr/series/suno-lyrics-complete) · [episode 0 video](https://youtu.be/WdfmKrI3t0A) · [episode 1 video](https://youtu.be/w2twWvVdYRY)

**License:** [CC BY 4.0](LICENSE). Attribution: **PrevitLAB (MOHOHA)**.
