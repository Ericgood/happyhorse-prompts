[![English](https://img.shields.io/badge/English-Switch-blue)](README.md) [![简体中文](https://img.shields.io/badge/简体中文-切换-blue)](README_zh.md) [![日本語](https://img.shields.io/badge/日本語-切替-blue)](README_ja.md) [![Español](https://img.shields.io/badge/Español-Cambiar-blue)](README_es.md)

<div align="center">
  <img src="assets/logo.png" alt="HappyHorse Logo" width="200">

  # 🐴 HappyHorse 프롬프트 모음

  **[HappyHorse](https://happyhorses.io) AI 동영상 생성 프롬프트 커뮤니티 큐레이션 컬렉션**

  [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
  [![GitHub stars](https://img.shields.io/github/stars/Ericgood/happyhorse-prompt?style=social)](https://github.com/Ericgood/happyhorse-prompt)
  [![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
  [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/Ericgood/happyhorse-prompt/pulls)

</div>

---

> **참고:** 이것은 커뮤니티 주도 프로젝트입니다. 저작권을 침해하는 콘텐츠를 발견하시면 [Issue를 생성](https://github.com/Ericgood/happyhorse-prompt/issues)해 주세요.

## 🐴 HappyHorse란?

**HappyHorse-1.0**은 텍스트에서 동영상과 오디오를 동시에 생성하는 150억 파라미터 통합 Transformer 모델입니다. 후처리 더빙이 필요 없습니다. 2026년 4월 초 [Artificial Analysis](https://artificialanalysis.ai/) Video Arena 리더보드에 익명으로 등장하여 Seedance 2.0, Kling 3.0, PixVerse V6 등 기존 모델을 제치고 **1위**를 차지했습니다.

### 주요 특징

- 🏆 **AI Video Arena 1위** — Elo 1333 (텍스트→동영상), Elo 1392 (이미지→동영상)
- 🧠 **150억 파라미터** — 40층 단일 스트림 Transformer, 크로스 어텐션 없음
- 🎬 **동영상 + 오디오 동시 생성** — 대화, 환경음, 폴리를 동영상 프레임과 함께 생성
- 🗣️ **다국어 립싱크** — 중국어, 영어, 일본어, 한국어, 독일어, 프랑스어, 광둥어
- ⚡ **8단계 디노이징** — DMD-2 증류를 통한 빠른 추론, CFG 불필요
- 📖 **오픈 소스** — 기본 모델, 증류 모델, 초해상도 모듈, 추론 코드 (상업적 사용 허가 포함)

### 아키텍처

**단일 스트림 셀프 어텐션 Transformer**를 사용합니다. 텍스트 토큰, 참조 이미지 잠재 표현, 노이즈가 있는 동영상/오디오 토큰을 하나의 시퀀스에서 동시에 디노이즈합니다. 처음과 마지막 4개 레이어는 모달리티별 프로젝션을 사용하고, 중간 32개 레이어는 모든 모달리티에서 파라미터를 공유합니다.

> *"오픈 소스 커뮤니티에서 처음부터 진정한 오디오-비디오 동시 사전 학습을 한 사람은 아무도 없었습니다."*
>
> — [36Kr HappyHorse 보고서](https://eu.36kr.com/en/p/3757826958635781)

### 리더보드 순위

| 카테고리 | Elo 점수 | 순위 |
|:---|:---:|:---:|
| 텍스트→동영상 (오디오 없음) | **1333** | 🥇 1위 |
| 이미지→동영상 (오디오 없음) | **1392** | 🥇 1위 |
| 텍스트→동영상 (오디오 포함) | 1205 | 🥈 2위 |
| 이미지→동영상 (오디오 포함) | 1161 | 🥈 2위 |

*데이터 출처: [Artificial Analysis Video Arena](https://artificialanalysis.ai/), 2026년 4월*

### 경쟁 비교

| 모델 | T2V Elo | 비고 |
|:---|:---:|:---|
| **HappyHorse-1.0** | **1333** | 오픈 소스, 오디오-비디오 동시 생성 |
| Seedance 2.0 (720p) | 1273 | ByteDance, 오디오 동기화 우위 |
| SkyReels V4 | 1244 | $7.20/분 |
| Kling 3.0 1080p Pro | 1241 | $13.44/분 |
| PixVerse V6 | 1239 | $5.40/분 |

### 미스터리

HappyHorse-1.0의 개발자는 공식적으로 확인되지 않았습니다. Artificial Analysis는 이를 **"익명" 모델**로 설명했습니다. 커뮤니티 조사에 따르면, 오픈 소스 [daVinci-MagiHuman](https://github.com/BrightXiaoHan/MagiHuman) 모델을 기반으로 한 반복 최적화이며, Sand.ai와 상하이 GAIR 연구소와 관련이 있을 수 있습니다. 이름은 2026년이 중국 십이지에서 **말의 해**인 것과 일치합니다.

> *출처: [36Kr](https://eu.36kr.com/en/p/3757826958635781) · [WaveSpeed AI](https://wavespeed.ai/blog/posts/what-is-happyhorse-1-0-ai-video-model/) · [Apiyi 분석](https://help.apiyi.com/en/happyhorse-model-mystery-ai-video-lmarena-analysis-en.html)*

---

## 📊 통계

| 총 프롬프트 | 추천 | 최종 업데이트 |
|:---:|:---:|:---:|
| 5 | 5 | 2026년 4월 |

---

## 🏆 공식 데모 — HappyHorse로 생성

이 프롬프트들은 HappyHorse의 능력을 보여주는 공식 데모입니다: 물리 인식 모션, 유체 역학, 캐릭터 애니메이션, 시간적 일관성, 동기화 오디오 생성.

---

### 1. 🎯 훌라후프 아이

![추천](https://img.shields.io/badge/⭐_추천-공식_데모-FF4D00)

> 물리 인식 모션 — 후프가 허리에서 가슴으로 올라가고, 무릎으로 내려가고, 바닥에 떨어짐. 현실적인 무게감과 운동량.

#### 📝 프롬프트

```
A hula hoop spinning on a kid's waist, gradually climbing to their chest, then dropping
to knees, then clattering to the floor. They pick it up to try again.
```

<div align="center">
  <a href="videos/hula-hoop-kid.mp4">
    <img src="assets/thumbnails/hula-hoop-kid.jpg" width="700" alt="훌라후프 아이 - 미리보기">
  </a>
  <br>
  <a href="videos/hula-hoop-kid.mp4">📥 동영상 다운로드</a> ・ <a href="https://x.com/i/status/2041591993386856448">🐦 소스</a>
</div>

---

### 2. ⛳ 골프공 퍼팅

![추천](https://img.shields.io/badge/⭐_추천-공식_데모-FF4D00)

> 캐릭터 감정과 물리의 동기화 — 골퍼의 바디 랭귀지가 공의 각 회전에 맞춰 변화.

#### 📝 프롬프트

```
A golf ball in a cup rolling around the rim three times before finally dropping in.
The golfer's body language matches each rotation. Audio: Ball rattle, exhale, plop.
```

<div align="center">
  <a href="videos/golf-ball-putt.mp4">
    <img src="assets/thumbnails/golf-ball-putt.jpg" width="700" alt="골프공 퍼팅 - 미리보기">
  </a>
  <br>
  <a href="videos/golf-ball-putt.mp4">📥 동영상 다운로드</a> ・ <a href="https://x.com/i/status/2041591995106521352">🐦 소스</a>
</div>

---

### 3. 🐱 고양이와 토스터 반사

![추천](https://img.shields.io/badge/⭐_추천-공식_데모-FF4D00)

> 반사 렌더링 + 동물 애니메이션 — 고양이가 크롬 토스터 표면을 두드리면 왜곡된 반사가 되돌려 두드림.

#### 📝 프롬프트

```
A cat staring at its own reflection in a toaster, paw tapping the chrome surface.
The distorted cat reflection taps back. Audio: Paw taps, confused meow.
```

<div align="center">
  <a href="videos/cat-toaster-reflection.mp4">
    <img src="assets/thumbnails/cat-toaster-reflection.jpg" width="700" alt="고양이와 토스터 - 미리보기">
  </a>
  <br>
  <a href="videos/cat-toaster-reflection.mp4">📥 동영상 다운로드</a> ・ <a href="https://x.com/i/status/2041591996754903188">🐦 소스</a>
</div>

---

### 4. ☕ 바리스타 라떼 아트

![추천](https://img.shields.io/badge/⭐_추천-공식_데모-FF4D00)

> 유체 역학의 걸작 — 우유가 크레마 아래로 가라앉고, 표면을 뚫고 나와 정밀한 손목 움직임으로 로제타 패턴을 형성.

#### 📝 프롬프트

```
A barista creating latte art by pouring steamed milk into espresso. The white milk
submerges beneath the brown crema initially, then breaks through the surface as the
cup fills. The barista's wrist makes precise oscillating movements, creating a rosetta
pattern. The milk and espresso maintain their distinct colors while interacting at
the boundary. Audio: The gentle pour of liquid, the hiss of the steam wand in the
background.
```

<div align="center">
  <a href="videos/barista-latte-art.mp4">
    <img src="assets/thumbnails/barista-latte-art.jpg" width="700" alt="바리스타 라떼 아트 - 미리보기">
  </a>
  <br>
  <a href="videos/barista-latte-art.mp4">📥 동영상 다운로드</a> ・ <a href="https://x.com/i/status/2041591999061758171">🐦 소스</a>
</div>

---

### 5. 🌸 꽃의 개화와 시듦 타임랩스

![추천](https://img.shields.io/badge/⭐_추천-공식_데모-FF4D00)

> 2주에 걸친 시간적 일관성 — 같은 꽃병, 같은 창문, 같은 각도. 빛은 날씨에 따라 자연스럽게 변화.

#### 📝 프롬프트

```
A flower blooming and wilting over two weeks, one photo per day. Same vase, same window,
same angle. Light changes with weather. Audio: Quiet domestic.
```

<div align="center">
  <a href="videos/flower-bloom-timelapse.mp4">
    <img src="assets/thumbnails/flower-bloom-timelapse.jpg" width="700" alt="꽃 타임랩스 - 미리보기">
  </a>
  <br>
  <a href="videos/flower-bloom-timelapse.mp4">📥 동영상 다운로드</a> ・ <a href="https://x.com/i/status/2039462980715524457">🐦 소스</a>
</div>

---

## 🤝 기여 방법

프롬프트 기여를 환영합니다!

### Pull Request로 제출

1. 이 저장소를 **Fork**
2. **프롬프트 추가** — 적절한 `prompts/<category>/` 폴더에 Markdown 파일 생성
3. **PR 제출** — 리뷰 후 병합합니다!

### Issue로 제출

PR이 번거로우신가요? [Issue를 생성](https://github.com/Ericgood/happyhorse-prompt/issues/new)하고 프롬프트를 첨부하면 저희가 추가합니다!

### 가이드라인

- ✅ 원본이거나 공유 허가를 받은 프롬프트
- ✅ 사용 모델 명시 (예: HappyHorse)
- ✅ 예상 출력 설명 추가
- ✅ 동영상/이미지 미리보기 강력 권장
- ❌ NSFW 콘텐츠 금지
- ❌ 저작권 캐릭터 복제 금지

## 📜 라이선스

이 프로젝트는 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) 라이선스로 공개됩니다. 적절한 크레딧을 표시하면 자유롭게 공유하고 수정할 수 있습니다.

## 🌐 링크

- 🐴 [HappyHorse 공식 웹사이트](https://happyhorses.io)
- 📰 [36Kr: HappyHorse 심층 분석](https://eu.36kr.com/en/p/3757826958635781)
- 📊 [Artificial Analysis Video Arena](https://artificialanalysis.ai/)
- 💬 [토론](https://github.com/Ericgood/happyhorse-prompt/discussions)
- 🐛 [문제 신고](https://github.com/Ericgood/happyhorse-prompt/issues)

---

<div align="center">

**유용하셨다면 ⭐를 눌러주세요!**

HappyHorse 커뮤니티가 ❤️를 담아 제작

</div>
