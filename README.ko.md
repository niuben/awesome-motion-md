# awesome-motion.md

![awesome-motion.md animated logo](asset/logo-motion.svg)

AI Agent가 시각적으로 인상적이고 지루하지 않은 UI 애니메이션을 생성하도록 돕는 `MOTION.md` 파일 큐레이션 모음입니다.

[English](README.md) | [中文版](README.zh-CN.md) | [日本語](README.ja.md) | [العربية](README.ar.md)

## 미리보기 갤러리

각 미리보기는 동일한 UI 요소를 사용하지만, 시각 스타일과 모션 동작은 각각의 `MOTION.md`를 기반으로 생성됩니다.

<table width="100%">
  <tr><td width="100%"><strong>Material Expressive</strong><br /><img src="asset/previews/material-expressive.gif" alt="Material Expressive preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Apple Fluid</strong><br /><img src="asset/previews/apple-fluid.gif" alt="Apple Fluid preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Fluent Productive</strong><br /><img src="asset/previews/fluent-productive.gif" alt="Fluent Productive preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Carbon Enterprise</strong><br /><img src="asset/previews/carbon-enterprise.gif" alt="Carbon Enterprise preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Linear Snappy</strong><br /><img src="asset/previews/linear-snappy.gif" alt="Linear Snappy preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Stripe Polished</strong><br /><img src="asset/previews/stripe-polished.gif" alt="Stripe Polished preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Vercel Minimal</strong><br /><img src="asset/previews/vercel-minimal.gif" alt="Vercel Minimal preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Framer Spring</strong><br /><img src="asset/previews/framer-spring.gif" alt="Framer Spring preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>GSAP Cinematic</strong><br /><img src="asset/previews/gsap-cinematic.gif" alt="GSAP Cinematic preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Game Impact</strong><br /><img src="asset/previews/game-impact.gif" alt="Game Impact preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Glitch Cyberpunk</strong><br /><img src="asset/previews/glitch-cyberpunk.gif" alt="Glitch Cyberpunk preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Editorial Scroll</strong><br /><img src="asset/previews/editorial-scroll.gif" alt="Editorial Scroll preview" width="100%" /></td></tr>
</table>

## 이 프로젝트는 무엇인가요?

`MOTION.md`는 Cursor, Claude Code, OpenCode 같은 AI 코딩 Agent를 위한 모션 디자인 룰북입니다.

AI에게 단순히 “애니메이션을 넣어줘”라고 요청해 평범한 fade 효과를 받는 대신, easing curve, duration token, entrance animation, hover state, scroll-triggered behavior, exit transition, accessibility rule, anti-pattern까지 포함한 구체적인 모션 명세를 제공합니다.

## 프로젝트 구조

```txt
awesome-motion-md/
├── asset/                # 데모 GIF와 시각 자료
├── motion-md/            # 모션 스타일 룰북
├── docs/                 # 가이드와 예제
├── README.md             # 영어 README
├── README.zh-CN.md       # 중국어 README
├── README.ja.md          # 일본어 README
├── README.ko.md          # 한국어 README
└── README.ar.md          # 아랍어 README
```

## 모션 스타일

모션 스타일은 `motion-md/`에 있으며, 각 스타일은 독립적인 완전한 `MOTION.md` 룰북입니다.

사용 가능한 스타일:

```txt
motion-md/
├── material-expressive/MOTION.md
├── apple-fluid/MOTION.md
├── fluent-productive/MOTION.md
├── carbon-enterprise/MOTION.md
├── linear-snappy/MOTION.md
├── stripe-polished/MOTION.md
├── vercel-minimal/MOTION.md
├── framer-spring/MOTION.md
├── gsap-cinematic/MOTION.md
├── game-impact/MOTION.md
├── glitch-cyberpunk/MOTION.md
└── editorial-scroll/MOTION.md
```

| 스타일 | 설명 |
| --- | --- |
| `material-expressive` | Material Design의 expressive spring system을 기반으로 한 물리감 있는 모션 스타일. |
| `apple-fluid` | Apple의 공간적이고 직접 조작적인 느낌에서 영감을 받은 차분하고 연속적인 프리미엄 모션. |
| `fluent-productive` | 생산성 인터페이스를 위한 빠르고 기능적이며 계층이 명확한 모션. |
| `carbon-enterprise` | 복잡한 엔터프라이즈 제품에 적합한 정확하고 접근성 높은 모션. |
| `linear-snappy` | 작은 이동 거리와 명확한 상태 변화를 가진 초고속 SaaS 모션. |
| `stripe-polished` | 깊이감, stagger, 상업적 완성도를 강조하는 랜딩 페이지용 세련된 모션. |
| `vercel-minimal` | 다크 UI와 섬세한 피드백에 어울리는 절제된 개발자 도구 모션. |
| `framer-spring` | spring, gesture, layout animation을 중심으로 한 모션 패턴. |
| `gsap-cinematic` | 강한 임팩트의 마케팅 페이지를 위한 timeline 기반 시네마틱 모션. |
| `game-impact` | anticipation, impact, reward 효과를 포함한 게임형 피드백 모션. |
| `glitch-cyberpunk` | 접근성 제한을 포함한 neon, scanline, glitch 모션. |
| `editorial-scroll` | 기사, 출시 페이지, scrollytelling에 적합한 내러티브 스크롤 모션. |

## 목표

AI가 생성한 인터페이스가 의도적이고, 표현력 있으며, 살아 있는 느낌을 갖게 만드는 것.
