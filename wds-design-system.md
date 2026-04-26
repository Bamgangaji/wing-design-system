# WDS (Wing Design System)
> Korean Air (대한항공) 공식 디자인 시스템. 이 문서를 기반으로 새로운 컴포넌트를 생성하거나 테마를 적용할 때는 반드시 아래 토큰과 규칙을 따라야 한다.

---

## 1. Overview

### 1.1 시스템 정보
- **제품**: 대한항공 모바일 앱 및 웹 서비스
- **디자인 시스템명**: WDS (Wing Design System)
- **운영 도구**: Figma, Zeroheight
- **토큰 컬렉션**: KE Global (Primitive) → KE Alias (Semantic)

### 1.2 네이밍 컨벤션
- 토큰은 `카테고리/역할/상태` 구조로 작성한다.
  - 예: `color/text/title`, `color/fill/interaction/primary`
- 컴포넌트명은 PascalCase 또는 kebab-case로 표기한다.
  - 예: `Button`, `InputBox`, `button`, `input-box`
- Variant는 Figma의 Property 명칭을 따른다.
- 상태는 `default`, `hover`, `pressed`, `focused`, `disabled`, `readonly`, `error` 순서로 정의한다.

### 1.3 반응형 브레이크포인트
| 이름 | 너비 | 컬럼 수 | 거터 | 마진 |
|------|------|---------|------|------|
| small | 375px | 4 | 16px | 20px |
| medium-768 | 768px | 8 | 16px | 20px |
| medium-980 | 980px | 16 | 32px | 40px |
| large-1200 | 1200px | 12 | 32px | 360px |
| large-1440 | 1440px | 16 | 32px | 240px |
| compact (모바일 앱) | - | 4 | 16px | 20px |

---

## 2. Foundation

### 2.1 Color — Primitive (KE Global)

#### Brand — Dark Blue (네이비, 대한항공 대표 색상)
| 토큰 | Hex | 용도 |
|------|-----|------|
| `color/brand/darkblue/100` | `#051766` | Primary 브랜드 색상, 주요 텍스트, CTA |
| `color/brand/darkblue/80` | `#374585` | Pressed 상태, 보조 강조 |
| `color/brand/darkblue/60` | `#6974A3` | 중간 강조 |
| `color/brand/darkblue/40` | `#9BA2C2` | 비활성 강조 |
| `color/brand/darkblue/20` | `#CDD1E0` | 연한 배경 |
| `color/brand/darkblue/10` | `#E6E7EF` | 매우 연한 배경, 선택 상태 배경 |
| `color/brand/darkblue/10-alpha20` | `#E6E7EF33` | 반투명 오버레이 |

#### Brand — Light Blue (스카이 블루, 보조 브랜드 색상)
| 토큰 | Hex | 용도 |
|------|-----|------|
| `color/brand/lightblue/100` | `#57BBEB` | CTA, 인터랙션 강조 |
| `color/brand/lightblue/80` | `#77C8EF` | Hover 상태 |
| `color/brand/lightblue/60` | `#98D5F3` | 보조 강조 |
| `color/brand/lightblue/40` | `#BCE4F7` | 연한 강조 배경 |
| `color/brand/lightblue/20` | `#DDF1FB` | 버블 배경, 하이라이트 |
| `color/brand/lightblue/10` | `#EEF8FD` | 선택 항목 배경, 하이라이트 배경 |

#### Neutral (회색 계열)
| 토큰 | Hex | 용도 |
|------|-----|------|
| `color/neutral/90` | `#252525` | 거의 검정, 강조 텍스트 |
| `color/neutral/90-alpha50` | `#25252580` | Scrim (딤처리) |
| `color/neutral/80` | `#333333` | 본문 텍스트 보조 |
| `color/neutral/70` | `#5E5E5E` | 보조 텍스트, 아이콘 |
| `color/neutral/60` | `#A4A4A4` | 비활성, Disabled 텍스트 |
| `color/neutral/50` | `#BDBDBD` | 연한 비활성 |
| `color/neutral/40` | `#D9D9D9` | 테두리, Disabled 배경 |
| `color/neutral/30` | `#EDEDED` | 구분선, 배경 |
| `color/neutral/20` | `#F7F7F7` | 보조 배경 |
| `color/neutral/10` | `#FFFFFF` | 기본 배경, 흰색 |
| `color/neutral/10-alpha80` | `#FFFFFFCC` | 반투명 흰색 오버레이 |
| `color/neutral/10-alpha40` | `#FFFFFF66` | 연한 반투명 흰색 |

#### System — 상태 색상
| 토큰 | Hex | 의미 |
|------|-----|------|
| `color/system/green/100` | `#28794E` | Positive (성공/완료) |
| `color/system/green/200` | `#086A36` | Positive 강조 |
| `color/system/lightgreen/100` | `#F0FFF4` | Positive 배경 |
| `color/system/lightgreen/200` | `#DFF5E5` | Positive 배경 강조 |
| `color/system/orange/100` | `#BD5814` | Warning (경고) |
| `color/system/orange/200` | `#B33C00` | Warning 강조 |
| `color/system/lightorange/100` | `#FFF7EC` | Warning 배경 |
| `color/system/lightorange/200` | `#FFE8C9` | Warning 배경 강조 |
| `color/system/red/100` | `#DA291C` | Negative/Accent (오류/강조) |
| `color/system/red/200` | `#C92317` | Negative 강조 |
| `color/system/red/100-alpha60` | `#DA291C99` | 반투명 오류 |
| `color/system/lightred/100` | `#FFF5F5` | Negative 배경 |
| `color/system/lightred/200` | `#FFE3E3` | Negative 배경 강조 |

#### Membership — SKYPASS 등급 색상
| 토큰 | Hex | 등급 |
|------|-----|------|
| `color/membership/skypass/100` | `#57BBEB` | SKYPASS (Light Blue) |
| `color/membership/skypass/200` | `#051766` | SKYPASS (Dark Blue) |
| `color/membership/morningcalm/100` | `#CFCFCF` | 모닝캄 (밝은 회색) |
| `color/membership/morningcalm/200` | `#5E5E5E` | 모닝캄 (어두운 회색) |
| `color/membership/select/100` | `#666D70` | 밀리언마일러 셀렉트 |
| `color/membership/select/200` | `#515254` | 밀리언마일러 셀렉트 강조 |
| `color/membership/premium/100` | `#9B7B54` | 프리미엄 (골드) |
| `color/membership/premium/200` | `#704A27` | 프리미엄 강조 |
| `color/membership/millionmiler/100` | `#515254` | 밀리언마일러 |
| `color/membership/millionmiler/200` | `#000000` | 밀리언마일러 강조 |

---

### 2.2 Color — Semantic (KE Alias)

#### Text 색상
| 시맨틱 토큰 | 참조 Primitive | Hex | 용도 |
|------------|--------------|-----|------|
| `color/text/title` | darkblue/100 | `#051766` | 제목 텍스트 |
| `color/text/body` | darkblue/100 | `#051766` | 본문 텍스트 |
| `color/text/body-secondary` | neutral/70 | `#5E5E5E` | 보조 본문 텍스트 |
| `color/text/label` | darkblue/100 | `#051766` | 레이블 텍스트 |
| `color/text/label-alternative` | neutral/90 | `#252525` | 대안 레이블 |
| `color/text/inverse` | neutral/10 | `#FFFFFF` | 어두운 배경 위 텍스트 |
| `color/text/inverse-secondary` | neutral/10-alpha80 | `#FFFFFFCC` | 어두운 배경 위 보조 텍스트 |
| `color/text/inverse-disabled` | neutral/10-alpha40 | `#FFFFFF66` | 어두운 배경 위 비활성 텍스트 |
| `color/text/disabled` | neutral/60 | `#A4A4A4` | 비활성 텍스트 |
| `color/text/readonly` | neutral/70 | `#5E5E5E` | 읽기 전용 텍스트 |
| `color/text/pressed-ghost` | darkblue/80 | `#374585` | Ghost 버튼 Pressed 텍스트 |
| `color/text/positive` | green/100 | `#28794E` | 성공/완료 텍스트 |
| `color/text/positive-on` | green/200 | `#086A36` | 성공 강조 텍스트 |
| `color/text/highlight` | green/100 | `#28794E` | 하이라이트 텍스트 |
| `color/text/highlight-on` | green/200 | `#086A36` | 하이라이트 강조 |
| `color/text/warning` | orange/100 | `#BD5814` | 경고 텍스트 |
| `color/text/warning-on` | orange/200 | `#B33C00` | 경고 강조 텍스트 |
| `color/text/accent` | red/100 | `#DA291C` | 강조/오류 텍스트 |
| `color/text/negative` | red/100 | `#DA291C` | 오류 텍스트 |
| `color/text/negative-on` | red/200 | `#C92317` | 오류 강조 텍스트 |
| `color/text/accent-alpha60` | red/100-alpha60 | `#DA291C99` | 반투명 강조 텍스트 |

#### Icon 색상
| 시맨틱 토큰 | 참조 Primitive | Hex | 용도 |
|------------|--------------|-----|------|
| `color/icon/primary` | darkblue/100 | `#051766` | 기본 아이콘 |
| `color/icon/secondary` | neutral/70 | `#5E5E5E` | 보조 아이콘 |
| `color/icon/tertiary` | neutral/60 | `#A4A4A4` | 3차 아이콘 |
| `color/icon/inverse` | neutral/10 | `#FFFFFF` | 어두운 배경 위 아이콘 |
| `color/icon/inverse-secondary` | neutral/10-alpha80 | `#FFFFFFCC` | 어두운 배경 위 보조 아이콘 |
| `color/icon/inverse-disabled` | neutral/10-alpha40 | `#FFFFFF66` | 어두운 배경 위 비활성 아이콘 |
| `color/icon/disabled` | neutral/60 | `#A4A4A4` | 비활성 아이콘 |
| `color/icon/positive` | green/100 | `#28794E` | 성공 아이콘 |
| `color/icon/positive-on` | green/200 | `#086A36` | 성공 강조 아이콘 |
| `color/icon/warning` | orange/100 | `#BD5814` | 경고 아이콘 |
| `color/icon/warning-on` | orange/200 | `#B33C00` | 경고 강조 아이콘 |
| `color/icon/negative` | red/100 | `#DA291C` | 오류 아이콘 |
| `color/icon/negative-on` | red/200 | `#C92317` | 오류 강조 아이콘 |

#### Fill — Surface (배경 색상)
| 시맨틱 토큰 | Hex | 용도 |
|------------|-----|------|
| `color/fill/surface/primary` | `#FFFFFF` | 기본 카드/패널 배경 |
| `color/fill/surface/secondary` | `#F7F7F7` | 보조 배경 |
| `color/fill/surface/tertiary` | `#EDEDED` | 3차 배경 |
| `color/fill/surface/quarternary` | `#E6E7EF` | 4차 배경 (브랜드 틴트) |
| `color/fill/surface/highlight` | `#EEF8FD` | 하이라이트 배경 |
| `color/fill/surface/highlight-on` | `#DDF1FB` | 하이라이트 배경 강조 |
| `color/fill/surface/highlight-alternative` | `#BCE4F7` | 하이라이트 대안 배경 |
| `color/fill/surface/positive` | `#F0FFF4` | 성공 배경 |
| `color/fill/surface/positive-on` | `#DFF5E5` | 성공 배경 강조 |
| `color/fill/surface/positive-accent` | `#28794E` | 성공 강조 배경 |
| `color/fill/surface/warning` | `#FFF7EC` | 경고 배경 |
| `color/fill/surface/warning-on` | `#FFE8C9` | 경고 배경 강조 |
| `color/fill/surface/negative` | `#FFF5F5` | 오류 배경 |
| `color/fill/surface/negative-on` | `#FFE3E3` | 오류 배경 강조 |
| `color/fill/surface/inverse` | `#051766` | 어두운 배경 (네이비) |
| `color/fill/surface/snackbar` | `#252525CC` | 스낵바 배경 |
| `color/fill/surface/ashblue` | `#395FB8` | 애시 블루 배경 |
| `color/fill/surface/bubble` | `#DDF1FB` | 말풍선 배경 |
| `color/fill/surface/bubble-inverse` | `#5E5E5E` | 반전 말풍선 배경 |

#### Fill — 좌석 등급 색상
| 시맨틱 토큰 | Hex | 좌석 등급 |
|------------|-----|----------|
| `color/fill/surface/economy` | `#FFFFFF` | 이코노미 |
| `color/fill/surface/extralegroom` | `#EEF8FD` | 익스트라 레그룸 |
| `color/fill/surface/preferred` | `#EEF8FD` | 프리퍼드 |
| `color/fill/surface/premium` | `#57BBEB` | 프리미엄 이코노미 |
| `color/fill/surface/premium-on` | `#77C8EF` | 프리미엄 이코노미 Hover |
| `color/fill/surface/premium-upgrade` | `#BCE4F7` | 프리미엄 업그레이드 |
| `color/fill/surface/prestige` | `#051766` | 프레스티지 (비즈니스) |
| `color/fill/surface/prestige-on` | `#374585` | 프레스티지 Hover |
| `color/fill/surface/prestige-upgrade` | `#6974A3` | 프레스티지 업그레이드 |
| `color/fill/surface/first` | `#5E5E5E` | 퍼스트 클래스 |
| `color/fill/surface/first-on` | `#333333` | 퍼스트 클래스 Hover |

#### Fill — Interaction (인터랙션 색상)
| 시맨틱 토큰 | Hex | 용도 |
|------------|-----|------|
| `color/fill/interaction/primary` | `#051766` | Primary 버튼/요소 배경 |
| `color/fill/interaction/secondary` | `#BCE4F7` | Secondary 인터랙션 배경 |
| `color/fill/interaction/tertiary` | `#DDF1FB` | Tertiary 인터랙션 배경 |
| `color/fill/interaction/cta` | `#57BBEB` | CTA 버튼 배경 |
| `color/fill/interaction/form` | `#FFFFFF` | 폼 입력 배경 |
| `color/fill/interaction/overlay` | `#FFFFFFCC` | 오버레이 |
| `color/fill/interaction/overlay-light` | `#FFFFFF66` | 연한 오버레이 |
| `color/fill/interaction/disabled` | `#D9D9D9` | 비활성 배경 |
| `color/fill/interaction/disabled-on` | `#F7F7F7` | 비활성 배경 보조 |
| `color/fill/interaction/readonly` | `#F7F7F7` | 읽기 전용 배경 |
| `color/fill/interaction/enabled-switch-basic` | `#5E5E5E` | Switch Off 상태 |
| `color/fill/interaction/enabled-switch-text` | `#EDEDED` | Switch 텍스트 |
| `color/fill/interaction/enabled-dot` | `#6974A3` | Dot 인디케이터 |
| `color/fill/interaction/enabled-menubar` | `#D9D9D9` | 메뉴바 배경 |
| `color/fill/interaction/enabled-chip` | `#F7F7F7` | Chip 기본 배경 |
| `color/fill/interaction/selected-item` | `#EEF8FD` | 선택된 항목 배경 |
| `color/fill/interaction/pressed-solid` | `#051766` | Solid 버튼 Pressed |
| `color/fill/interaction/pressed-ghost` | `#E6E7EF` | Ghost 버튼 Pressed |
| `color/fill/interaction/pressed-ghost-inverse` | `#E6E7EF33` | Ghost Inverse Pressed |
| `color/fill/interaction/negative` | `#FFF5F5` | 오류 인터랙션 배경 |
| `color/fill/interaction/accent` | `#DA291C` | 강조 배경 |
| `color/fill/interaction/transparent` | `#FFFFFF00` | 투명 배경 |

#### Fill — Canvas (캔버스 배경)
| 시맨틱 토큰 | Hex | 용도 |
|------------|-----|------|
| `color/fill/canvas/primary` | `#FFFFFF` | 기본 캔버스 |
| `color/fill/canvas/secondary` | `#F7F7F7` | 보조 캔버스 |
| `color/fill/canvas/tertiary` | `#EDEDED` | 3차 캔버스 |
| `color/fill/canvas/scrim` | `#25252580` | 스크림 (딤처리) |

#### Border 색상
| 시맨틱 토큰 | Hex | 용도 |
|------------|-----|------|
| `color/border/primary` | `#051766` | 강조 테두리 |
| `color/border/secondary` | `#5E5E5E` | 보조 테두리 |
| `color/border/tertiary` | `#D9D9D9` | 기본 구분 테두리 |
| `color/border/inverse` | `#FFFFFF` | 반전 테두리 |
| `color/border/disabled` | `#A4A4A4` | 비활성 테두리 |
| `color/border/readonly` | `#5E5E5E` | 읽기 전용 테두리 |
| `color/border/surface` | `#D9D9D9` | 서피스 테두리 |
| `color/border/divider-primary` | `#D9D9D9` | 주요 구분선 |
| `color/border/divider-secondary` | `#EDEDED` | 보조 구분선 |
| `color/border/divider-highlight` | `#E6E7EF` | 하이라이트 구분선 |
| `color/border/divider-highlight-blue` | `#DDF1FB` | 블루 하이라이트 구분선 |
| `color/border/divider-top` | `#051766` | 상단 강조 구분선 |
| `color/border/positive` | `#28794E` | 성공 테두리 |
| `color/border/warning` | `#BD5814` | 경고 테두리 |
| `color/border/negative` | `#DA291C` | 오류 테두리 |
| `color/border/transparent` | `#FFFFFFCC` | 반투명 테두리 |

---

### 2.3 Typography

#### 폰트 패밀리
| 토큰 | 값 | 언어 |
|------|-----|------|
| `font/family/hanjingroup-sans` | `Hanjin Group Sans` | 한국어 (기본) |
| `font/family/yugothic-ui` | `Yu Gothic UI` | 일본어 |
| `font/family/microsoft-yahei` | `Microsoft YaHei` | 중국어 간체 |
| `font/family/microsoft-jhenghei` | `Microsoft JhengHei` | 중국어 번체 |
| `font/family/helvetica-neue` | `Helvetica Neue` | 영어 (대체) |
| `font/family/roboto` | `Roboto` | 영어 (Android) |

#### 폰트 웨이트
| 토큰 | 값 |
|------|-----|
| `font/weight/light` | `300` |
| `font/weight/regular` | `400` |
| `font/weight/bold` | `700` |

#### 타이포그래피 스케일
| 토큰 | 폰트 크기 | 웨이트 | Line Height | 용도 |
|------|----------|--------|-------------|------|
| `body-xl-bold` | 21px | Bold (700) | 150% | 대형 강조 본문 |
| `body-xl` | 21px | Regular (400) | 150% | 대형 본문 |
| `body-lg-bold` | 18px | Bold (700) | 150% | 중대형 강조 본문 |
| `body-lg` | 18px | Regular (400) | 150% | 중대형 본문 |
| `body-md-bold` | 16px | Bold (700) | 150% | 기본 강조 본문 |
| `body-md` | 16px | Regular (400) | 150% | 기본 본문 (가장 많이 사용) |
| `body-sm-bold` | 14px | Bold (700) | 150% | 소형 강조 본문, 레이블 |
| `body-sm` | 14px | Regular (400) | 150% | 소형 본문, 보조 텍스트 |
| `body-xs-bold` | 12px | Bold (700) | 150% | 최소 강조 (캡션, 뱃지) |
| `body-xs` | 12px | Regular (400) | 150% | 최소 텍스트 (캡션) |

#### Wide 타이포그래피 (웹 대형 화면용)
| 토큰 | 폰트 크기 | 용도 |
|------|----------|------|
| `font/wide/title-lg` | 42px | 대형 타이틀 |
| `font/wide/title-sm` | 36px | 소형 타이틀 |
| `font/wide/subtitle-lg-bold` | 28px | 대형 서브타이틀 Bold |
| `font/wide/subtitle-lg` | 28px | 대형 서브타이틀 |
| `font/wide/subtitle-sm-bold` | 21px | 소형 서브타이틀 Bold |
| `font/wide/subtitle-sm` | 21px | 소형 서브타이틀 |

#### Compact 타이포그래피 (모바일 앱용)
| 토큰 | 폰트 크기 | 용도 |
|------|----------|------|
| `font/compact/title-lg` | 28px | 모바일 대형 타이틀 |
| `font/compact/title-sm` | 24px | 모바일 소형 타이틀 |
| `font/compact/subtitle-lg-bold` | 21px | 모바일 대형 서브타이틀 Bold |
| `font/compact/subtitle-lg` | 21px | 모바일 대형 서브타이틀 |
| `font/compact/subtitle-sm-bold` | 18px | 모바일 소형 서브타이틀 Bold |
| `font/compact/subtitle-sm` | 18px | 모바일 소형 서브타이틀 |

---

### 2.4 Spacing (Size Scale)
모든 간격은 아래 스케일에서만 사용한다.

| 토큰 | 값 |
|------|-----|
| `size/0` | 0px |
| `size/1` | 1px |
| `size/2` | 2px |
| `size/4` | 4px |
| `size/8` | 8px |
| `size/12` | 12px |
| `size/16` | 16px |
| `size/20` | 20px |
| `size/24` | 24px |
| `size/28` | 28px |
| `size/32` | 32px |
| `size/36` | 36px |
| `size/40` | 40px |
| `size/48` | 48px |
| `size/56` | 56px |
| `size/64` | 64px |
| `size/80` | 80px |
| `size/96` | 96px |
| `size/112` | 112px |
| `size/128` | 128px |
| `size/9999` | 9999px (full radius용) |

---

### 2.5 Border Radius
| 토큰 | 값 | 용도 |
|------|-----|------|
| `radius/xs` | 4px | 작은 요소 (체크박스 등) |
| `radius/sm` | 8px | 소형 컴포넌트 |
| `radius/md` | 12px | 기본 컴포넌트 (인풋, 칩 등) |
| `radius/lg` | 16px | 카드, 대형 컴포넌트 |
| `radius/full` | 9999px | 완전한 원형 (버튼, 뱃지) |
| `radius/checkbox` | 2px | 체크박스 전용 |
| `radius/card` | 16px | 카드 전용 |
| `radius/button` | 24px | 버튼 전용 (pill 형태) |

---

### 2.6 Foundation 설계 원칙

**색상 사용 규칙**
- 텍스트: 항상 시맨틱 토큰 사용 (`color/text/*`)
- 배경: 항상 시맨틱 토큰 사용 (`color/fill/surface/*` 또는 `color/fill/canvas/*`)
- 테두리: 항상 시맨틱 토큰 사용 (`color/border/*`)
- Primitive 토큰을 컴포넌트에 직접 사용하지 않는다.

**접근성 원칙**
- 텍스트와 배경 간 명암비: WCAG AA 기준 4.5:1 이상
- 대형 텍스트(18px 이상 또는 14px Bold 이상): 3:1 이상
- 색상만으로 정보를 전달하지 않는다 — 아이콘 또는 텍스트 병행 필수

**다국어 지원**
- 기본 폰트: `Hanjin Group Sans` (한국어)
- 일본어 노출 시: `Yu Gothic UI` 적용
- 중국어 간체: `Microsoft YaHei`, 번체: `Microsoft JhengHei`
- 영어 폴백: `Helvetica Neue` → `Roboto`

---

---

## 3. Components

> **Claude 사용 지침**: 새 컴포넌트 생성 또는 기존 컴포넌트 수정 시, 아래 정의된 토큰과 규칙을 반드시 따른다. 임의의 색상값(hex)을 직접 사용하지 않고, 반드시 시맨틱 토큰(`color/text/*`, `color/fill/*`, `color/border/*`)을 참조한다.

---

### 3.1 액션 (Action)

---

#### Button

**정의**
사용자가 특정 액션을 실행하는 가장 기본적인 인터랙션 요소. WDS에서 모든 주요 사용자 행동의 시작점이다.

**목적**
- 예약, 검색, 결제 등 명확한 액션을 트리거한다.
- 시각적 계층을 통해 주요/보조/파괴적 액션을 구분한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `solid`, `ghost`, `text-only` |
| Size | `lg`, `md`, `sm` |
| State | `default`, `hover`, `pressed`, `disabled`, `loading` |
| Width | `fixed`, `full-width` |

**토큰 매핑**
| Variant | Background | Text | Border | Radius |
|---------|-----------|------|--------|--------|
| Solid (Primary) | `color/fill/interaction/primary` (#051766) | `color/text/inverse` (#FFFFFF) | none | `radius/button` (24px) |
| Solid (CTA) | `color/fill/interaction/cta` (#57BBEB) | `color/text/inverse` (#FFFFFF) | none | `radius/button` (24px) |
| Ghost | `color/fill/interaction/transparent` | `color/text/body` (#051766) | `color/border/primary` (#051766) | `radius/button` (24px) |
| Text-only | transparent | `color/text/body` (#051766) | none | - |
| Disabled | `color/fill/interaction/disabled` (#D9D9D9) | `color/text/disabled` (#A4A4A4) | none | `radius/button` (24px) |
| Pressed (Solid) | `color/fill/interaction/pressed-solid` (#051766) | - | - | - |
| Pressed (Ghost) | `color/fill/interaction/pressed-ghost` (#E6E7EF) | `color/text/pressed-ghost` (#374585) | - | - |

**Size 스펙**
| Size | Height | Font Token | Padding (H) |
|------|--------|-----------|-------------|
| LG | 56px | `body-lg-bold` (18px/Bold) | 20px |
| MD | 48px | `body-md-bold` (16px/Bold) | 16px |
| SM | 36px | `body-sm-bold` (14px/Bold) | 12px |

**Usage**
- ✅ 레이블은 동사형으로 작성한다 (예: "예약하기", "검색", "저장")
- ✅ Solid Primary는 한 화면에 1개만 사용한다
- ✅ 로딩 중 상태에서는 스피너를 표시하고 버튼을 비활성화한다
- ❌ 단순 페이지 이동에는 Link 컴포넌트를 사용한다

**접근성**
- `<button>` 태그 사용, `type="button"` 명시
- Disabled: `aria-disabled="true"`, `disabled` 속성
- Loading: `aria-busy="true"`
- 최소 터치 영역: 44×44px

---

#### Floating Action Button (FAB)

**정의**
화면 위에 부유하여 가장 주요한 단일 액션을 강조하는 버튼.

**목적**
- 검색, 필터, 상단 이동 등 화면 전체에서 항상 접근 가능한 핵심 액션을 제공한다.

**Variants**
| Property | Values |
|----------|--------|
| Size | `lg` (56px), `sm` (40px) |
| Type | `icon-only`, `icon+label` |
| State | `default`, `pressed`, `disabled` |

**토큰 매핑**
| 속성 | 토큰 | 값 |
|------|------|-----|
| Background | `color/fill/interaction/primary` | `#051766` |
| Icon | `color/icon/inverse` | `#FFFFFF` |
| Radius | `radius/full` | 9999px |

**Usage**
- ✅ 한 화면에 1개만 사용한다
- ✅ 화면 우하단에 고정 배치가 기본이다
- ❌ 복수의 FAB를 동시에 노출하지 않는다

**접근성**
- `aria-label`로 액션 명칭 명시 필수

---

#### Button Group

**정의**
2개 이상의 버튼을 묶어 관련 액션을 그룹화하는 컴포넌트.

**목적**
- 확인/취소, 이전/다음 등 대립하거나 연속되는 액션을 함께 제공한다.

**Variants**
| Property | Values |
|----------|--------|
| Layout | `horizontal`, `vertical` |
| Ratio | `equal`, `1:2` |
| Count | 2개, 3개 |

**Usage**
- ✅ 좌측/하단: 보조 액션 (Ghost), 우측/상단: 주요 액션 (Solid)
- ✅ 버튼 간 간격: `size/8` (8px)
- ❌ 4개 이상은 Button Group으로 사용하지 않는다

---

#### Menu Button

**정의**
클릭 시 드롭다운 메뉴를 표시하는 버튼.

**목적**
- 더보기, 정렬, 옵션 선택 등 추가 선택지를 공간을 절약하며 제공한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `icon-only`, `label+icon` |
| State | `default`, `opened`, `disabled` |

**접근성**
- `aria-haspopup="menu"`, `aria-expanded` 상태 관리
- 메뉴 열림 시 포커스 첫 항목으로 이동
- ESC로 메뉴 닫기

---

#### Input Button

**정의**
입력 필드 내부 또는 우측에 붙어 있는 버튼. 입력과 액션이 결합된 형태.

**목적**
- 검색창 내 검색 버튼, 쿠폰 코드 입력 후 적용 버튼 등에 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| Position | `inside`, `outside` |
| Type | `text`, `icon` |

---

#### Button Card

**정의**
카드 형태의 버튼. 이미지, 아이콘, 텍스트를 포함한 대형 선택형 버튼.

**목적**
- 좌석 등급 선택, 서비스 카테고리 선택 등 시각적으로 구분이 필요한 선택지를 제공한다.

**Variants**
| Property | Values |
|----------|--------|
| State | `default`, `selected`, `disabled` |
| Size | `lg`, `md`, `sm` |

**토큰 매핑**
| State | Background | Border |
|-------|-----------|--------|
| Default | `color/fill/surface/primary` | `color/border/tertiary` |
| Selected | `color/fill/interaction/selected-item` | `color/border/primary` |
| Disabled | `color/fill/interaction/disabled-on` | `color/border/disabled` |

---

### 3.2 입력 (Input)

---

#### Input Box

**정의**
사용자가 키보드나 키패드를 사용하여 짧은 텍스트(이름, 이메일, 항공권 번호 등)를 직접 입력하거나 수정할 수 있는 단일 라인 입력 필드.

**Variants**
| Property | Values |
|----------|--------|
| State | `default`, `hovered`, `focused`, `active-typing`, `filled`, `readonly`, `disabled`, `aria-disabled`, `error`, `success`, `validation` |
| Type | `basic`, `password`, `phone-number`, `card-number`, `flight-number` |
| Size | `lg`, `md` |
| Adornment | `none`, `leading-icon`, `trailing-icon`, `prefix`, `clear-button` |

**토큰 매핑**
| State | Background | Border | Text |
|-------|-----------|--------|------|
| Default | `color/fill/interaction/form` | `color/border/tertiary` | `color/text/body` |
| Focused | `color/fill/interaction/form` | `color/border/primary` | `color/text/body` |
| Error | `color/fill/interaction/negative` | `color/border/negative` | `color/text/negative` |
| Disabled | `color/fill/interaction/disabled-on` | `color/border/disabled` | `color/text/disabled` |
| Readonly | `color/fill/interaction/readonly` | `color/border/readonly` | `color/text/readonly` |

**Size 스펙**
| Size | Height | Font |
|------|--------|------|
| LG | 56px | `body-md` (16px) |
| MD | 48px | `body-sm` (14px) |

**Usage (입력 및 텍스트 규칙)**
* ✅ **레이블 필수:** Placeholder를 레이블 대신 사용하지 않는다. Placeholder는 입력 예시를 보여주는 도우미 역할로만 사용하며, 포커스 시 사라지므로 날짜 포맷 등 중요 정보는 반드시 레이블에 포함한다.
* ✅ **보조 설명:** 입력 안내가 필요한 경우 `Description`을 `Tooltip`보다 우선하여 적용하며, 공간이 제한적인 경우에만 `Tooltip`을 사용한다.
* ✅ **긴 텍스트 처리:** 텍스트가 길어져도 Input Box 내에서 개행되지 않고 잘려서(Truncate) 표시된다. 텍스트 전체 노출이 필수라면 `Textarea` 컴포넌트를 사용한다.
* ✅ **레이아웃:** Compact(모바일) 해상도에서는 1단으로 배치하며, Wide(웹) 해상도에서는 1단 또는 2단으로 배치한다.

**Usage (아이콘 및 부가 요소)**
* ✅ **Clear 버튼:** Input Box에 키보드 포커스가 이동하면, 입력된 값을 한 번에 삭제할 수 있는 `삭제(X) 버튼`을 우측에 시각적으로 표출한다.
* ✅ **Leading Icon (좌측 아이콘):** 신용카드 번호를 입력하는 경우에만 예외적으로 사용한다.
* ✅ **Trailing Icon (우측 아이콘):** 할인코드 조회 등 특정 액션이 결합된 경우 '조회' 버튼 등의 용도로 사용한다.
* ✅ **Prefix (접두어):** 항공편 번호 입력 시 상자에 "KE"를 prefix로 고정 노출하고 사용자로부터는 숫자만 입력받도록 구성할 수 있다.

**Usage (피드백 및 검증)**
* ✅ **오류 표출:** 잘못된 정보 입력 또는 누락 시, 에러 문구를 Input Box 하단에 즉시 표출하고 포커스를 해당 Input Box로 이동시킨다.
* ✅ **실시간 Validation:** 비밀번호 생성 등 입력 포맷이 복잡한 경우, 입력 조건(Description)을 Input Box **상단**에 배치하고 실시간으로 조건 충족 여부(Validation)를 시각적으로 표출한다.

**접근성 (Accessibility)**
* `<label>`과 `for`/`id` 속성을 명확히 연결하여 스크린 리더가 필드명을 읽을 수 있도록 한다.
* 에러 발생 시 `aria-invalid="true"`를 부여하고, `aria-describedby`를 통해 하단의 에러 메시지와 필드를 연결한다.
* **Autocomplete 속성 지정:** 사용자의 빠른 입력을 돕기 위해 목적에 맞는 HTML `autocomplete` 속성을 반드시 적용한다.

| 목적 | `autocomplete` 속성 값 |
|------|------------------------|
| 이름 (전체) | `name` |
| 이름 (First) | `given-name` |
| 성 (Last) | `family-name` |
| 생년월일 | `bday` |
| 이메일 | `email` |
| 전화번호 | `tel` |
| 도시 | `address-level2` |
| 주소 | `address-line1` |
| 상세 주소 | `address-line2` |
| 우편번호 | `postal-code` |
| 조직/회사 | `organization` |
| 직급 | `organization-title` |
---

#### Textarea

**정의**
최대 입력 글자 수가 제한되어 있는 여러 줄의 텍스트를 입력하거나 수정할 수 있는 멀티라인 입력 필드.

**Variants**
| Property | Values |
|----------|--------|
| State | `default` (enabled), `hovered`, `focused`, `active-typing`, `with-scroll`, `readonly`, `disabled`, `error` |
| Size | `md` |
| Feature | `character-count`, `clear-button` |

**토큰 매핑**
| State | Background | Border | Text |
|-------|-----------|--------|------|
| Default | `color/fill/interaction/form` | `color/border/tertiary` | `color/text/body` |
| Focused | `color/fill/interaction/form` | `color/border/primary` | `color/text/body` |
| Error | `color/fill/interaction/negative` | `color/border/negative` | `color/text/negative` |
| Disabled | `color/fill/interaction/disabled-on` | `color/border/disabled` | `color/text/disabled` |
| Readonly | `color/fill/interaction/readonly` | `color/border/readonly` | `color/text/readonly` |

**Usage (높이 및 스크롤 규칙)**
* ✅ **높이 가변:** 입력 박스의 기본 높이는 고정되어 있으나, 중요한 정보를 더 많이 노출해야 하는 경우 지정된 최대 높이까지 세로로 늘어날 수 있다.
* ✅ **스크롤 바 표출:** 입력된 텍스트가 최대 높이를 초과하여 길어질 경우, 컴포넌트 내부에 세로 스크롤 바를 표출하여 탐색을 지원한다.

**Usage (입력 및 피드백 규칙)**
* ✅ **글자 수 카운트:** 텍스트 영역 우측 상단에 실시간으로 입력된 글자 수 / 최대 글자 수 정보를 배치한다 (예: 0/300).
* ✅ **Clear 버튼 표출:** 사용자가 텍스트를 입력 중인 상태(`active-typing`)일 때, 입력된 텍스트를 한 번에 지울 수 있는 `삭제(X) 버튼`을 표출한다.
* ✅ **오류 및 글자 수 제한:** 제한된 글자 수를 넘어서면 더 이상 텍스트가 입력되지 않도록 차단하며, 에러 상태로 전환하여 오류 문구를 Textarea 하단에 즉시 표출한다.

**접근성 (Accessibility)**
* `<label>` 태그의 `for` 속성과 Textarea의 `id`를 명확히 연결한다.
* 에러 발생 시 `aria-invalid="true"` 속성을 부여한다.
* 우측 상단의 글자 수 카운트 정보와 하단의 에러 메시지는 `aria-describedby`를 통해 스크린 리더 사용자가 해당 정보를 함께 인지할 수 있도록 연결한다.

---

#### Checkbox

#### Checkbox

**정의**
여러 개의 옵션 중에서 0개 또는 1개 이상을 독립적으로 선택하거나 해제할 수 있는 입력 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic`, `group-horizontal`, `group-vertical` |
| Size | `lg` (24px), `md` (20px) |
| State | `unselected`, `selected`, `indeterminate`, `focused & hovered`, `disabled`, `aria-disabled`, `error` |
| Depth (Group) | `1-depth`, `2-depth` |

**토큰 매핑**
| State | Box Background | Box Border | Check Icon |
|-------|--------------|-----------|-----------|
| Unselected | `color/fill/surface/primary` | `color/border/tertiary` | - |
| Selected / Indeterminate | `color/fill/interaction/primary` | `color/border/primary` | `color/icon/inverse` |
| Disabled | `color/fill/interaction/disabled` | `color/border/disabled` | `color/icon/disabled` |

* 공통 적용: `radius/checkbox` (2px)

**Usage (선택 및 배치 규칙)**
* ✅ **다중 선택:** 0개 또는 1개 이상의 옵션 선택 시 사용한다. (반드시 1개만 선택해야 하는 경우 `Radio Group` 컴포넌트로 대체한다.)
* ✅ **모두 선택:** 항목 선택이 모두 필수이거나 옵션 개수가 많을 경우, 사용자의 빠른 선택을 돕는 '전체 선택(모두 선택하기)' 기능을 제공하는 것을 권장한다.
* ✅ **그룹화:** 여러 개의 Checkbox를 그룹으로 묶어 사용할 경우, 맥락을 명확히 전달하기 위해 그룹 레이블을 선택적으로 제공한다.

**Usage (레이블 및 상호작용 규칙)**
* ✅ **긍정문 사용:** 레이블은 부정문이나 이중 부정을 피하고, 직관적인 긍정문으로 작성하여 사용자의 혼란을 방지한다.
* ✅ **저장 시점:** 체크박스 선택 즉시 상태가 서버에 저장되거나 화면이 전환되지 않아야 하며, 최종적으로 '제출(Submit/Save)' 버튼을 눌렀을 때 값이 저장되도록 구현한다.

**Usage (피드백 및 검증)**
* ✅ **오류 표출 위치:** Checkbox를 단독으로 사용할 때는 개별 항목 하단에 오류 문구를 표출하고, 그룹으로 사용할 때는 그룹 컨테이너 전체 하단에 오류 문구를 표출한다.

**접근성 (Accessibility)**
* **구조화:** 그룹 형태의 Checkbox는 `<fieldset>` 태그로 묶고, 그룹의 제목은 `<legend>` 태그로 제공하여 논리적 구조를 생성한다.
* **오류 식별 (WCAG 3.3.1, 3.3.3):** 에러 발생 시 `<input>` 태그에 `aria-invalid="true"`를 부여하고, `aria-describedby`를 통해 오류 상황과 해결 방법을 스크린 리더가 즉시 읽어주도록 연결한다.
* **키보드 조작 (WCAG 2.1.1):** 마우스 없이 키보드(`Tab` 키로 포커스 이동, `Space` 키로 선택/해제 토글)만으로 모든 기능이 정상적으로 조작되어야 한다.
---

#### Radio Group

#### Radio Group

**정의**
상호 배타적인 여러 개의 옵션 중에서 반드시 한 개만 선택해야 할 때 사용하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic`, `segment` (버튼 형태) |
| State | `unselected`, `selected`, `focused & hovered`, `disabled`, `error` |
| Layout (Basic) | `vertical`, `horizontal` |
| Width (Segment) | `hug` (콘텐츠 너비 맞춤), `fill` (컨테이너 너비 채움) |
| Size | `xl`, `lg`, `md` (주로 웹 사용), `sm` (주로 모바일 사용) |

**토큰 매핑**
| State | Outer Ring / Border | Inner Dot / Background | Label |
|-------|-----------|----------|-------|
| Unselected | `color/border/tertiary` | - | `color/text/body` |
| Selected | `color/border/primary` | `color/fill/interaction/primary` | `color/text/body` |
| Disabled | `color/border/disabled` | `color/fill/interaction/disabled` | `color/text/disabled` |

**Usage (선택 및 배치 규칙)**
* ✅ **단일 선택 전용:** 한 개의 옵션만 선택할 수 있으며, 새로운 옵션을 선택하면 기존에 선택된 옵션은 자동으로 해제된다. (2개 이상 선택이 필요하다면 `Checkbox` 컴포넌트로 대체한다.)
* ✅ **개수 제한:** 옵션 개수가 2~5개일 때 적합하다. 옵션이 10개를 초과하여 한눈에 파악하기 어려운 경우 `Select Box` 컴포넌트로 대체한다.
* ✅ **기본값 제공:** 초기 상태에서 빈 화면을 방지하고 사용자의 결정을 돕기 위해, 가장 보편적인 옵션 하나를 '디폴트로 선택된 상태'로 제공하는 것을 권장한다.

**Usage (레이블 및 상호작용 규칙)**
* ✅ **그룹 레이블 필수:** Radio Group은 본질적으로 여러 개의 옵션이 하나의 묶음을 이루므로, 항목들의 맥락을 설명하는 상위 '그룹 레이블'을 생략 없이 반드시 제공한다.
* ✅ **저장 시점:** 라디오 버튼 선택 즉시 설정이 변경되거나 서버에 저장되지 않아야 하며, 최종적으로 '제출(Submit/Save)' 버튼을 눌렀을 때 값이 적용되도록 구현한다. (선택 즉시 적용되는 인터랙션이 필요하다면 `Switch` 컴포넌트로 대체한다.)
* ✅ **텍스트 처리:** 레이블 텍스트가 길어질 경우, 영역을 벗어나 잘리지 않고 하단으로 개행되어 전체 내용이 표출되도록 한다.

**Usage (피드백 및 검증)**
* ✅ **오류 표출 위치:** 옵션을 선택하지 않고 제출하는 등 오류가 발생하면, 특정 항목 아래가 아닌 Radio Group '전체 컨테이너' 하단에 오류 문구를 표출한다.

**접근성 (Accessibility)**
* 논리적인 그룹화를 위해 Radio Group 전체를 `<fieldset>` 태그로 묶고, 반드시 표출해야 하는 그룹 레이블은 `<legend>` 태그를 사용하여 스크린 리더에 구조를 전달한다.
* 입력 요소에는 `type="radio"` 속성을 사용하고, 동일한 그룹에 속한 버튼들은 동일한 `name` 속성값을 가져야 방향키 조작 시 포커스가 그룹 내에서만 순환된다.
---

#### Select Box

#### Radio Group

**정의**
상호 배타적인 여러 개의 옵션 중에서 반드시 한 개만 선택해야 할 때 사용하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic`, `segment` (버튼 형태) |
| State | `unselected`, `selected`, `focused & hovered`, `disabled`, `error` |
| Layout (Basic) | `vertical`, `horizontal` |
| Width (Segment) | `hug` (콘텐츠 너비 맞춤), `fill` (컨테이너 너비 채움) |
| Size | `xl`, `lg`, `md` (주로 웹 사용), `sm` (주로 모바일 사용) |

**토큰 매핑**
| State | Outer Ring / Border | Inner Dot / Background | Label |
|-------|-----------|----------|-------|
| Unselected | `color/border/tertiary` | - | `color/text/body` |
| Selected | `color/border/primary` | `color/fill/interaction/primary` | `color/text/body` |
| Disabled | `color/border/disabled` | `color/fill/interaction/disabled` | `color/text/disabled` |

**Usage (선택 및 배치 규칙)**
* ✅ **단일 선택 전용:** 한 개의 옵션만 선택할 수 있으며, 새로운 옵션을 선택하면 기존에 선택된 옵션은 자동으로 해제된다. (2개 이상 선택이 필요하다면 `Checkbox` 컴포넌트로 대체한다.)
* ✅ **개수 제한:** 옵션 개수가 2~5개일 때 적합하다. 옵션이 10개를 초과하여 한눈에 파악하기 어려운 경우 `Select Box` 컴포넌트로 대체한다.
* ✅ **기본값 제공:** 초기 상태에서 빈 화면을 방지하고 사용자의 결정을 돕기 위해, 가장 보편적인 옵션 하나를 '디폴트로 선택된 상태'로 제공하는 것을 권장한다.

**Usage (레이블 및 상호작용 규칙)**
* ✅ **그룹 레이블 필수:** Radio Group은 본질적으로 여러 개의 옵션이 하나의 묶음을 이루므로, 항목들의 맥락을 설명하는 상위 '그룹 레이블'을 생략 없이 반드시 제공한다.
* ✅ **저장 시점:** 라디오 버튼 선택 즉시 설정이 변경되거나 서버에 저장되지 않아야 하며, 최종적으로 '제출(Submit/Save)' 버튼을 눌렀을 때 값이 적용되도록 구현한다. (선택 즉시 적용되는 인터랙션이 필요하다면 `Switch` 컴포넌트로 대체한다.)
* ✅ **텍스트 처리:** 레이블 텍스트가 길어질 경우, 영역을 벗어나 잘리지 않고 하단으로 개행되어 전체 내용이 표출되도록 한다.

**Usage (피드백 및 검증)**
* ✅ **오류 표출 위치:** 옵션을 선택하지 않고 제출하는 등 오류가 발생하면, 특정 항목 아래가 아닌 Radio Group '전체 컨테이너' 하단에 오류 문구를 표출한다.

**접근성 (Accessibility)**
* 논리적인 그룹화를 위해 Radio Group 전체를 `<fieldset>` 태그로 묶고, 반드시 표출해야 하는 그룹 레이블은 `<legend>` 태그를 사용하여 스크린 리더에 구조를 전달한다.
* 입력 요소에는 `type="radio"` 속성을 사용하고, 동일한 그룹에 속한 버튼들은 동일한 `name` 속성값을 가져야 방향키 조작 시 포커스가 그룹 내에서만 순환된다.

---

#### Switch

#### Switch

**정의**
설정이나 기능을 즉시 켜고 끄거나, 상호 배타적인 두 상태 중 하나를 선택하는 토글 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (레이블 우측 토글), `setting` (모바일 설정형), `text` (텍스트 토글형) |
| State | `unselected` (off), `selected` (on), `focused & hovered`, `pressed`, `disabled`, `aria-disabled` |
| Background | `white`, `gray` (Setting 및 Text 타입 적용) |

**토큰 매핑**
| State | Track Background | Thumb |
|-------|----------------|-------|
| Off | `color/fill/interaction/enabled-switch-basic` (#5E5E5E) | `color/fill/surface/primary` |
| On | `color/fill/interaction/primary` (#051766) | `color/fill/surface/primary` |
| Disabled | `color/fill/interaction/disabled` | `color/fill/surface/primary` |
* Text Type 배경: `color/fill/interaction/enabled-switch-text` 적용

**Usage (기능 및 상호작용 규칙)**
* ✅ **즉시 적용:** Switch는 Checkbox나 Radio Group과 달리, 선택(토글) 즉시 상태가 적용 및 저장되어야 한다. (제출 버튼 클릭 후 적용되는 항목은 Switch를 사용하지 않는다.)
* ✅ **고정 레이블:** 레이블 텍스트는 토글 상태(On/Off)에 따라 변경되지 않도록 고정하여 사용자의 혼란을 방지한다.
* ✅ **클릭 영역:** 사용자의 조작 편의성을 위해 토글 버튼 자체뿐만 아니라 레이블이 포함된 컨테이너 전체 영역을 클릭(또는 터치) 가능하도록 구현한다.

**Usage (배치 및 텍스트 규칙)**
* ✅ **요소 배치 순서:** Basic 타입에서 Tooltip과 함께 사용할 경우 `레이블` → `Tooltip` → `토글 버튼` 순서로 배치한다.
* ✅ **추가 설명 (Setting):** Setting 타입에서 부가 설명 문구가 필요한 경우 레이블 하단에 표출하며, 이에 따라 컨테이너의 전체 높이가 유연하게 늘어난다.
* ✅ **긴 텍스트 표출:** 레이블 텍스트가 길어지면 버튼 영역이 가로로 확장되다가 허용 범위를 넘어서면 잘리지 않고 하단으로 개행된다.
* ✅ **배경 색상 지정:** Setting 및 Text 타입은 위치한 배경색(`White` 또는 `Gray`)에 맞춰 알맞은 옵션을 적용하되, 한 화면/그룹 내에서 스타일을 혼용하지 않는다.
* ✅ **레이아웃:** Compact(모바일) 해상도에서는 1단으로 배치하고, Wide(웹/데스크톱) 해상도에서는 2단 이상으로 배치한다.

**접근성 (Accessibility)**
* HTML 요소에 `role="switch"` 속성을 적용하여 해당 UI가 스위치임을 명시한다.
* 스크린 리더 사용자가 현재 상태를 정확히 인지할 수 있도록, 상태 변화에 따라 `aria-checked="true"` 또는 `aria-checked="false"` 속성을 동적으로 업데이트한다.
* 마우스 조작뿐만 아니라 키보드의 `Enter` 또는 `Space` 키를 통해 상태를 변경할 수 있어야 한다.

---

#### Autocomplete

#### Autocomplete

**정의**
텍스트 입력 시 관련 추천 항목을 실시간으로 제안하여, 방대한 목록(공항, 도시명 등)에서 쉽게 필터링하고 선택할 수 있도록 돕는 입력 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (출/도착지 등 일반 검색), `search` (통합 검색용) |
| State | `default` (collapsed), `focused`, `active-typing`, `dropdown-open` (expanded), `selected`, `error`, `disabled` |

**토큰 매핑**
| 영역 | 토큰 |
|------|------|
| Dropdown background | `color/fill/surface/primary` |
| Hover/Selected item | `color/fill/interaction/selected-item` |
| Matching text | `color/text/highlight` |

**Usage (동작 및 레이아웃 규칙)**
* ✅ **너비 및 확장:** 전체 컨테이너 너비는 화면 해상도에 맞게 유연하게 확장된다. 입력 박스를 누르면 하단에 전체 너비에 맞춘 리스트박스가 확장 표출된다.
* ✅ **입력 중(Typing) 상태:** 사용자가 텍스트를 입력하는 중에는 우측의 펼침/접힘 화살표 아이콘이 사라지고, 입력된 값을 한 번에 삭제할 수 있는 `삭제(X) 버튼`이 표출된다.
* ✅ **긴 텍스트 표출:** 텍스트가 길어질 경우, `Input Box` 영역 내에서는 텍스트가 잘려서(Truncate) 표출되지만, 하단 `Listbox`의 항목들은 너비를 넘어가면 개행되어 전체 텍스트가 표출된다.
* ✅ **매칭 텍스트 강조:** 사용자가 입력한 값과 매칭되는 결과 텍스트에는 하이라이트 색상을 적용하여 시각적으로 구분한다.

**Usage (리스트박스 노출 규칙)**
* ✅ **최대 높이:** 확장된 리스트박스의 최대 높이는 `332px`이며, 리스트가 이를 초과할 경우 내부에 세로 스크롤바가 생성된다.
* ✅ **로딩 상태:** 리스트를 서버에서 불러오는 등 일정 시간이 필요한 경우 로딩 인디케이터를 표출하며, 이때 리스트박스의 최대 높이는 `120px`로 제한한다.
* ✅ **검색어 표출 순서 (Search 타입):** 통합 검색 화면에서 검색어를 입력하면 `최근 검색어` → `제안 검색어` 순서로 리스트가 표출된다.

**접근성 (Accessibility)**
* **WAI-ARIA 역할:** 입력 필드는 `role="combobox"`, 하단 목록은 `role="listbox"`, 개별 항목은 `role="option"`을 사용하여 스크린 리더에 컴포넌트의 역할을 명확히 전달한다.
* **상태 메시지 (WCAG 4.1.3):** 검색 결과에 대한 정보(예: "검색 결과가 n개 있습니다")는 화면에 보이지 않더라도 `aria-live` 속성을 활용한 숨김 텍스트로 제공하여 즉각적으로 읽어주도록 한다.
* **키보드 상호작용 (WCAG 2.1.1):**
  * `Arrow (방향키)`: 상/하 키를 통해 리스트박스 항목 간 포커스 이동이 가능해야 하며, Search 타입의 경우 좌/우 키로 검색어와 삭제 버튼 간 이동이 가능해야 한다.
  * `Enter`: 리스트나 검색어가 선택되며, 선택된 값이 입력 박스에 채워지고 리스트박스는 닫힌다.
  * `ESC`: 입력 박스 내의 입력값이 삭제되고 확장된 영역이 닫히며 포커스는 입력 박스로 되돌아간다.

---

#### Date Picker

**정의**
달력 UI를 통해 날짜를 선택하는 입력 컴포넌트.

**목적**
- 항공권 출발일/귀국일, 일정 설정 등 날짜 입력에 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| Mode | `single` (단일 날짜), `range` (기간 선택) |
| View | `inline`, `popover` |
| State | `default`, `selected`, `range-start`, `range-end`, `in-range`, `disabled`, `today` |

**토큰 매핑**
| State | Background | Text |
|-------|-----------|------|
| Today | - | `color/text/accent` |
| Selected | `color/fill/interaction/primary` | `color/text/inverse` |
| In-range | `color/fill/surface/highlight` | `color/text/body` |
| Disabled | - | `color/text/disabled` |

**Usage**
- ✅ 과거 날짜는 Disabled 처리한다
- ✅ 모바일에서는 Bottom Sheet 내에 표시한다

---

#### Flexible Date

**정의**
특정 날짜 대신 "며칠 이내", "이번 달" 등 유연한 기간 조건으로 항공편을 검색하는 날짜 선택 컴포넌트.

**목적**
- 날짜가 확정되지 않은 사용자가 최저가 항공편을 탐색할 수 있도록 돕는다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `±3일`, `±7일`, `이번 달`, `다음 달`, `월 선택` |
| State | `default`, `selected` |

**토큰 매핑**
| State | Background | Border |
|-------|-----------|--------|
| Default | `color/fill/surface/secondary` | `color/border/tertiary` |
| Selected | `color/fill/interaction/selected-item` | `color/border/primary` |

---

#### DateInput

#### Date Input

**정의**
항공권 구매를 위한 핵심 UI(Booking Tool)의 구성 요소로, 클릭 시 Date Picker를 호출하여 여정 날짜를 선택하고 결과를 표시하는 버튼형 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (편도/왕복 지원, 메인 Booking Tool용), `box` (편도 전용, 단일 날짜 선택용) |
| State | `unselected` (선택 전), `selected` (선택 후), `focused & hovered`, `disabled`, `aria-disabled`, `readonly`, `error` |
| Trip Type | `oneway` (편도), `roundtrip` (왕복) |

**토큰 매핑**
| State | Background | Border | Text | Icon |
|-------|-----------|--------|------|------|
| Unselected | `color/fill/surface/primary` | `color/border/tertiary` | `color/text/body-secondary` | `color/icon/primary` |
| Selected | `color/fill/surface/primary` | `color/border/tertiary` | `color/text/body` | `color/icon/primary` |
| Error | `color/fill/surface/negative` | `color/border/negative` | `color/text/negative` | `color/icon/negative` |
| Disabled | `color/fill/interaction/disabled-on` | `color/border/disabled` | `color/text/disabled` | `color/icon/disabled` |

**Usage (상호작용 및 포맷 규칙)**
* ✅ **Date Picker 연동:** 컴포넌트를 누르면 여정에 맞는 `Date Picker` 오버레이가 표출되며, 사용자가 날짜를 선택하고 닫으면 Date Input에 해당 날짜가 업데이트된다.
* ✅ **날짜 표출 포맷:** 공간 제약을 고려하여 **연도는 생략**하고 `월`, `일`, `요일` 정보만 표출한다. 편도 여정은 출발일만, 왕복 여정은 출발일과 도착일을 함께 표출한다.
* ✅ **아이콘 상태 연동:** 지정된 캘린더 아이콘을 레이블과 함께 배치하며, 컴포넌트의 상태(Disabled, Error 등)가 변하면 아이콘의 색상도 동일한 위계의 시맨틱 토큰으로 맞춰 변경한다.

**Usage (긴 텍스트 및 레이아웃 규칙)**
* ✅ **선택 전 (Placeholder):** 안내 텍스트가 최대 너비를 초과하는 경우, 영역 안에서 개행 없이 말줄임(...) 처리하여 단정하게 표출한다.
* ✅ **선택 후 (Date 표시):** 사용자가 날짜를 선택한 후에는 모바일 등 너비가 좁은 환경이더라도 **말줄임 없이 모든 날짜 정보를 표출**하며, 최대 너비를 넘어갈 경우 잘리지 않고 하단으로 개행되어 전체 정보가 표시된다.
* ✅ **Type별 조합:** `Basic` 타입은 FromTo, Passenger, Class 컴포넌트와 함께 메인 Booking Tool을 구성할 때 사용하며, `Box` 타입은 다른 Input Box들과 나란히 배치해야 하는 좁은 영역(예: 예약 조회, Quick Booking)에 사용한다.

**접근성 (Accessibility)**
* 비활성 상태 시 상황에 맞게 `disabled` 속성 또는 `aria-disabled="true"` 속성을 부여하여 스크린 리더에 상태를 명확히 전달한다.
* 에러 발생 시 `<button>` 태그에 `aria-invalid="true"`를 부여하고, 하단의 오류 문구와 `aria-describedby`로 연결한다.

#### Spinbutton

#### Spinbutton

**정의**
증가(+) 및 감소(-) 버튼을 눌러 입력 필드의 숫자 값을 세밀하게 조정하는 컴포넌트. 탑승객 수, 수하물 개수 등 범위가 작고 제한된 숫자 입력에 주로 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| State | `default` (enabled), `hovered & focused`, `pressed`, `disabled`, `readonly`, `error` |
| Value State | `0` (default), `1 이상` (positive), `min-reached`, `max-reached` |
| Orientation | `horizontal`, `vertical` |

**Usage (수치 조정 및 피드백 규칙)**
* ✅ **사용 범위:** 10 이하의 소량의 숫자를 조정할 때 사용하며, 최대값은 한 자리 수(예: 9)까지만 사용하는 것을 권장한다. 대량의 숫자 입력이 필요할 경우 `Input Box`로 대체한다.
* ✅ **기본값 표출:** 입력 박스가 빈(Empty) 상태로 존재할 수 없으며, 항상 기본 숫자를 표출해야 한다. 
* ✅ **최소/최대 제약:** 설정된 최소/최대 값에 도달하면 해당 방향의 버튼(+ 또는 -)을 `Disabled` 상태로 변경하여 더 이상 조작할 수 없음을 직관적으로 알린다. (예: 0일 때 감소 버튼 비활성화)
* ✅ **시각적 강조 (색상):** 기본 숫자 값이 0이 아닌 **1 이상**일 때, 숫자 텍스트에 `Positive` 색상(`color/text/positive`)을 적용하여 값이 활성화되었음을 강조한다.

**Usage (레이아웃 및 부가 정보 규칙)**
* ✅ **부가 설명:** 레이블 하단에 `Description`을 간결하게 추가할 수 있으며, 설명이 지나치게 길거나 복잡할 경우 `Tooltip`을 병행하여 사용한다.
* ✅ **오류 표출:** 입력 불가능한 상태이거나 오류 발생 시, 해당 Spinbutton의 레이블(또는 전체 컨테이너) 하단에 오류 메시지를 표출한다.
* ✅ **반응형 배치 (Orientation):** * `Compact` (모바일): 가로형(Horizontal)만 사용한다.
  * `Wide` (웹): 가로형(Horizontal)과 세로형(Vertical) 모두 사용 가능하다. 단, 세로형 배치는 한 화면에 최대 3개까지만 나란히 배치하며 해상도에 따라 일정한 간격으로 자동 정렬되도록 한다.

**인터랙션 및 모션 (Motion)**
* 수치가 변경될 때 숫자의 위치(Position)와 색상(Color) 변화에 트랜지션을 적용하여 부드러운 피드백을 제공한다.
* **Duration:** 300ms (3 beat)
* **Easing:** Ease in and out

**접근성 (Accessibility)**
* `role="spinbutton"`을 사용하여 스크린 리더에 컴포넌트의 역할을 명시한다.
* `aria-valuenow`, `aria-valuemin`, `aria-valuemax` 속성을 통해 현재 값과 허용 가능한 범위를 스크린 리더가 읽어줄 수 있도록 실시간으로 업데이트한다.
---

#### File Upload

#### File Upload

**정의**
사용자가 파일을 한 개 또는 여러 개 선택하여 시스템에 업로드할 때 사용하는 입력 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `button` (모바일/기본), `drag-and-drop` (웹/데스크톱) |
| State | `default` (enabled), `pressed`, `loading`, `error` |
| Selection | `single` (단일 파일), `multiple` (다중 파일) |

**토큰 매핑**
| State | Background | Border |
|-------|-----------|--------|
| Default | `color/fill/surface/secondary` | `color/border/tertiary` (dashed) |
| Hover/Drag | `color/fill/surface/highlight` | `color/border/primary` (dashed) |
| Error | `color/fill/surface/negative` | `color/border/negative` |

**Usage (업로드 및 피드백 규칙)**
* ✅ **필수 항목 표시:** 파일 첨부가 필수인 경우, 레이블에 Red Dot(필수 표시)을 시각적으로 표출한다.
* ✅ **오류 표출:** 필수 항목 누락, 제한 용량 초과, 지원하지 않는 파일 포맷 등 오류 발생 시 업로드 영역 하단에 즉시 오류 문구를 표출한다.
* ✅ **상태 피드백:** 파일이 업로드되는 동안 스피너(Spinner) 로딩 이미지를 통해 진행 상태를 시각적으로 안내하고, 업로드가 완료되면 해당 영역을 파일 삭제 버튼으로 변경한다.

**Usage (파일 리스트 및 레이아웃 규칙)**
* ✅ **긴 파일명 처리:** 파일명이 길어 영역을 초과하는 경우, 파일명의 끝부분을 말줄임(...) 처리하되 **파일 확장자(.pdf, .png 등)는 생략 없이 반드시 노출**되도록 한다.
* ✅ **리스트 정렬:** 여러 파일이 업로드된 상태에서 중간에 있는 파일을 삭제할 경우, 하단에 위치한 파일들이 위로 이동하여 리스트 중간에 빈 공간(Stack)이 생기지 않도록 정렬한다.
* ✅ **Drag & Drop:** Wide(데스크톱) 해상도에서는 영역 안으로 파일을 직접 끌어다 놓을 수 있는 Drag & Drop 기능을 지원한다.

**접근성 (Accessibility)**
* **안내 제공:** 파일 포맷에 대한 제약 조건 등 안내 사항은 `<label>` 태그 내에 삽입하여 스크린 리더가 함께 읽을 수 있도록 한다. (스크린 리더 사용자에게 혼란을 줄 수 있는 "여기로 드래그하세요" 등의 시각적 방향 지시어는 피한다.)
* **키보드 및 포커스 관리:** * 키보드 조작 시 `Enter` 키뿐만 아니라 `Space` 키로도 파일 업로드를 실행할 수 있어야 한다.
  * 포커스 표시는 CSS `:focus`가 아닌 `:focus-visible`을 적용하여 명확한 시각적 단서를 제공한다.
  * 파일 추가 후에는 새로 추가된 파일 영역으로 포커스를 이동시킨다.
  * 파일 삭제 시 이전 파일 영역으로 포커스를 이동시키며, 남은 파일이 없으면 '파일 추가' 버튼으로 포커스를 이동시킨다.
* **명확한 연결 (WAI-ARIA):**
  * `<label>`의 `for`와 파일 추가 `<input>`의 `id`를 일치시켜, 레이블 클릭 시에도 파일 선택 창이 열리도록 한다.
  * 업로드된 파일 항목의 `<input>` 속성에 `title="파일명"`을 삽입하여 현재 선택된 파일을 명확히 식별할 수 있게 한다.
  * 삭제 버튼에는 `aria-describedby="{파일ID}"`를 사용하여 어떤 파일이 삭제되는지 대상을 정확히 연결한다.
  * 오류 발생 시 `<input>`에 `aria-invalid="true"`를 부여하고, `aria-describedby`를 통해 하단의 에러 메시지 ID와 연결한다.
---

#### Consent

#### Consent

**정의**
이용 약관, 개인정보 취급 방침, 마케팅 수신 등 법규나 정책에 대한 사용자의 명시적인 확인이나 동의를 받기 위해 사용하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Component Type | `consent-button` (약관 상세 확인용 버튼), `consent-checkbox` (동의 체크박스) |
| Layout Type | `button + checkbox` 조합, `button-only`, `checkbox-only` |
| State (Checkbox) | `unselected`, `selected`, `focused & hovered`, `error` |
| State (Button) | `agree-false` (미동의 상태 표출), `agree-true` (동의 완료 표출), `focused & hovered`, `error` |

**Usage (구성 및 조합 규칙)**
* ✅ **기본 조합:** 사전에 상세 내용을 확인해야 하는 약관은 `동의 버튼(Consent button)`과 `동의 체크박스(Consent checkbox)`를 조합하여 사용한다.
* ✅ 상황에 따라 상세 확인 없이 바로 동의가 가능한 경우 `동의 체크박스` 단독으로, 또는 동의 여부를 버튼 텍스트로 치환하는 경우 `동의 버튼` 단독으로 사용할 수 있다.

**Usage (클릭 영역 및 인터랙션 규칙)**
* ✅ **클릭 영역:** 동의 체크박스의 클릭(터치) 가능 영역은 체크박스와 텍스트를 포함한 레이블 전체로 설정한다. 단, 레이블 내부에 텍스트 링크나 Arrow 버튼이 겹쳐 있는 경우 링크/버튼 영역이 체크박스 토글보다 우선하여 동작해야 한다.
* ✅ **오류 표출:** 필수 동의 항목을 선택하지 않고 다음 단계(제출 등)로 진행하려 할 때 오류가 발생하며, 오류 문구는 해당 체크박스 또는 버튼 영역의 **하단**에 표출한다.

**Usage (텍스트 및 레이아웃 규칙)**
* ✅ **긴 텍스트 표출:** 동의 버튼이나 체크박스의 텍스트가 길어져 줄바꿈이 일어나는 경우, 체크박스와 텍스트는 컨테이너의 상단(Top)을 기준으로 정렬한다.
* ✅ **버튼명 길이에 따른 배치:** * 버튼 텍스트가 짧아 컴포넌트 전체 너비의 **50% 미만**을 차지할 경우, 텍스트와 체크박스(또는 화살표)를 좌우 양끝으로 배치한다 (Space between).
  * 버튼 텍스트가 길어 컴포넌트 전체 너비의 **50% 이상**을 차지할 경우, 버튼 텍스트를 화살표 하단으로 개행하여 배치한다.
* ✅ **링크 사용 주의:** 동의 체크박스 레이블 중간에 약관 페이지로 이동하는 텍스트 링크를 삽입할 수 있으나, 이 경우 컴포넌트 우측의 Arrow(화살표) 버튼과 중복으로 함께 사용하지 않는다.

**접근성 (Accessibility)**
* 필수 항목의 경우 `<input type="checkbox">` 요소에 `aria-required="true"`를 부여한다.
* 동의 버튼을 통해 모달이나 새 창이 열리는 경우 `aria-haspopup` 또는 `aria-expanded`를 적절히 제공하여 스크린 리더에 열림/닫힘 상태를 안내한다.
* 에러 발생 시 `aria-invalid="true"`를 부여하고 하단의 오류 문구 ID를 `aria-describedby`로 연결한다.

---

### 3.3 탐색 (Navigation)

---

#### Tab

#### Tab

**정의**
하나의 화면 내에서 연관된 여러 개의 콘텐츠를 논리적으로 그룹화하여, 공간 효율적으로 전환하며 탐색할 수 있도록 돕는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Category | `basic` (텍스트 중심의 기본 탭), `custom` (아이콘 조합 및 패널 스타일 커스텀) |
| Style Type| `underline`, `filled`, `chip` |
| State | `unselected` (default), `selected`, `focused & hovered`, `disabled` |
| Scroll | `fixed` (고정형), `scrollable` (스크롤형) |

**토큰 매핑**
| Style Type | Selected BG | Selected Text | Indicator |
|------------|------------|--------------|-----------|
| Underline | transparent | `color/text/body` | `color/border/divider-top` (#051766) |
| Filled | `color/fill/interaction/primary` | `color/text/inverse` | none |
| Chip | `color/fill/interaction/primary` | `color/text/inverse` | none |

**Usage (구성과 선택 규칙)**
* ✅ **최소 개수:** Tab 버튼은 반드시 2개 이상일 때만 사용한다. (1개인 경우 Tab으로 구성하지 않는다.)
* ✅ **항상 선택됨:** 화면 진입 시 항상 첫 번째(앞에 위치한) Tab이 선택된 상태로 노출되어야 하며, 선택된 Tab과 패널은 화면에 항상 보여야 한다.
* ❌ **제한 사항:** 순서가 중요한 단계별 흐름(Step)에는 Tab 대신 `Progress Indicator`를 사용한다.

**Usage (텍스트 및 레이아웃 규칙)**
* ✅ **긴 텍스트 표출:** Tab 버튼 내 텍스트가 최대 너비에 도달하면 하단으로 개행된다. 최대 2줄까지 표출되며, 2줄을 초과하면 말줄임(...) 처리되므로 가급적 개행되지 않도록 간결하게 작성한다.
* ✅ **너비 기준:** Compact(모바일)와 Wide(웹) 해상도에 맞춰 각각 정의된 최소/최대 너비 기준을 적용한다.
* ✅ **패널 간격 (Custom):** Custom Tab 패널을 Compact(모바일) 환경에서 사용할 때는 좌우 여백(Margin) 없이 Full 화면 너비로 사용한다.

**Usage (패널 내부 및 아이콘 규칙)**
* ✅ **패널 콘텐츠:** Tab 패널 내부에는 Image, Button, List, Paragraph 등 다양한 컴포넌트를 자유롭게 포함할 수 있다.
* ✅ **Heading 위계 조절:** Tab 패널 내부에 `Heading`을 사용할 때는 페이지 전체의 정보 위계에 맞게 Level을 한 단계 낮추어 적용한다.
* ✅ **아이콘 사용 (Custom 전용):** `Basic` Tab은 아이콘을 사용하지 않는다. `Custom` Tab 버튼의 경우에만 텍스트 앞에 아이콘을 선택적으로 적용할 수 있다.

**모션 (Motion)**
Tab 버튼 선택 시 기존 패널이 닫히고 새 패널이 열리는(Reveal) 애니메이션이 동시에 교차하며 동작한다.
* **Duration:** 200ms (2 beat)
* **Easing:** Decel
* **적용 속성:** 텍스트 Color/Weight 변경, Underline Color 변경, 패널 Position 및 Opacity 변화

**접근성 (Accessibility)**
* 전체 컨테이너에 `role="tablist"`를 부여하고, 개별 탭 버튼은 `role="tab"`, 콘텐츠 영역은 `role="tabpanel"`을 적용한다.
* 현재 선택된 탭에는 `aria-selected="true"`를, 선택되지 않은 탭에는 `aria-selected="false"`를 적용하여 스크린 리더 사용자에게 상태를 전달한다.

---

#### Navigation Bar

#### Navigation Bar

**정의**
앱 및 모바일 웹 환경에서 사용자가 가장 많이 사용하는 핵심 주요 메뉴들을 담아, 항상 화면 하단에 고정하여 빠른 이동을 지원하는 탐색 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `icon-only`, `icon+label` (기본) |
| Item Count | 3개, 4개, 5개 (최대 5개 제한) |
| State | `unselected` (default), `selected`, `pressed`, `focused` |

**토큰 매핑**
| State | Icon | Label | Background |
|-------|------|-------|------------|
| Default | `color/icon/secondary` | `color/text/body-secondary` | `color/fill/surface/primary` |
| Selected | `color/icon/primary` | `color/text/body` | `color/fill/surface/primary` |

**Usage (구성 및 배치 규칙)**
* ✅ **조합 및 시각적 구분:** 각 메뉴는 반드시 아이콘과 레이블의 조합으로 구성하며, 현재 선택된 메뉴는 다른 메뉴들과 아이콘/텍스트 색상(`Primary` 사용)으로 명확히 시각적으로 구분되게 한다.
* ✅ **하단 고정:** 사용자가 쉽고 빠르게 접근할 수 있도록 항상 화면 최하단에 고정(Sticky) 배치한다.
* ✅ **핵심 기능 제한:** 사용자가 가장 많이 사용하는 주요(Global) 메뉴로만 구성하며, 보조 메뉴는 포함하지 않는다. (메뉴 개수는 3~5개로 제한)
* ✅ **탐색 최적화:** 사용자가 스크롤하며 화면을 넓게 탐색할 때 등 사용자의 행동에 방해가 되지 않도록, 화면 탐색 중에는 선택적으로 사라졌다가(Scroll down) 다시 나타나도록(Scroll up) 구현할 수 있다.

**Usage (텍스트 처리 규칙)**
* ✅ **긴 텍스트 표출:** 메뉴명이 길어질 경우 중앙이 아닌 **상단(Top)을 기준**으로 정렬하여 최대 2줄까지 개행 표출한다.
* ✅ **간결성 유지:** 메뉴명은 최대한 짧고 간결하게 작성하여, 텍스트가 길어져도 인접한 다른 메뉴명과 시각적으로 겹치지 않도록 주의한다.

**모션 (Motion)**
Navigation bar가 표출/미표출되거나 메뉴를 누를 때 부드러운 트랜지션을 제공한다.
* **표출 시 (Enter):** 300ms (3 beat) / Standard_decel (0, 0, 0, 1)
* **미표출 시 (Exit):** 200ms (2 beat) / Standard_decel (0, 0, 0, 1)

**접근성 (Accessibility)**
* 전체 컨테이너는 `<nav>` 태그로 묶고, `aria-label="주요 탐색"` 또는 `aria-label="Global Navigation"` 등의 라벨을 제공한다.
* 현재 선택된 탭 요소에는 `aria-current="page"` 속성을 적용하여 스크린 리더 사용자에게 현재 위치를 명확히 전달한다.

---

#### Top Bar

#### Top Bar

**정의**
웹 페이지 최상단에 배치되며 페이지 제목(Title)과 이전(Back) 버튼 등 주요 탐색 액션을 포함하는 헤더 바 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `default`, `transparent`, `search` |
| Left Action | `back`, `close`, `logo`, `none` |
| Right Action | `icon-buttons`, `text-button`, `none` |
| State | `enabled` (default), `focused & hovered` |

**토큰 매핑**
| Type | Background | Title | Icon |
|------|-----------|-------|------|
| Default | `color/fill/surface/primary` | `color/text/title` | `color/icon/primary` |
| Transparent | transparent | `color/text/inverse` | `color/icon/inverse` |

**Usage (플랫폼 및 배치 규칙)**
* ✅ **플랫폼 환경 구분:** Top Bar는 원칙적으로 **웹(PC 웹, 모바일 웹) 전용 컴포넌트**로 사용한다. 네이티브 모바일 앱(iOS, Android)의 경우 각 OS가 제공하는 기본 시스템 헤더를 우선적으로 사용한다.
* ✅ **상단 고정 (Sticky):** 사용자가 화면을 스크롤하여 페이지 하단으로 이동하더라도 항상 화면 최상단에 고정 표출되어, 언제든 이전 화면으로 돌아가거나 주요 액션을 취할 수 있도록 한다.

**Usage (텍스트 규칙)**
* ✅ **간결한 제목:** 페이지 제목은 현재 화면의 목적을 즉시 파악할 수 있도록 최대한 명확하고 짧게 작성한다.
* ✅ **긴 제목 개행:** 텍스트가 길어져 컨테이너의 허용 너비를 초과하는 경우, 텍스트를 말줄임(...) 처리하지 않고 하단으로 개행하여 전체 제목을 표출한다.

**접근성 (Accessibility)**
* 페이지의 헤더 영역임을 명시하기 위해 컴포넌트 전체를 `<header>` 랜드마크 태그로 감싸 시맨틱 구조를 확보한다.
* 아이콘으로만 구성된 이전(Back) 버튼이나 닫기(Close) 버튼에는 `aria-label="이전 페이지로 이동"` 또는 `aria-label="닫기"` 등 스크린 리더 사용자를 위한 대체 텍스트를 반드시 제공한다.
---

#### LNB (Left Navigation Bar)
#### LNB (Left Navigation Bar)

**정의**
웹 또는 태블릿 환경에서 주로 좌측에 위치하며, 각 페이지의 하위 메뉴들을 계층 구조로 나열하여 탐색을 돕는 로컬 네비게이션 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Mode | `expanded` (확장), `collapsed` (축소) |
| Depth | `1-depth`, `2-depth`, `3-depth`, `4-depth` |
| State | `unselected`, `selected`, `focused & hovered` |

**토큰 매핑**
| State | Background | Text |
|-------|-----------|------|
| Default | `color/fill/canvas/secondary` | `color/text/body` |
| Hovered | `color/fill/surface/tertiary` | `color/text/body` |
| Selected | `color/fill/interaction/selected-item` | `color/text/body` |

**Usage (계층 및 확장 규칙)**
* ✅ **계층 구조 표출:** 각 메뉴는 하위 계층(Depth)을 가질 수 있으며, 하위 메뉴가 존재하는 경우 우측에 `Arrow(화살표)` 아이콘을 표출하여 확장/축소가 가능함을 안내한다.
* ✅ **활성화 상태 유지:** 페이지 이동 및 진입 시, 현재 사용자가 위치한(활성화된) 메뉴를 포함하는 상위 메뉴 뎁스는 기본적으로 '확장된 상태(Expanded)'로 표출하여 현재 위치 맥락을 제공한다.
* ✅ **들여쓰기 (Indentation):** Depth(계층)가 깊어질수록 좌측 여백을 다르게 적용하여 정보의 위계를 시각적으로 명확히 구분한다. (예: 4Depth는 앞선 Depth와 명확히 구분되는 들여쓰기 적용)

**Usage (텍스트 처리 규칙)**
* ✅ **긴 메뉴명 표출:** 메뉴명이 길어 LNB의 최대 너비를 초과하는 경우, 말줄임(...) 처리하지 않고 하단으로 개행하여 전체 메뉴명을 표출한다.

**접근성 (Accessibility)**
* LNB 영역 전체를 `<nav>` 랜드마크 태그로 감싸고, `aria-label="보조 탐색"` 등을 부여하여 메인 네비게이션과 구분한다.
* 하위 메뉴를 여닫는 화살표 버튼에는 상태에 따라 `aria-expanded="true"` 또는 `aria-expanded="false"`를 제공한다.
* 현재 사용자가 위치한 페이지에 해당하는 메뉴 항목에는 `aria-current="page"`를 적용하여 스크린 리더가 현재 위치를 명확히 안내할 수 있도록 한다.
---

#### Menubar

#### Menubar

**정의**
웹 화면 상단에 배치되어 서비스의 주요 카테고리(메인 메뉴 및 서브 메뉴)를 1 Depth 구조로 가로로 나열하는 글로벌 탐색(Global Navigation) 바.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` |
| View Mode | `expanded` (확장/기본), `collapsed` (축소/모바일) |
| State | `unselected` (default), `focused & hovered`, `selected` (active) |

**토큰 매핑**
| State | Background | Text |
|-------|-----------|------|
| Default | `color/fill/surface/primary` | `color/text/body` |
| Hovered | `color/fill/interaction/enabled-menubar` | `color/text/body` |
| Selected (Active) | `color/fill/surface/primary` | `color/text/title` |

**Usage (구성 및 컴포넌트 구분 규칙)**
* ✅ **Chip과의 구분:** Menubar는 '페이지 이동을 위한 링크의 집합'이므로 내부적으로 정보 구조(메인/서브)를 갖는다. 반면, 한 페이지 내에서 콘텐츠를 정렬하거나 뺼/더할 때는 `Chip` 컴포넌트를 사용해야 한다.
* ✅ **배치 구조:** 화면 상단에 가로형(Horizontal)으로 배치되며, 기본적으로 1 Depth 메뉴 구성에 사용한다.

**Usage (텍스트 및 노출 규칙)**
* ✅ **긴 텍스트 표출:** 각 메뉴의 너비는 텍스트 길이에 맞춰 자동 조정(hug)된다. 화면이 좁아 메뉴 텍스트가 최대 허용 너비를 초과할 경우, 영역 안에서 하단으로 개행되어 표출된다.
* ✅ **선택 상태 유지:** 페이지 진입 시, 현재 접속 중인 페이지에 해당하는 메뉴는 시각적으로 선택된(Active) 상태로 항상 화면에 보여야 한다.
* ✅ **반응형 동작:** * **Wide (웹):** 해상도가 충분할 경우 모든 메뉴가 확장된(Expanded) 상태로 넓게 표출된다.
  * **Compact (모바일):** 해상도가 좁아 전체 메뉴를 표출하기 어려운 경우, 초기 상태는 축소(Collapsed) 상태로 제공되며, 사용자가 영역을 좌우로 슬라이드(Swipe)하여 숨겨진 메뉴를 탐색할 수 있도록 한다. 필요한 경우 확장/축소 버튼을 함께 제공한다.

**접근성 (Accessibility)**
* Menubar 영역 전체를 `<nav>` 태그로 감싸고, `aria-label="주요 메뉴"` 등의 역할을 부여한다.
* 내부에 포함된 각 텍스트 요소는 실제 페이지 이동을 담당하므로 `<a>` 태그를 사용한다.
* 현재 위치한 활성 메뉴에는 `aria-current="page"` 속성을 적용하여 스크린 리더 사용자가 현재 위치를 파악할 수 있도록 돕는다.

---

#### Pagination

#### Pagination

**정의**
대량의 데이터나 콘텐츠를 여러 개의 페이지 단위로 분리하여 탐색할 수 있도록 돕는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (일반적인 페이지 이동), `search` (페이지 번호 직접 입력 이동) |
| State | `unselected` (default), `selected` (active), `focused & hovered`, `disabled` |

**토큰 매핑**
| State | Background | Text |
|-------|-----------|------|
| Default | transparent | `color/text/body` |
| Selected | `color/fill/interaction/primary` | `color/text/inverse` |
| Disabled | transparent | `color/text/disabled` |

**Usage (숫자 표출 및 생략 규칙)**
* ✅ **전체 표출:** 전체 페이지 수가 비교적 적은 경우, 말줄임 처리 없이 모든 페이지 숫자를 표출한다.
* ✅ **말줄임 표출:** 전체 페이지 수가 많은 경우 중간 숫자를 말줄임표(`...`)로 축약하여 표시한다. 단, 축약하더라도 **첫 번째 페이지와 마지막 페이지의 숫자는 항상 화면에 표출**해야 한다.
* ✅ **중앙 정렬:** 현재 선택된 페이지(Active)는 페이지를 이동할 때마다 동적으로 변경되며, 가급적 리스트의 중앙에 표출되도록 배치한다.

**Usage (이동 액션 규칙)**
* ✅ **이전/다음 버튼 제어:** 사용자가 첫 번째 페이지에 위치해 있을 때는 '이전(<)' 버튼을 표출하지 않으며, 마지막 페이지에 위치해 있을 때는 '다음(>)' 버튼을 표출하지 않는다.
* ✅ **Search 타입 활용:** 게시판 등 페이지 수가 방대하여 여러 단계를 건너뛰어야 하는 경우, 사용자가 페이지 번호를 직접 입력하여 해당 페이지로 즉시 이동할 수 있는 `Search` 타입을 제공한다.

**접근성 (Accessibility)**
* Pagination 영역 전체를 `<nav>` 랜드마크 태그로 감싸고 `aria-label="페이지 탐색"`(또는 "Pagination") 속성을 부여한다.
* 개별 페이지 번호는 `<a>` 또는 `<button>` 태그를 사용하며, 현재 선택된 페이지 요소에는 `aria-current="page"` 속성을 적용하여 스크린 리더 사용자가 현재 위치를 명확히 인지할 수 있게 돕는다.
* 아이콘으로만 제공되는 이전/다음 버튼에는 `aria-label="이전 페이지"`, `aria-label="다음 페이지"`와 같이 명확한 대체 텍스트를 제공한다.

---

#### Sticky

#### Sticky

**정의**
스크롤에 관계없이 화면 하단에 항상 고정되어, 주요 CTA 버튼과 필수 정보(예: 결제 금액)를 지속적으로 노출하는 컨테이너 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Button Count | `1-button`, `2-button` |
| Button Layout | `horizontal` (수평 배치), `vertical` (수직 배치) |
| Alignment | `center` (Compact), `right` (Wide) |
| Content | `button-only`, `with-info` (금액 등 부가 정보 포함) |

**토큰 매핑**
| 영역 | 토큰 |
|------|------|
| Background | `color/fill/surface/primary` |
| Top Border | `color/border/divider-primary` |

**Usage (적용 범위 및 목적)**
* ✅ **적용 영역:** 기본 페이지(Page)뿐만 아니라 모달(Dialog), 바텀 시트(Bottom Sheet) 등 다양한 환경에서 최하단에 고정하여 사용한다.
* ✅ **사용 목적:** 항공권 구매, 회원 로그인 등 전환율(Conversion)이 중요한 단계에서 다음 단계로 넘어가는 CTA를 사용자가 항상 인지하고 클릭할 수 있도록 제한적으로 사용한다. 결제 금액 등 필수 확인 정보를 함께 배치할 수 있다.

**Usage (정렬 및 레이아웃 규칙)**
* ✅ **해상도별 정렬:** Compact(모바일) 환경에서는 버튼을 **중앙 정렬**하고, Wide(웹/태블릿) 환경에서는 콘텐츠 너비를 기준으로 **우측 정렬**한다.
* ✅ **버튼 배치 전환:** * 버튼이 1개일 때는 단독으로 꽉 채워 배치한다.
  * 버튼이 2개일 때는 **수평(Horizontal) 배치**를 원칙으로 한다. (예: 좌측 Secondary, 우측 CTA)
  * 단, 2개의 버튼을 사용할 때 레이블 텍스트가 길어져 컴포넌트 영역을 초과할 우려가 있는 경우, **수직(Vertical) 배치**로 전환하여 레이아웃이 깨지지 않도록 한다.

**Usage (텍스트 처리 규칙)**
* ✅ **긴 텍스트(금액) 표출:** 결제 금액과 같이 자리수가 큰 숫자를 표출할 때 텍스트 영역이 좁다면, 숫자를 임의로 자르지 않고 '금액 단위'를 기준으로 하단으로 개행하여 가독성을 유지한다.

**접근성 (Accessibility)**
* 스크린 리더 사용자가 해당 영역이 고정된 CTA 영역임을 인지할 수 있도록 적절한 랜드마크(예: `<aside>` 또는 `<div role="region">`)를 사용하고 `aria-label="주요 액션"` 등을 부여한다.
* 탭(Tab) 키 탐색 시 페이지의 메인 콘텐츠를 먼저 탐색한 후 Sticky 영역의 액션 버튼으로 포커스가 논리적으로 이동하도록 DOM 순서(DOM order)를 구성한다.

---

### 3.4 피드백 (Feedback)

---

#### Badge

#### Badge

**정의**
서비스의 현재 상태, 티켓의 특징, 또는 분류 키워드 등의 부가 정보를 사용자가 직관적이고 빠르게 인식할 수 있도록 돕는 시각적 인디케이터 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic`, `using-state`, `booking`, `extra` |
| Semantic State | `positive` (성공/완료), `neutral-positive` (일부 완료/진행), `neutral-negative` (대기/추가 작업), `negative` (실패/오류), `none` |
| Background Variant| `100`, `200` (배경색에 따른 가독성 보정용) |

**토큰 및 색상 매핑 (상태별 기본)**
| State | 의미 |
|-------|------|
| Positive | Task가 성공적으로 완료되어 모든 프로세스가 끝난 긍정 상태 |
| Neutral-positive | Task가 일부만 완료되었거나, 완료되지 않았지만 긍정(Positive)에 가까운 상태 |
| Neutral-negative | 대기해야 하거나 추가 작업을 수행해야 하는 부정(Negative)에 가까운 상태 |
| Negative | Task가 실패했거나 완료하지 못한 부정 상태 |
| 좌석 등급 (Extra) | 이코노미(Grey/White), 프레스티지(`color/fill/surface/prestige`), 프리미엄(`color/fill/surface/premium`) 등 지정된 토큰 사용 |

**Usage (타입별 사용 목적 및 구성 규칙)**
* ✅ **Basic (운항 상태):** 이륙 대기, 지연, 결항 등 '항공편 운항 현황'을 나타낼 때 사용한다. 시각적 인지를 돕는 **아이콘과 컨테이너 색상**을 조합하여 표출한다.
* ✅ **Using state (사용자 관점 상태):** 구매 내역, 예약 목록 등 '사용자 관점의 서비스 상태'를 나타낼 때 사용한다. 컨테이너(배경) 없이 **텍스트 색상**만으로 상태를 표현한다.
* ✅ **Booking (예매 특징):** 예매 플로우에서 '최저가' 등 항공권의 특징을 표시할 때 사용한다. 텍스트가 길어져도 개행되지 않고 **가로 너비가 확장**되는 것이 특징이다.
* ✅ **Extra (일반 정보):** 마일리지 몰 상품, 기내식 키워드 등 일반적인 정보나 기업 관점의 상태를 나타낼 때 사용한다. 아이콘을 사용하지 않으며, 의미에 따라 상태 지정 색상을 예외적으로 따르지 않고 단순 포인트 컬러로 활용할 수 있다.

**Usage (레이블 및 텍스트 규칙)**
* ✅ **레이블 작성:** Badge 1개당 1개의 상태만 명사형 단어 조합으로 간결하게 작성한다. (여러 단어 나열 금지, 문장형 작성 금지, 임의의 붙여쓰기 금지)
* ✅ **긴 텍스트 개행:** 텍스트는 최대 2줄까지 작성할 수 있으며, 허용 너비를 초과하면 띄어쓰기 단위로 개행된다. (단, Booking 타입은 개행 없이 가로로 확장됨)

**Usage (레이아웃 및 접근성 규칙)**
* ✅ **가독성 보정 (대비):** Badge가 놓이는 배경색(White 또는 Gray)에 따라 가독성이 떨어질 수 있으므로, 명도 대비를 고려하여 알맞은 배경 Variant(100 또는 200)를 선택 적용한다.
* ✅ **부가 설명 (Tooltip):** * **Compact (모바일):** 공간 제약을 고려하여 Badge 우측에 `Tooltip` 아이콘을 배치하여 추가 정보를 표출한다.
  * **Wide (웹):** Tooltip을 사용하지 않고 Badge 하단에 직접 텍스트 문구로 부가 설명을 표출한다.
* ✅ **접근성:** 색상에만 의존하여 정보를 전달하지 않도록, Basic 타입에서는 아이콘을 병행하여 접근성을 높인다.

---

#### Chip

#### Chip

**정의**
여러 개의 옵션 중에서 하나 또는 여러 개를 선택하여, 한 화면 내의 콘텐츠를 필터링하거나 정렬할 때 사용하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (다중 선택), `single` (단일 선택) |
| State | `unselected` (default), `selected`, `focused & hovered`, `disabled` |
| Background | `white`, `gray` (배치되는 배경에 따라 선택 적용) |
| Feature | `leading-icon`, `select-all` (Basic 전용) |

**Usage (선택 및 탐색 규칙)**
* ✅ **기본 선택 상태:** `Basic` 타입은 처음에 아무것도 선택되지 않은(모두 해제된) 상태로 제공될 수 있으나, `Single` 타입은 구조상 반드시 하나의 옵션이 디폴트로 선택되어 있어야 한다.
* ✅ **전체 선택:** 다중 선택 기능인 `Basic` 타입에서는 '전체 선택' 칩을 제공할 수 있으며, 클릭 시 전체 선택 및 전체 해제가 토글되도록 동작한다.
* ✅ **슬라이드 탐색:** 칩의 개수가 많아 화면 너비를 초과하는 경우, 축소된 상태를 유지하되 사용자가 좌우로 슬라이드(Swipe)하여 숨겨진 칩을 탐색할 수 있도록 제공한다.

**Usage (시각 및 텍스트 규칙)**
* ✅ **아이콘 일관성:** 칩 텍스트를 보조하기 위해 텍스트 앞에 아이콘(Leading icon)을 사용할 수 있다. 단, 하나의 칩 그룹 안에서는 아이콘을 모두 적용하거나 모두 생략하는 식으로 통일해야 하며 혼용해서는 안 된다.
* ✅ **긴 텍스트 표출:** 칩 내부의 텍스트가 최대 허용 너비를 초과하여 길어질 경우, 영역 안에서 하단으로 개행하여 표출한다.
* ✅ **배경색 맞춤:** 칩이 배치되는 부모 컨테이너의 배경 색상(White 또는 Gray)에 맞춰 묻히지 않도록 적절한 스타일 옵션을 적용한다.

**접근성 (Accessibility)**
* **Basic (다중 선택):** `<input type="checkbox">`와 동일한 마크업 구조를 사용한다. 개별 칩의 상태는 `aria-checked="true"` 또는 `false`로 전달한다.
* **Single (단일 선택):** `<input type="radio">` 요소와 동일한 마크업을 사용하며, 동일한 `name` 그룹으로 묶어준다.
* **키보드 제어 (WCAG 2.1.1):** 키보드의 `Tab` 이동 및 `Space` (또는 `Enter`) 키를 통해 마우스 클릭과 동일하게 칩을 선택하고 해제할 수 있어야 한다. Single 타입의 경우 방향키를 이용한 탐색을 지원한다.
---

#### Notice Bar

#### Notice bar

**정의**
사용자에게 현재 화면이나 시스템의 중요한 상태, 알림, 공지 등을 전달하기 위해 짧은 문구 또는 문장으로 구성된 가로형 피드백 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (일반 정보 안내), `notification` (홈 상단 중요 공지/알림) |
| Status | `neutral` (일반/정보), `warning` (주의/경고), `negative` (중요/긴급), `positive` (성공/안전) |
| Size (Basic) | `md` (기본), `sm` (보조 설명용) |
| Background Variant| `100`, `200` (배경색에 따른 가독성 보정용) |

**토큰 매핑 (Status 기반)**
| Status | Background (Variant 200 예시) | Icon / Text Emphasis |
|--------|------------------------------|----------------------|
| Neutral | `color/fill/surface/secondary` | `color/text/body-secondary` |
| Warning | `color/fill/surface/warning` | `color/text/warning` |
| Negative | `color/fill/surface/negative` | `color/text/negative` |
| Positive | `color/fill/surface/positive` | `color/text/positive` |

**Usage (유형 및 배치 규칙)**
* ✅ **Basic:** 페이지 콘텐츠 내에서 정보 및 제약 사항을 안내할 때 사용한다. 콘텐츠의 맥락에 따라 상단 또는 하단(데이터 테이블 부가 설명 등)에 배치한다.
* ✅ **Notification:** 홈 화면 최상단에 고정하여 중요한 공지를 전달할 때 사용한다. (동시에 최대 3개까지 노출 가능하며 `Negative` > `Warning` > `Neutral` 순으로 정렬한다.)
* ✅ **너비:** 컨텐츠 영역의 전체 너비(Full Width)에 꽉 차게 적용하며, 임의로 좁게 사용하지 않는다.
* ✅ **가독성 보정:** Notice Bar가 놓이는 배경이 White인지 Gray인지에 따라 컴포넌트의 배경색상(Variant)을 달리하여 명확한 대비를 준다.

**Usage (텍스트 및 기능 규칙)**
* ✅ **긴 텍스트 표출:** 텍스트가 길어지면 아이콘은 최상단에 고정된 상태에서 텍스트만 우측에서 줄바꿈(개행)되어 표출된다. Notification 타입은 텍스트를 간략히 노출하고, 클릭 시 바텀 시트(Bottom Sheet) 등으로 상세 내용을 제공할 수 있다.
* ✅ **링크 사용 제한:** Basic 타입은 텍스트 중간에 페이지 이동을 위한 텍스트 링크(Link)를 포함할 수 있으나, **Notification 타입은 내부에 링크를 사용할 수 없다.**
* ✅ **닫기(X) 버튼:** Notification 타입은 우측에 닫기(Close) 버튼을 제공하며, 컨테이너 높이의 중앙에 정렬한다.

**접근성 (Accessibility)**
* 중요도나 알림의 성격에 따라 `role="alert"` (긴급/오류), `role="status"` (일반 안내)를 적용하여 스크린 리더가 즉각적으로 상황을 읽어줄 수 있도록 한다.
* Notification의 닫기 버튼에는 `aria-label="알림 닫기"` 등 명확한 대체 텍스트를 제공한다.
---

#### Snack Bar

#### Snack bar

**정의**
사용자의 액션에 대한 간단한 피드백이나 부가적인 메시지를 화면 하단(또는 상단)에 오버레이 형태로 일시적으로 제공하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Position | `bottom` (모바일 및 기본), `top` |
| State | `default` (enabled), `focused` (닫기 버튼 포커스) |

**토큰 매핑**
| 영역 | 색상 적용 기준 |
|------|--------------|
| Background | 배경 컨텐츠와 시각적으로 명확히 구분되는 어두운 Neutral 계열 색상 적용 (명도비 4.5:1 준수) |
| Text / Icon | `color/text/inverse`, `color/icon/inverse` (어두운 배경에 대비되는 밝은 색상) |

**Usage (적용 범위 및 배치 규칙)**
* ✅ **사용 목적:** '복사 완료', '공유 완료' 등 빠르고 간단한 작업 완료 피드백이나 가벼운 Follow-up 안내에 사용한다. (사용자가 반드시 인지하고 조작해야 하는 중요/복잡한 피드백은 `Dialog`, `Result box`, `System message`로 대체한다.)
* ✅ **단일 표출:** 한 화면에 여러 개의 Snack bar를 동시에 겹쳐서 표출하지 않으며, 한 번에 1개만 표출한다.
* ✅ **FAB와의 간격:** 화면 하단에 FAB(Floating Action Button)가 함께 존재하는 경우, FAB와 겹치지 않도록 20px의 간격을 두고 안전하게 표출한다.
* ✅ **색상 제한:** 다양한 화면 위에 오버레이되므로 시각적 방해를 최소화하기 위해 기본(Neutral) 어두운 색상만 사용한다. (의미 부여를 위한 다른 Semantic 색상 혼용 금지)

**Usage (텍스트 및 동작 규칙)**
* ✅ **간결한 텍스트:** 핵심 내용만 최대한 간결하게 작성하며, 텍스트가 길어지더라도 최대 2줄 이내로 표출되도록 제한한다.
* ✅ **자동 숨김 (Auto-dismiss):** 액션 직후 표출되며, 사용자가 직접 닫지 않아도 문구의 양에 따라 설정된 시간(최소 4초 ~ 최대 10초)이 지나면 자동으로 사라진다.
* ✅ **사용자 제어 보장:** 사용자가 즉시 닫을 수 있도록 우측에 `닫기(X)` 버튼을 제공한다. 사용자가 Snack bar 영역에 마우스를 올리거나(Hover) 키보드 포커스가 이동하면, 내용 확인을 위해 타이머가 일시 정지되어 자동으로 사라지지 않아야 한다.

**모션 (Motion)**
* **Enter (표출):** 300ms (3 beat) / Easing: decel / Position Up
* **Exit (숨김):** 200ms (2 beat) / Easing: decel / Position Down
* **Delay (유지):** 4,000ms ~ 10,000ms (기획에 따라 동적 설정)

**접근성 (Accessibility)**
* 일시적인 피드백 메시지이므로 스크린 리더가 즉각적으로 읽어줄 수 있도록 컨테이너에 `role="status"`(일반 알림) 또는 `role="alert"`(중요 알림) 속성을 적용한다.
* 화면의 DOM에 동적으로 추가/삭제되므로 `aria-live="polite"`를 통해 사용자 조작을 방해하지 않고 자연스럽게 메시지를 전달한다.
* 우측의 닫기(X) 버튼에는 `aria-label="알림 닫기"` 등의 대체 텍스트를 반드시 제공하여 스크린 리더 사용자의 명확한 조작을 지원한다.
---

#### Tooltip

#### Tooltip

**정의**
특정 UI 요소에 대한 부가적인 설명이나 아이콘의 의미를 말풍선 형태로 화면 위에 띄워 일시적으로 제공하는 피드백 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (일반적인 부가 설명), `amenity` (특정 부가서비스/아이콘 의미 설명) |
| Placement | `top` (기본), `bottom` |
| Pointer Position| `center` (기본), `left`, `right` |
| Background | `dark` (기본), `white` (어두운 배경 위 표출 시) |

**Usage (아이콘 및 위치 규칙)**
* ✅ **트리거 아이콘:** `Basic` 타입의 툴팁을 띄우는 트리거 버튼은 반드시 **물음표(?) 아이콘**만 사용하며, 임의의 다른 아이콘을 혼용하지 않는다.
* ✅ **표출 방향:** 말풍선이 나타나는 기본 위치는 아이콘의 위쪽(`Top`)이며, 화면 상단 여백이 부족할 경우 아래쪽(`Bottom`)으로 자동 변경된다.
* ✅ **Pointer(꼬리) 위치:** 말풍선 꼬리의 기본 위치는 툴팁 너비의 중앙(`Center`)이다. 단, 툴팁이 화면 좌우 가장자리에 닿을 경우 화면 밖으로 잘리지 않도록 꼬리의 위치를 `Left` 또는 `Right`로 가변하여 적용한다.
* ✅ **고정 간격:** 트리거 아이콘과 툴팁 말풍선 사이의 간격은 디바이스 해상도와 관계없이 항상 **8px**로 고정한다.

**Usage (콘텐츠 및 텍스트 규칙)**
* ✅ **간결한 구성:** 최대한 간결한 문장으로 작성하며, 문구가 복잡할 경우 선택적으로 `Title`을 함께 사용할 수 있다.
* ✅ **내부 컴포넌트 조합:** 내용이 길거나 정보의 구조화가 필요한 경우, 가독성을 높이기 위해 툴팁 내부에 `List`, `Paragraph`, `Divider` 컴포넌트를 조합하여 사용할 수 있다.
* ❌ **인터랙션 요소 금지:** 툴팁은 순수 정보 제공용이므로, 내부에 `Link`나 `Button` 등 사용자가 클릭해야 하는 인터랙티브 요소를 절대 포함하지 않는다. 복잡한 도식화도 지양한다.
* ✅ **긴 텍스트 개행:** 텍스트 길이에 따라 너비가 유동적으로 변하며, 뷰포트 기준 최대 허용 너비를 초과하면 하단으로 자동 개행된다 (최대 2줄 권장).

**Usage (가독성 및 동작 규칙)**
* ✅ **배경색 대비:** 툴팁이 띄워지는 바닥 배경이 White가 아닌 유색(Gray 등)일 경우, 시각적 대비와 가독성을 확보하기 위해 `White` 컬러의 툴팁을 사용한다.
* ✅ **스크롤 대응:** 툴팁이 열려있는 상태에서 스크롤이 발생할 경우, 툴팁이 스크롤을 따라가게 하거나 화면에 고정(Floating)하여 콘텐츠가 잘 보이지 않는 현상을 방지한다.

**접근성 (Accessibility)**
* 툴팁을 띄우는 트리거 요소(버튼)에는 `aria-describedby` 속성을 부여하고, 툴팁 컨테이너의 `id`와 연결하여 스크린 리더 사용자가 해당 요소에 포커스 했을 때 툴팁 내용을 읽을 수 있도록 구성한다.
* 툴팁 컨테이너 자체에는 `role="tooltip"`을 부여한다.
* 키보드 `Tab` 이동을 통해 트리거 요소에 포커스가 갔을 때도 마우스 Hover와 동일하게 툴팁이 표출되어야 한다.
---

#### Dialog

#### Dialog

**정의**
현재 화면 위에 떠 있는(Overlay) 형태로 나타나며, 사용자의 주의를 집중시키고 중요한 선택이나 액션을 요구할 때 사용하는 컨테이너 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic`, `full`, `overlay` (웹 전용), `alert` (경고/오류용) |
| Modality | `modal` (배경 차단), `non-modal` (배경 조작 가능) |
| Size (Basic) | `sm` (400~522px), `md` (768px), `lg` (940px) |

**토큰 매핑**
| 영역 | 토큰 |
|------|------|
| Container Background | `color/fill/surface/primary` |
| Dimmed Background (Modal) | `color/fill/interaction/dimmed` (투명도 포함) |
| Title | `color/text/title` |

**Usage (유형 및 목적 규칙)**
* ✅ **Bottom sheet와의 구분:** 주요 Task 단계에서 **반드시 선택이나 제어가 필요할 때** Dialog를 사용한다. (단순 부가 정보 제공이나 흐름을 끊지 않는 탐색은 `Bottom sheet`를 사용한다.)
* ✅ **Modal vs Non-modal:** * `Modal`: 배경 콘텐츠가 비활성화(Dimmed)되고 인터랙션이 차단되며, 스크롤이 Dialog 내부에서만 발생한다. 중요한 선택 시 사용한다.
  * `Non-modal`: 배경 콘텐츠가 활성화되어 상호작용 가능하며, 부모 페이지와 함께 스크롤된다. 추가 옵션 탐색 시 사용한다.
* ✅ **Alert:** 사용자의 흐름을 전면 차단해야 하는 심각한 오류나 필수 확인 알림의 경우 `Alert` 타입을 사용한다.
* ❌ **중복 표출 금지:** Dialog 위에 또 다른 Dialog를 띄우는 등 중복 표출을 금지한다. 여러 단계가 필요하다면 Flow(단계 전환) 화면으로 구성한다.

**Usage (텍스트 및 정렬 규칙)**
* ✅ **간결한 제목:** 사용자가 본문을 모두 읽지 않아도 목적을 파악할 수 있도록 제목은 짧고 명확하게 작성한다.
* ✅ **본문 정렬:** 내용이 2~3줄 이내로 매우 짧은 경우 제목을 생략하거나 중앙 정렬(Center)로 강조할 수 있으나, 문장이 길어질 경우 중앙 정렬을 사용하지 않는다.

**Usage (해상도 및 반응형 규칙)**
* **Basic Type:**
  * `Compact` (모바일): 하단에서 올라오는 **Bottom sheet** 형태로 전환하여 표출한다.
  * `Wide` (웹): 화면 중앙에 모달 형태로 띄운다. (sm, md, lg 사이즈 적용)
* **Full Type:**
  * `Compact` (모바일): 여백 없이 화면 전체를 빈틈없이 채우거나 Bottom sheet 형태로 표출한다.
  * `Wide` (웹): 화면 상하좌우에 60px의 여백을 둔 중앙 모달 형태로 표출한다.
* **Overlay Type:**
  * `Wide` (웹) 환경에서만 사용하며, 메인 콘텐츠 영역(789px)과 우측 사이드바 영역(379px)을 고정값으로 나란히 배치한다.
* **Alert Type:**
  * `Compact` (모바일): 좌우 20px 마진을 제외하고 꽉 차게 표출한다.
  * `Wide` (웹): 최대 너비 768px로 제한하여 화면 중앙에 표출한다.

**접근성 (Accessibility)**
* 컨테이너에 `role="dialog"`를 부여하고, Alert 타입의 경우 `role="alertdialog"`를 부여하여 스크린 리더에 심각성을 알린다.
* 모달(`Modal`) 형태인 경우 `aria-modal="true"`를 적용하고, 키보드 `Tab` 포커스가 Dialog 외부(배경)로 빠져나가지 않도록 포커스 트랩(Focus Trap)을 반드시 구현한다.
* `aria-labelledby`(제목 연결)와 `aria-describedby`(본문 연결) 속성을 사용하여 Dialog가 열렸을 때 스크린 리더가 내용을 즉시 읽을 수 있도록 한다.
---

#### Bottom Sheet

#### Bottom sheet

**정의**
모바일(Compact) 환경에서 화면 하단에서 위로 슬라이드 되어 나타나며, 메인 Task를 보조하는 부가적인 정보나 추가 옵션을 제공하는 오버레이 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `default`, `flow` (여러 단계의 흐름을 가질 때) |
| Modality | `modal` (배경 차단), `non-modal` (배경 조작 가능) |
| Content Scroll| `scrollable` (콘텐츠가 많을 경우 내부 스크롤 허용) |

**Usage (유형 및 목적 규칙)**
* ✅ **Dialog와의 구분:** 사용자의 흐름을 전면 차단하고 반드시 선택을 요구하는 중요한 알림은 `Dialog`를 사용한다. 반면, 현재 화면의 흐름을 유지한 채 부가적인 정보를 확인하거나 추가 옵션을 선택할 때는 `Bottom sheet`를 사용한다.
* ✅ **Modal vs Non-modal:** * `Modal`: 메인(배경) 콘텐츠가 비활성화(Dimmed)되며 상호작용이 불가능하다.
  * `Non-modal`: 메인 콘텐츠가 활성화 상태를 유지하며 상호작용 및 스크롤이 가능하다.
* ❌ **중복 표출 금지:** 한 번에 하나의 Bottom sheet만 표출하며, 중복해서 띄우지 않는다.

**Usage (레이아웃 및 스크롤 규칙)**
* ✅ **전체 화면 비율 제한:** Bottom sheet가 열려도 화면 상단의 Status bar 영역까지 모두 덮지 않도록 최대 높이를 제한한다.
* ✅ **내부 스크롤 고정:** 내부 콘텐츠가 많아 스크롤이 발생하더라도, 상단의 헤더(제목, 이전/닫기 버튼)와 하단의 고정 버튼(CTA) 영역은 항상 제자리에 고정(Sticky)되어 표출되어야 한다.
* ✅ **닫기 수단:** 우측 상단의 `닫기(X)` 버튼을 제공하며, Modal 타입의 경우 배경 딤(Dimmed) 영역을 탭하여 닫을 수 있도록 지원한다.
* ✅ **Flow 타입:** 여러 단계(Step)를 가지는 흐름일 경우, 헤더 좌측에 `이전(<)` 버튼을, 중앙에 제목을, 우측에 `닫기(X)` 버튼을 배치한다.

**Usage (반응형 규칙)**
* ✅ **해상도 전환:** 모바일(Compact) 해상도에서 Bottom sheet로 표출되던 콘텐츠는, 웹/태블릿(Wide) 해상도에서는 화면 중앙에 뜨는 `Dialog` 형태로 전환되어 표출된다.

**접근성 (Accessibility)**
* `role="dialog"`와 `aria-modal="true"`(모달인 경우)를 부여하여 화면 위에 떠 있는 독립적인 영역임을 스크린 리더에 알린다.
* 키보드 및 스크린 리더 포커스가 Bottom sheet 내부로 이동해야 하며, 모달 타입의 경우 닫히기 전까지 배경으로 포커스가 빠져나가지 않도록 포커스 트랩(Focus Trap)을 적용한다.
* `닫기(X)` 버튼에는 `aria-label="닫기"` 대체 텍스트를 반드시 제공한다.
* 키보드 사용자를 위해 `ESC` 키를 눌렀을 때 Bottom sheet가 닫히도록 단축키를 지원한다.

---

#### Progress Indicator

#### Progress Indicator

**정의**
사용자가 여러 단계로 나뉜 복잡한 프로세스나 긴 흐름을 진행할 때, 현재 위치와 전체 흐름(완료/남은 단계)을 시각적으로 파악하고 이동할 수 있도록 돕는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| View Mode | `number-only` (모바일/Compact), `number + label` (웹/Wide) |
| Step State | `current` (현재 진행), `completed` (완료됨), `incompleted` (미완료/진행 예정) |
| Step Count | 최소 3단계 ~ 최대 5단계 권장 |

**토큰 매핑**
| State | Indicator Background | Text / Label |
|-------|----------------------|--------------|
| Current | `color/fill/interaction/primary` | `color/text/inverse` (번호), `color/text/title` (라벨) |
| Completed | `color/fill/surface/secondary` | `color/text/body` |
| Incompleted | `color/fill/interaction/disabled` | `color/text/disabled` |
| Line (연결선) | `color/border/disabled` (미완료/기본), `color/border/primary` (완료 구간) |

**Usage (적용 단계 및 기준)**
* ✅ **사용 범위:** 화면 전환이 발생하는 3단계 이상의 프로세스에서 사용한다. (단순한 1~2단계 작업에서는 사용하지 않으며, 6단계 이상인 경우 프로세스를 재설계하여 5단계 이하로 축소할 것을 권장한다.)
* ✅ **위치:** 항상 페이지 `Heading(제목)`의 바로 하단에 좌측 정렬로 배치하며, 임의로 위치를 변경하지 않는다.

**Usage (텍스트 및 반응형 규칙)**
* ✅ **텍스트 노출:** * `Wide` (웹): 공간이 충분하므로 숫자가 포함된 인디케이터와 함께 각 단계의 **레이블(텍스트)**을 명확하게 제공한다.
  * `Compact` (모바일): 공간 제약을 고려하여 레이블을 생략하고 **숫자 인디케이터**만 간략히 제공한다.
* ✅ **긴 텍스트 표출 (Wide):** 레이블 텍스트가 길어지면 개행(최대 2줄 권장)하여 표출하되, 각 단계의 가로 너비 비율은 동일하게 유지하고 높이만 유동적으로 늘어난다.

**Usage (탐색 및 상호작용 규칙)**
* ✅ **단계 이동:** 이미 진행을 완료한 이전 단계(`Completed`)는 클릭하여 해당 단계로 되돌아갈 수 있도록 이동 기능을 제공한다. 단, 아직 도달하지 않은 미래의 단계(`Incompleted`)는 클릭할 수 없도록 차단한다.

**접근성 (Accessibility)**
* 전체 컨테이너에 `role="navigation"`과 `aria-label="진행 단계"`를 부여한다.
* 개별 단계에는 `aria-current="step"` (현재 단계) 및 `aria-disabled="true"` (미완료 단계) 속성을 동적으로 적용하여 스크린 리더 사용자가 전체 프로세스 중 현재 어느 위치에 있는지 명확히 파악할 수 있도록 돕는다.
* 완료된 단계는 `<a>` 또는 `<button>` 태그를 사용하여 키보드로 포커스 및 이동이 가능하게 구현한다.
---

#### System Message

#### System message

**정의**
시스템 오류, 작업 차단 등 긴급하고 중대한 상태 정보를 아이콘과 텍스트로 구성하여 화면 최상단에 고정 표출하는 알림 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (텍스트 안내), `link` (해결 페이지로 이동하는 링크 포함) |
| State | `enabled` (default), `focused` (전체 포커스), `focused-link` (내부 링크 포커스) |

**토큰 매핑**
| 영역 | 토큰 |
|------|------|
| Background | `color/fill/surface/negative` |
| Text | `color/text/negative` |
| Icon | `color/icon/negative` |

**Usage (표출 및 유지 규칙)**
* ✅ **제한적 사용:** 사용자의 정상적인 Task 진행을 전면으로 방해하는 매우 중요한 정보이므로, 시스템 에러나 불가피한 차단 상황에서만 제한적으로 사용한다.
* ✅ **단일 표출:** 하나의 Task나 화면에는 단 한 개의 시스템 메시지만 표출하며, 2개 이상을 중복해서 띄우지 않는다.
* ✅ **유지 (No Auto-dismiss):** Snack bar와 달리 일정 시간이 지나도 자동으로 사라지지 않는다. 사용자가 해당 오류 조건을 해결하거나 다른 Task로 강제 전환할 때까지 화면에 계속 유지되어야 한다.
* ✅ **위치 및 너비:** 사용자가 즉시 인지할 수 있도록 페이지 또는 콘텐츠 영역의 최상단(Top)에 배치하며, 콘텐츠 레이아웃 너비(Full Width)와 동일하게 꽉 차게 표출한다. 하단 배치는 금지한다.

**Usage (텍스트 규칙)**
* ✅ **긴 텍스트 표출:** 텍스트 내용이 길어질 경우 하단으로 개행되며, 이때 좌측의 알림 아이콘은 텍스트의 중앙이 아닌 **좌측 상단(Top-left) 정렬**을 유지한다.
* ✅ **Link 포함:** 오류 해결을 위한 액션이나 상세 페이지 안내가 필요한 경우, 텍스트 문장의 끝부분에 밑줄(Underline)이 포함된 `Link`를 사용할 수 있다.

**접근성 (Accessibility)**
* 시스템 수준의 긴급한 오류이므로 컨테이너에 `role="alert"` 속성을 부여하여 스크린 리더 사용자가 화면에 진입하자마자 즉각적으로 오류 상황을 인지할 수 있도록 구현한다.
* 내부에 링크(`Link`)가 포함된 경우, `Tab` 키로 탐색 시 해당 링크로 포커스가 명확히 진입하고 이동할 수 있어야 한다.

---

#### Nudge

#### Nudge

**정의**
사용자가 특정 기능이나 혜택을 인지하고 액션을 취하도록 유도하기 위해, 버튼 등 클릭 가능한 요소 근처에 띄우는 말풍선 형태의 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Placement | `top`, `bottom` |
| Pointer Position| `center` (기본), `left`, `right` |

**토큰 매핑**
| 영역 | 토큰 |
|------|------|
| Background | `color/fill/interaction/primary` |
| Text | `color/text/inverse` |

**Usage (적용 범위 및 목적)**
* ✅ **목적 및 성격:** 사용자가 혜택을 놓치지 않도록 액션을 유도(Nudging)하는 역할을 한다. **조건을 충족하여 한 번 닫히면 다시 볼 수 없으므로, 서비스 이용에 필수적인 중요한 정보는 담지 않는다.**
* ✅ **단일 표출:** 사용자의 화면 탐색 흐름을 방해하지 않도록 한 화면에 1개만 표출한다.
* ✅ **배치 위치:** 화면에 배치된 다른 콘텐츠 영역을 심하게 가리지 않도록 주의하며, 가리키고자 하는 대상 컴포넌트의 상단(`top`) 또는 하단(`bottom`)에 배치한다.

**Usage (텍스트 및 내부 요소 규칙)**
* ✅ **간결성:** 긴 텍스트로 인해 줄바꿈(개행)이 일어나지 않도록, 한 줄로 매우 짧고 직관적인 문구를 작성한다.
* ✅ **강조:** 텍스트 내에서 특히 강조하고 싶은 키워드가 있다면 Bold 처리를 사용할 수 있다.
* ❌ **인터랙션 요소 금지:** Nudge 자체가 클릭을 유도하기 위한 보조 장치이므로, Nudge 말풍선 내부에 별도의 텍스트 링크(Link)나 닫기(X) 버튼을 포함하지 않는다. (조건 충족 시 자동 닫힘)

**Usage (꼬리 위치 규칙)**
* ✅ **Pointer 가변 적용:** Pointer(꼬리)의 기본 위치는 말풍선 너비의 중앙(`center`)이다. 하지만 Nudge가 화면 가장자리에 위치하거나 대상 컴포넌트의 위치가 치우쳐 있을 경우, 시각적인 어색함을 없애기 위해 꼬리의 위치를 `left` 또는 `right`로 가변 조정하여 사용한다.

**접근성 (Accessibility)**
* 동적으로 표출되는 요소이므로 `aria-live="polite"`를 적용하여 스크린 리더가 자연스럽게 읽어주도록 한다.
* Nudge가 가리키는 대상 버튼(또는 요소)에 `aria-describedby` 속성을 부여하고 Nudge의 `id`와 연결하여, 사용자가 대상 요소에 포커스 했을 때 유도 메시지를 함께 인지할 수 있도록 구성한다.

---

#### Result Box

#### Result box

**정의**
사용자가 요청한 작업의 최종 결과(성공, 실패, 부분 완료) 또는 데이터가 없는 상태(Empty state)를 아이콘과 텍스트의 조합으로 화면 중앙에 명확하게 안내하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Size | `sm` (다른 콘텐츠와 병렬 표출 시), `lg` (단독 표출 시) |
| Layout (방향) | `vertical` (Compact/Wide 공통), `horizontal` (Wide 전용) |
| Status | `positive`, `neutral-negative`, `negative`, `empty` |

**토큰 매핑 및 상태 정의**
| Status | 의미 | 아이콘 / 색상 |
|--------|------|-------------|
| Positive | Task가 성공적으로 완료됨 | 지정된 완료 아이콘 / `Green 100` (`color/fill/surface/positive`) |
| Neutral-negative | 체크인 일부 완료 등 부분적/중립적 부정 | 맥락에 맞는 아이콘 / `Orange 100` (`color/fill/surface/warning`) |
| Negative | Task가 완전히 실패했거나 시스템 오류 | 지정된 에러 아이콘 / `Red 100` (`color/fill/surface/negative`) |
| Empty | 404 에러, 검색/예약 결과 없음 | 검색, 장바구니 등 맥락에 맞는 아이콘 / `Neutral 70` (`color/text/body-secondary`) |

**Usage (구성 및 텍스트 규칙)**
* ✅ **Title 작성:** 제목(Title)은 결과를 한 문장으로 짧고 간결하게 작성하며, 끝에 **온점(.)을 사용하지 않는다.**
* ✅ **Description 작성:** 제목만으로 부족한 부가 설명이나, 사용자가 취해야 할 '다음 액션 가이드'를 보조 텍스트(Description)로 제공한다. (예: 404 에러 시 브라우저 새로고침, URL 재확인 등 안내)
* ✅ **텍스트 개행:** 다국어 환경 등 텍스트가 길어져 최대 너비를 초과할 경우 **단어 단위**로 줄바꿈(개행)하며 말줄임표(...)는 사용하지 않는다. 이때 아이콘과 텍스트 영역은 수직/수평 중앙에 정렬된다.

**Usage (아이콘 선택 규칙)**
* ✅ `Positive`와 `Negative` 상태는 사전에 디자인 시스템에 지정된 고정 아이콘을 사용한다.
* ✅ `Empty` 상태는 사용자가 처한 맥락(검색 결과 없음, 예약 없음, 쿠폰 없음 등)에 맞춰 직관적인 의미를 전달하는 아이콘(돋보기, 비행기, 장바구니 등)을 유연하게 선택하여 사용한다. 적절한 아이콘이 없을 경우 기본 도형(`@union`) 아이콘을 사용한다.

**Usage (레이아웃 및 반응형 규칙)**
* ✅ **레이아웃 구조:** 모바일(Compact) 해상도에서는 아이콘이 위에 있고 텍스트가 아래에 있는 `Vertical(세로형)` 배치만 사용한다. 웹(Wide) 해상도에서는 화면 구성과 여백에 따라 `Vertical(세로형)`과 `Horizontal(가로형)`을 모두 사용할 수 있다.

**모션 (Motion)**
* `Positive` 상태의 체크(Check) 아이콘은 화면이 처음 로드될 때 사용자의 시선을 끄는 부드러운 드로잉(Drawing) 애니메이션이 1회 동작한다.

**접근성 (Accessibility)**
* 시스템의 중요한 결과 피드백이므로, Result box 컨테이너에 `role="status"` 또는 `role="alert"`(에러 시)를 적용하여 스크린 리더 사용자가 화면 렌더링 즉시 결과 상태를 알 수 있도록 제공한다.

---

#### Loading

#### Loading

**정의**
사용자가 요청한 Task가 진행 중이며 데이터를 로드하고 있음을 시각적인 애니메이션으로 안내하여, 사용자의 체감 대기 시간을 줄여주는 상태 표시 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (Spinner/Dot), `skeleton` (UI 뼈대), `brand-logo` (브랜드 로고 기반) |
| Size (Basic) | `xs`, `sm`, `md`, `lg` |
| Block Level| `full-page` (전체 화면 차단), `partial` (부분 영역 차단) |

**Usage (타입별 사용 목적 및 규칙)**
* ✅ **Basic (기본 로딩):** 전체 화면 및 부분 화면 모두 사용 가능하다. 로딩 시간이 길어질 경우 시스템 오류로 오인하는 것을 방지하기 위해, 처음에는 **Spinner가 나타나 3회전 한 후 Dot 형태로 자연스럽게 변경**되는 모션을 적용한다.
* ✅ **Skeleton (스켈레톤):** 화면 레이아웃을 미리 보여주거나 이미지를 로드할 때 사용하여 체감 속도를 높인다.
  * `Wave`: 좁은 영역이나 여러 컴포넌트가 복합적으로 구성된 UI에 사용한다.
  * `Pulsate`: 넓은 영역이거나 동일한 UI가 반복되는 리스트 등에 사용한다.
* ✅ **Brand Logo (브랜드 로고):** Booking(예매) Flow와 같이 화면이 완전히 전환되는 **전체 차단(Full-page)** 상황에서만 제한적으로 사용한다. (부분 차단 영역에는 사용 불가). 로딩 중 상태 안내 문구를 하단에 표출하며, 단계가 이동할 때마다 문구를 변경하여 사용자의 이탈을 방지한다. 문구는 일정 시간 후 사라지므로 필수/중요 정보는 담지 않는다.

**Usage (차단 및 배치 규칙)**
* ✅ **부분 차단 우선:** 전체 화면 차단은 사용자의 탐색 흐름을 완전히 끊으므로 페이지 이동 등 꼭 필요한 상황에서만 사용하며, 가급적 데이터가 로드되는 해당 영역만 **부분 차단**하여 로딩을 표출하는 것을 권장한다. (예: 한 페이지 내에서의 검색/조회)
* ✅ **배치 (Alignment):** 전체 화면 로딩 시 화면 정중앙에 배치하며, 부분 영역(예: 버튼 하단 목록) 로딩 시 해당 컴포넌트 여백 기준 중앙에 배치한다.

**모션 (Motion)**
* **Skeleton:**
  * `Wave`: 1000ms (10 beat) / Linear
  * `Pulsate`: 700ms (7 beat) / Linear
* **Brand Logo:**
  * `Logo`: 2000ms (2 beat)마다 반복 재생
  * `Text (Enter)`: 400ms (4 beat) / Position Up / Linear
  * `Text (Delay)`: 3600ms (36 beat) 유지 후 사라짐

**접근성 (Accessibility)**
* 로딩이 진행 중인 컨테이너 또는 요소에 `aria-busy="true"`를 적용하여 스크린 리더가 해당 영역이 업데이트 중임을 인지하게 한다. 로딩이 완료되면 `false`로 변경하거나 속성을 제거한다.
* 시각적인 로딩 애니메이션 요소에는 `role="progressbar"`를 부여하고, 필요에 따라 진행률을 알 수 없는 경우 `aria-valuetext="로딩 중"`과 같은 대체 텍스트를 제공한다.

---

#### Ribbon Banner

#### Ribbon banner

**정의**
광고, 홍보, 제휴 프로모션 등 마케팅 목적의 정보를 이미지와 텍스트의 조합으로 눈에 띄게 전달하는 배너 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Size | `sm` (텍스트/이미지 좌우 배치), `lg` (텍스트/이미지 상하 배치) |
| Color (중요도) | `dark-blue` (High), `green`, `light-blue`, `gray` (Low) |
| Actions | `none`, `link`, `button` |

**토큰 매핑 및 색상 기준**
| Color | 특징 및 사용 기준 |
|-------|-----------------|
| Dark blue | 중요도가 가장 높은 최우선 프로모션에 사용 |
| Green / Light blue | 일반적인 프로모션 및 안내 |
| Gray | 중요도가 비교적 낮은 일반 안내 |
* ※ 삽입되는 이미지는 선택한 배너의 배경 색상 톤과 어울리도록 보정하여 일관성을 맞춘다.

**Usage (구성 및 텍스트 규칙)**
* ✅ **Title / Description:** Title은 필수로 작성하며(1줄 권장), Description(최대 2줄 권장)은 부가 설명이 필요할 때 선택적으로 사용한다. 강조가 필요한 키워드에는 Bold 처리를 할 수 있다.
* ✅ **긴 텍스트 처리:** 지정된 텍스트 영역 너비를 초과하면 글자가 잘리지 않고 단어 단위로 자동 개행(줄바꿈)된다. 글자 수에 따라 배너의 전체 높이가 유동적으로 가변한다.
* ✅ **인터랙션 및 버튼:** 배너 영역 전체가 클릭/탭 가능한 영역(Clickable Area)으로 동작한다. 필요한 경우 내부에 텍스트 링크(Link)나 버튼(Button) 요소를 시각적으로 포함할 수 있다.

**Usage (이미지 및 로고 규칙)**
* ✅ **이미지 적용:** 이미지는 반드시 배경이 투명한 이미지(PNG, SVG 등)를 사용한다. 핵심 피사체(물체/인물)가 지정된 안전 영역 내에 위치하도록 제작한다.
* ✅ **제휴사 로고:** 제휴(Partnership) 관련 배너일 경우, 제휴사의 로고를 우측 상단에 배치하며 메인 이미지와 시각적으로 겹치지 않도록 주의한다.

**Usage (해상도 및 레이아웃 규칙)**
* **Compact (모바일) - sm 사이즈:** 텍스트와 이미지가 **좌우**로 배치된다. 텍스트 개행으로 배너 높이가 늘어나도 이미지의 크기(너비/높이)는 1:1 비율로 고정되며 상하 여백만 늘어난다.
* **Compact (모바일) - lg 사이즈:** 텍스트와 이미지가 **상하**로 배치된다. 2:1 비율로 배너의 높이를 변경하며, 텍스트로 인해 높이가 늘어날 경우 이미지의 최대 너비(284px)를 유지한 채 이미지 상단 영역이 함께 늘어난다.
* **Wide (웹):** 2:1 비율을 기본으로 사용한다. 단, 배너의 최대 너비(368px)를 넘어갈 경우 상단의 텍스트 영역 높이만 늘어나고 이미지는 하단에 고정되는 레이아웃을 취한다.

**접근성 (Accessibility)**
* 배너 전체가 링크로 동작하므로 `<a>` 또는 `<button>` 태그를 사용한다.
* 배경에 삽입되는 프로모션 이미지에는 시각적 의미를 담고 있는 경우 `alt` 속성을 통해 이미지의 목적이나 내용을 스크린 리더에 제공한다.

---

#### Page Feedback

**정의**
페이지 하단에서 사용자가 콘텐츠에 대한 만족도를 빠르게 평가하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `thumbs`, `rating`, `emoji` |
| State | `default`, `submitted` |

---

### 3.5 텍스트 & 아이콘 (Text & Icon)

---

#### Heading

#### Heading

**정의**
페이지 내 특정 콘텐츠 블록이나 섹션의 주제(제목)를 명확히 전달하여 정보의 논리적 위계를 구조화하는 텍스트 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Level | `H1`, `H2`, `H3`, `H4`, `H5`, `H6` |
| Alignment | `Left` (기본) |
| Add-on | `Subtitle` (H1 전용), `Link` |

**Usage (위계 및 계층 규칙)**
* ✅ **H1 필수 사용:** 모든 페이지는 해당 페이지의 대주제를 나타내는 가장 상위 제목으로 `Heading level 1 (H1)`을 반드시 포함해야 한다.
* ✅ **순차적 레벨 적용:** 상위 제목(H1)부터 하위 제목(H6)까지 콘텐츠의 정보 위계에 맞게 단계를 건너뛰지 않고 순차적으로 사용한다.
* ✅ **특수 컨테이너 내 위계:**
  * `Dialog` 및 `Bottom sheet`: 전체 페이지 위에 뜨는 하위 요소이므로, 내부 제목은 `H2`부터 사용한다.
  * `Tab`: Tab 버튼 자체가 1차 제목 역할을 하므로, Tab 패널 내부에 들어가는 제목은 현재 맥락보다 한 단계 낮은 Level을 적용한다.

**Usage (텍스트 및 스타일 규칙)**
* ✅ **중복 방지:** 한 페이지 내에서 완전히 동일한 문구의 Heading을 중복해서 사용하지 않도록 유의한다.
* ✅ **정렬:** 모든 Heading은 **좌측 정렬(Left)**을 기본으로 적용한다.
* ✅ **Subtitle (부제목):** Subtitle 컴포넌트는 오직 가장 상위 제목인 `H1`의 상단에만 추가하여 제한적으로 사용할 수 있다.
* ✅ **Link 적용 주의:** Heading에 링크를 포함해야 할 경우, 텍스트의 일부분이 아닌 **Heading 문구 전체**에 링크(Link) 속성을 적용해야 한다.

**접근성 (Accessibility)**
* **WCAG 1.3.1 / 2.4.6 준수:** 시각적인 글자 크기만 키우는 것이 아니라, 실제 마크업 상으로도 `<h1>`~`<h6>` 태그를 올바르게 사용하여 스크린 리더(Screen Reader)가 페이지의 정보 구조와 관계를 파악하고 탐색할 수 있도록 지원해야 한다.
* 스크린 리더 사용자는 단축키를 통해 Heading 단위로 페이지를 점프하며 탐색하므로, 제목 내용이 해당 섹션의 목적을 명확히 설명할 수 있도록 작성한다.
---

#### Paragraph

#### Paragraph

**정의**
서비스 내의 본문 문장 및 문단을 구성하거나, 보조적인 설명 문구(Disclaimer)를 제공할 때 사용하는 가장 기본적인 텍스트 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (일반 본문 문단), `disclaimer` (보조/주의 설명 문구) |
| Alignment | `left` (기본), `center` |
| Size | `sm` (14px, Disclaimer), `lg` (16px, Basic/Disclaimer) |

**Usage (구성 및 정렬 규칙)**
* ✅ **List와의 구분:** 여러 문장이 동등한 레벨로 열거될 때는 불릿(Bullet) 기호가 있는 `List` 컴포넌트를 사용하고, 서술형으로 이어지는 일반적인 문장이나 단일 문장일 때는 `Paragraph`를 사용한다. 단, 그룹핑된 영역 내에서 시각적 통일성을 위해 `List` 대신 `Paragraph`를 연속해서 배치할 수도 있다.
* ✅ **정렬:** 긴 텍스트의 가독성을 위해 **좌측 정렬(Left)**을 기본으로 한다. 단, 텍스트가 3줄 이하로 매우 짧은 문장/문단인 경우에 한해 선택적으로 **중앙 정렬(Center)**을 사용할 수 있다.

**Usage (텍스트 서식 및 강조 규칙)**
* ✅ **사이즈 통일:** 하나의 Paragraph(문단) 내에서는 텍스트 크기(Size)를 섞어서 사용하지 않고 동일하게 유지해야 한다.
* ✅ **문구 강조:** 문단 내에서 특정 단어나 문장을 강조해야 할 경우 다음 방법을 사용한다.
  * **Bold / Color:** 강조할 텍스트에 Bold(굵게) 처리를 하거나, 맥락에 맞게 Semantic Color(`Positive` 또는 `Negative`)를 부분적으로 적용한다.
  * **Text box 전환:** 문장 전체를 강하게 강조해야 하는 경우, Paragraph 대신 컨테이너로 감싸진 `Text box` 컴포넌트로 대체하여 사용한다.
* ✅ **Link 포함:** 문장 내에 다른 페이지로 이동하는 텍스트 링크(Link)를 자연스럽게 포함하여 사용할 수 있다.
* ✅ **Disclaimer 크기:** 보조 설명 문구인 Disclaimer는 화면 중요도에 따라 `sm(14px)` 또는 `lg(16px)` 사이즈를 선택하여 적용한다.

**접근성 (Accessibility)**
* 일반적인 본문 텍스트이므로 HTML `<p>` 태그를 사용하여 문단의 시맨틱 의미를 부여한다.
* 강조를 위해 사용된 색상(`Positive`, `Negative`) 외에도 Bold(`<strong>` 또는 `<b>`)를 함께 적용하여, 색맹/색약 사용자나 스크린 리더 사용자도 강조의 의미를 동일하게 파악할 수 있도록 한다.
---

#### Link

#### Link

**정의**
사용자를 현재 서비스 내의 다른 페이지나 외부 웹사이트로 단순 이동시킬 때 사용하는 텍스트 기반의 네비게이션 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Style | `underline` (기본), `leading-icon` (좌측 아이콘), `trailing-icon` (우측 아이콘), `arrow` (화살표 형태) |
| State | `enabled` (default), `focused & hovered` |

**Button vs Link 구분 기준**
| 구분 | Button (버튼) | Link (링크) |
|------|-------------|------------|
| **목적/동작** | 폼 제출, 모달 열기, 상태 변경 등 특정 이벤트 실행 | 내부 또는 외부 페이지로 단순 이동 (URL 변경) |
| **계층 구조** | Primary, Secondary 등 시각적 위계가 존재 | 일반적으로 시각적 위계(계층) 없음 |
| **상태** | Disabled(비활성화) 상태 존재 | **Disabled 상태 없음 (항상 활성화)** |
| **키보드 제어** | `Enter` 키 또는 `Space bar`로 실행 | **`Enter` 키로만 실행** |
| **스크린 리더** | "버튼"으로 낭독됨 | "링크"로 낭독됨 |

**Usage (텍스트 및 시각 규칙)**
* ✅ **명확한 링크명:** 사용자가 링크를 클릭하기 전에 목적지를 직관적으로 예측할 수 있어야 한다. ("여기" 또는 "클릭"과 같은 모호한 텍스트 사용 금지)
* ✅ **상태 제한 (No Disabled):** 링크는 동작 불가능한 비활성화(Disabled) 상태를 가지지 않으며, 항상 클릭 가능한 상태로 제공된다.
* ✅ **접근성 대비:** 텍스트 링크는 주변 배경과 최소 **4.5:1 이상의 명도 대비**를 준수하여 시각적으로 명확히 인지되어야 한다.

**Usage (배치 및 정렬 규칙)**
* ✅ 주변 컴포넌트의 성격에 따라 정렬 기준을 다르게 적용한다.
  * **List와 조합 시:** 좌측 정렬 배치
  * **Data table과 조합 시:** 우측 정렬 배치

**접근성 (Accessibility)**
* 시맨틱 HTML인 `<a>` 태그를 사용하고 반드시 `href` 속성을 포함하여 스크린 리더가 요소의 역할을 "링크"로 명확하게 낭독하도록 한다.
* 링크가 새 창(New window/tab)으로 열리는 경우, `aria-label`이나 `title` 속성, 또는 숨김 텍스트를 통해 "새 창으로 열림"을 스크린 리더 사용자에게 사전 안내해야 한다.

---

#### Divider

#### Divider

**정의**
텍스트나 콘텐츠 블록 사이의 시각적 계층 구조를 명확히 하고, 연관된 정보를 논리적으로 분리/그룹화할 때 사용하는 라인(선) 형태의 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Orientation| `horizontal` (가로), `vertical` (세로) |
| Layout Type| `full` (좌우/상하 여백 없음), `inset` (박스 레이아웃 내 양끝 여백 존재) |
| Line Style | `line` (실선), `dash` (점선 - Primary 전용) |
| Color Style| `primary` (기본), `highlight` (강조), `top` (최상위 컨테이너 구분용) |

**토큰 매핑**
| Style | Border Color | 특징 |
|-------|-------------|------|
| Primary | `color/border/divider-primary` | 가장 일반적인 콘텐츠 및 섹션 구분에 사용 |
| Highlight | `color/border/divider-highlight` | Divider보다 콘텐츠 데이터(텍스트)가 더 강조되어야 할 때 시각적으로 힘을 뺀 보조 역할로 사용 |
| Top | `color/border/divider-top` | Accordion, Expander 등 굵은 구분이 필요한 최상위 컴포넌트 제목 영역(Heading) 하단에 사용 |

**Usage (유형 및 목적 규칙)**
* ✅ **보조 역할:** Divider는 화면의 주 콘텐츠보다 눈에 띄게 강조되어서는 안 되며, 콘텐츠의 가독성을 높이기 위한 시각적 보조 수단으로만 사용한다.
* ✅ **여백 설정 (Full vs Inset):** 카드(Card)나 박스 레이아웃 내부 등 패딩(Padding)이 존재하는 컨테이너 안에서는 여백이 있는 `Inset`을 사용하고, 화면 전체 너비를 가로지르는 경우에는 여백이 없는 `Full`을 사용한다.
* ✅ **위치:** Divider는 두 섹션 **사이(Between)**에 위치하여 서로를 구분하는 용도이므로, 리스트나 섹션의 가장 마지막 끝부분에는 사용하지 않는다.

**접근성 (Accessibility)**
* 단순한 시각적 구분을 위한 장식용 요소이므로 `<hr>` 태그를 사용하거나 CSS `border` 속성으로 구현한다.
* 스크린 리더가 불필요하게 선을 읽어 사용자 흐름을 방해하지 않도록 `<hr aria-hidden="true">` 처리를 권장한다. (의미적으로 중요한 섹션 구분 시에만 `role="separator"`를 제한적으로 사용한다.)
---

#### Icon

**정의**
의미와 액션을 시각적으로 전달하는 SVG 아이콘 컴포넌트.

**Size 스펙**
| Size | px | 용도 |
|------|----|------|
| XL | 32px | 빈 상태 일러스트 |
| LG | 24px | Navigation, Top Bar |
| MD | 20px | 인라인, 버튼 내 |
| SM | 16px | 캡션, Badge 내 |

**토큰 매핑**
| 역할 | 토큰 | 값 |
|------|------|-----|
| 기본 | `color/icon/primary` | `#051766` |
| 보조 | `color/icon/secondary` | `#5E5E5E` |
| 반전 | `color/icon/inverse` | `#FFFFFF` |
| 비활성 | `color/icon/disabled` | `#A4A4A4` |
| 성공 | `color/icon/positive` | `#28794E` |
| 경고 | `color/icon/warning` | `#BD5814` |
| 오류 | `color/icon/negative` | `#DA291C` |

**접근성**
- 장식적: `aria-hidden="true"`
- 의미 있는 아이콘: `aria-label` 또는 `<title>` 제공

---

#### Icon-text

#### Icon text

**정의**
서비스의 핵심 특징, 혜택, 부가 서비스 등의 콘텐츠 정보를 시각적 아이콘과 짧은 레이블(텍스트)의 조합으로 직관적이고 간결하게 전달하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Size | `sm`, `md`, `lg` |
| Orientation | `horizontal` (아이콘 좌측, 텍스트 우측), `vertical` (아이콘 상단, 텍스트 하단) |
| Feature | `tooltip` (부가 설명 필요 시), `container-border` (테두리 여부) |

**Usage (구성 및 텍스트 규칙)**
* ✅ **레이블 간결성:** 레이블은 직관적이고 간결한 단어(명사형)로 작성하며, 긴 문장이나 서브 텍스트를 포함하지 않는다. 부연 설명이 필요한 경우에 한해 우측에 `Tooltip`을 선택적으로 배치하여 사용한다.
* ✅ **긴 텍스트 개행:** 다국어 등으로 인해 레이블이 길어지는 경우, 레이블 영역 내에서 하단으로 개행되며 전체 높이가 늘어난다.
* ✅ **높이 통일 (그룹핑):** 여러 개의 Icon text가 동일한 행(Row)에 그룹으로 배치될 때, 각 요소의 높이는 가장 높은 컴포넌트(최대 높이)를 기준으로 통일하여 시각적 안정감을 준다.

**Usage (방향 및 반응형 배치 규칙)**
* **정렬 (Alignment):**
  * `Horizontal` (가로형): 아이콘과 레이블을 좌우로 배치하며 **좌측 정렬**을 사용한다.
  * `Vertical` (세로형): 아이콘과 레이블을 상하로 배치하며 **중앙 정렬**을 사용한다.
* **Compact (모바일) 배치:**
  * 화면이 좁으므로 가급적 `Horizontal` (가로형)을 사용한다.
  * 1열 또는 최대 2열(Grid)로 나란히 배치하며, 그 이상의 개수는 하단 행으로 개행하여 배치한다.
* **Wide (웹) 배치:**
  * `Horizontal`: 1행에 최대 3개까지 좌측 정렬로 배치하며, 초과 시 하단 행으로 배치한다.
  * `Vertical`: 1행에 최대 5개까지 중앙 정렬로 배치하며, 초과 시 하단 행으로 배치한다.

**접근성 (Accessibility)**
* 아이콘이 단순한 장식이 아니라 정보를 전달하는 역할을 하므로, 시각 장애 사용자를 위해 아이콘에 대한 대체 텍스트(예: `aria-label` 또는 `sr-only` 텍스트)를 제공하거나 레이블이 그 의미를 충분히 포함하도록 구성한다.
* `Tooltip`을 병행 사용하는 경우, 키보드 초점(Focus) 이동 시에도 툴팁 내용에 접근할 수 있도록 마크업 구조를 올바르게 연결한다.
---

#### Icon-text Information

#### Icon text information

**정의**
서비스의 핵심 정보나 안내 사항을 아이콘, 레이블(Title), 추가 설명(Description) 문구가 결합된 박스(Container) 형태로 제공하는 복합 디스플레이 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Container Color | `white`, `grey` |
| Orientation | `vertical` (Compact/Wide 공통), `horizontal` (Wide 전용) |
| Add-on Elements | `badge`, `tooltip`, `divider` |

**토큰 매핑**
| 영역 | 토큰 |
|------|------|
| Background (White) | `color/fill/surface/primary` |
| Background (Grey) | `color/fill/surface/secondary` |
| Title | `color/text/title` |

**Usage (구성 및 높이 규칙)**
* ✅ **필수 요소:** 아이콘과 레이블(Title)은 정보 전달의 핵심이므로 생략할 수 없으며 반드시 포함해야 한다.
* ✅ **Description (추가 설명):** 보조 문구는 선택적으로 사용할 수 있다. 단, 여러 개의 컴포넌트가 하나의 그룹으로 나란히 쓰일 경우, 시각적 일관성을 위해 Description 적용 여부를 모두 동일하게 통일해야 한다. (내부에 `Paragraph`나 `List` 활용 가능)
* ✅ **최대 높이 통일:** 여러 개의 컨테이너가 같은 행에 배치될 경우, 컨테이너의 높이는 가장 내용이 많은(가장 높은) 컨테이너의 최대 높이에 맞춰 일괄 통일한다.

**Usage (추가 옵션 및 조합 규칙)**
* ✅ **부가 요소 조합:**
  * `Badge`: 콘텐츠의 상태 정보를 제공할 때 사용한다.
  * `Tooltip`: 타이틀(Title)에 부가 설명이 필요한 경우 레이블 우측에 사용한다. **(주의: Description 문구 안에는 Tooltip을 사용할 수 없다.)**
  * `Divider`: 컨테이너 내부의 콘텐츠를 상하로 구분할 때 가로형으로 사용한다.

**Usage (반응형 및 레이아웃 규칙)**
* ✅ **Compact (모바일):** * `Vertical (세로형)` 레이아웃만 사용 가능하다.
  * 화면 너비에 꽉 차는 Full size로 1열 배치하며, 2개 이상일 경우 하단 행으로 개행하여 배치한다.
* ✅ **Wide (웹):** * 텍스트 글자 수와 화면 구성에 따라 `Vertical` 또는 `Horizontal` 레이아웃을 선택할 수 있다.
  * `Horizontal (가로형)`: 1행에 최대 3개까지 나란히 배치한다.
  * `Vertical (세로형)`: 1행에 최대 1개씩(Full size) 세로로 배치한다.

**접근성 (Accessibility)**
* 아이콘과 텍스트가 하나의 정보 덩어리로 인식되도록 컨테이너 내부 구조를 논리적으로 마크업한다.
* `Tooltip`을 Title에 사용할 경우, 키보드 초점(Focus) 이동 시 올바른 순서로 툴팁 내용에 접근할 수 있도록 DOM 순서를 고려한다.

---

#### Legend

#### Legend

**정의**
화면 내에 사용된 다양한 그래픽 요소(아이콘, 색상, 기호 등)의 의미를 텍스트 레이블과 함께 나열하여, 사용자가 인터페이스를 올바르게 이해할 수 있도록 돕는 범례 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Orientation | `horizontal` (가로형), `vertical` (세로형) |
| Size | `sm`, `lg` |
| Columns (Vertical) | `1-column` (1열), `2-column` (2열) |
| Add-on | `divider` (구분선 포함 여부) |

**Usage (레이아웃 및 정렬 규칙)**
* ✅ **방향 선택:** 화면 여백과 범례 항목의 개수를 고려하여 가로형(`Horizontal`)과 세로형(`Vertical`) 중 알맞은 형태를 선택하여 사용한다.
* ✅ **세로형(Vertical) 단 구성:** 레이블의 길이와 항목의 개수에 따라 1열(1단) 또는 2열(2단)로 배치하여 공간을 효율적으로 활용할 수 있다.
* ✅ **아이콘-텍스트 정렬 (Alignment):** 기본적으로 아이콘과 텍스트는 수평 **중앙 정렬(Center)**을 적용한다. 단, 공간 제약으로 인해 레이블 텍스트가 하단으로 개행될 경우, 시각적 균형을 맞추기 위해 아이콘과 텍스트를 **상단 정렬(Top)**로 변경하여 적용한다.

**Usage (텍스트 및 구성 규칙)**
* ✅ **간결한 텍스트:** 레이블은 단어 수준의 매우 짧고 명확한 문구로 작성한다. 만약 텍스트가 허용 너비를 초과할 경우 영역 내에서 자동 개행된다.
* ✅ **구분선(Divider) 활용:** 범례 항목이 많아 복합적으로 나열되는 경우, 세로형(`Vertical`) 레이아웃 내에서 `Divider` 컴포넌트를 함께 사용하여 항목 간의 정보 그룹을 시각적으로 명확히 분리할 수 있다.

**접근성 (Accessibility)**
* 시각적인 그래픽 요소의 의미를 풀어서 설명하는 컴포넌트이므로, 스크린 리더 사용자가 해당 영역이 범례임을 알 수 있도록 전체 컨테이너에 `role="group"` 또는 `role="region"`을 부여하고 `aria-label="아이콘 범례"` 등의 설명을 제공한다.
* 아이콘 자체는 장식용(`aria-hidden="true"`)으로 처리하고 텍스트 레이블을 통해 의미가 전달되도록 구성한다.

---

### 3.6 카드 & 컨테이너 (Card & Container)

공통 토큰:
- Card Radius: `radius/card` (16px)
- Card Background: `color/fill/surface/primary`
- Card Border: `color/border/tertiary`

---

#### Bottom Card

#### Bottom card

**정의**
화면 내 콘텐츠의 상세 정보를 `Bottom sheet`로 연결해 보여주기 위한 진입점 역할을 하는 버튼 형태의 카드 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic`, `icon` |
| Background Color | `white`, `grey` |
| Button Option | `true` (포함), `false` (생략) |
| State | `enabled`, `hovered`, `focused`, `pressed` |

**Usage (텍스트 및 구성 규칙)**
* ✅ **텍스트 중복 금지:** 카드 내의 `Title`, `Description`, `Button` 텍스트는 서로 중복된 내용을 사용하지 않고 명확히 구분하여 작성한다.
* ✅ **버튼명 일치:** 하단 `Button`의 텍스트는 버튼을 눌렀을 때 표출되는 `Bottom sheet`의 Heading(제목)과 동일하게 작성하는 것을 권장한다.
* ✅ **긴 텍스트 표출:** `Title`과 `Description`은 각각 최대 2줄까지 간결하게 작성한다. 텍스트가 길어지면 카드의 높이가 가변적으로 늘어난다.
* ✅ **버튼 생략:** 하단 버튼은 선택적으로 생략할 수 있으나, 동일한 그룹 내의 카드들은 생략 여부를 일관되게 통일해야 한다.
  * **Basic 타입:** 버튼을 생략해도 카드의 최소 높이가 줄어들지 않으며, 내부 텍스트가 높이 기준 수직 가운데 정렬된다.
  * **Icon 타입:** 버튼을 생략하면 버튼의 높이만큼 카드의 전체 높이가 줄어든다.

**Usage (레이아웃 및 반응형 규칙)**
* ✅ **높이 통일 (그룹핑):** 여러 개의 Bottom card가 같은 행(Row)에 배치될 경우, 텍스트가 가장 긴(가장 높은) 카드를 기준으로 **모든 카드의 높이를 일괄 통일**한다.
* ✅ **색상 통일:** White 배경 위에서 White 또는 Grey 카드를 선택하여 사용할 수 있으나, 같은 그룹 내에서는 반드시 하나의 색상으로 통일해서 혼용하지 않는다.
* ✅ **Compact (모바일) 배치:** 세로(수직) 방향으로 나열하며, 개수 제한 없이 배치할 수 있다.
* ✅ **Wide (웹) 배치:** 가로(수평) 1행에 최대 3개까지 배치할 수 있다.
  * 1개 배치 시: 전체 화면 너비의 1/2 크기로 적용한다.
  * 2~3개 배치 시: 전체 화면 너비(Full)를 균등하게 분할하여 꽉 차게 배치한다.

**접근성 (Accessibility)**
* 카드 전체가 하나의 액션을 수행하는 버튼 역할을 하므로, 시맨틱 HTML인 `<button>` 태그를 사용하거나 `role="button"`을 부여하여 스크린 리더 사용자가 해당 요소의 역할을 명확히 인지할 수 있도록 한다.

---

#### Content Visual Card

#### Content visual card

**정의**
가장 중요한 핵심 콘텐츠나 프로모션을 시각적인 이미지와 텍스트로 조합하여 사용자에게 강렬하게 강조할 때 사용하는 카드 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Layout | `compact` (상하 배치), `wide` (좌우 배치) |
| Elements | `image`, `title`, `description`, `button` (선택), `3D motif` (선택) |
| Display | `single` (단일 표출), `carousel` (다중 표출 시 스와이프 및 인디케이터 제공) |

**Usage (텍스트 및 버튼 규칙)**
* ✅ **텍스트 분량 제한:** 시각적 정보 전달이 주가 되므로 텍스트는 최대한 간결하게 유지한다. **Title은 최대 2줄, Description은 최대 3줄** 작성을 권장한다. (최대 글자 수를 초과할 경우 카드의 전체 높이가 유동적으로 늘어난다.)
* ✅ **Button (CTA):** 사용자의 명확한 다음 액션이 필요한 경우 카드 내부에 버튼을 선택적으로 추가하여 사용할 수 있다.

**Usage (이미지 및 3D Motif 규칙)**
* ✅ **단일 이미지 대응 (3:2 비율):** 이미지의 기본 가로세로 비율은 3:2를 유지하며, 모든 해상도(기기)에 대응할 수 있도록 1개의 이미지만 제작한다. 단, 반응형에 따라 이미지가 잘릴 수 있으므로 **핵심 피사체는 반드시 중앙의 안전 영역 내에 위치**해야 한다.
* ✅ **3D Motif 활용:** 브랜드 아이덴티티 강조를 위해 카드 이미지 좌측에 3D Motif를 크롭하여 배치할 수 있다. (크롭 너비: Compact 24px / Wide 32px)
  * **[금지 규정]** 투명도 적용 불가(항상 100%), Red accent 영역 숨김 불가, 다른 색상 오버레이 금지, 세로 회전 금지, 비율 왜곡 금지.

**Usage (해상도 및 다국어 반응형 규칙)**
* **다국어 높이 가변 (Wide):**
  * 글자 수가 상대적으로 적은 언어(한국어, 중국어, 일본어): 카드 높이 **340px** 유지 (이미지 상하 크롭).
  * 글자 수가 많아지는 언어(영어 등): 텍스트 공간 확보를 위해 카드 높이 **384px** 적용.
* **Compact (모바일):** 텍스트와 이미지가 상하로 배치되며, 3:2 비율을 그대로 유지한 채 화면 너비에 맞춰 축소/확대된다.
* **Wide (웹):** 텍스트(좌)와 이미지(우)가 좌우로 배치된다. 화면이 줄어들면 높이는 고정된 상태에서 이미지의 좌우가 크롭된다. (이미지 최대 너비 480px 도달 시, 이후부터는 이미지는 고정되고 전체 카드 너비만 늘어남).

**Usage (다중 배치 규칙)**
* ✅ **Carousel (캐러셀):** 1개의 화면 내에서 Content visual card를 2개 이상 배치해야 할 경우, 화면을 과도하게 차지하지 않도록 카드의 너비를 줄이고 하단에 인디케이터(Indicator)를 포함한 Carousel 형태로 제공한다.

**접근성 (Accessibility)**
* 카드 내의 배경 이미지가 시각적인 정보를 포함하고 있으므로, 스크린 리더 사용자를 위해 의미를 담은 명확한 `alt` 텍스트를 제공한다.
* Carousel로 2개 이상의 카드가 제공될 경우, 스크린 리더 사용자와 키보드 사용자가 각 카드로 포커스를 이동하고 내용을 확인할 수 있도록 스와이프 기능 외에 포커스 가능한 컨트롤(이전/다음 버튼 또는 인디케이터)을 제공해야 한다.

---

#### Image Card

#### Image card

**정의**
시각적으로 강조된 비주얼 이미지와 간결한 텍스트(Title, Description)를 조합하여 연관 페이지로의 이동(Link, Dialog 등)을 유도하는 카드 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (카드 전체 클릭), `button` (우측 하단 CTA 버튼 포함) |
| Orientation | `vertical` (상하 배치 - 최소 2개 이상 사용 시), `horizontal` (좌우 배치 - 단독 사용 시) |
| State | `enabled` (default), `hovered`, `focused`, `pressed` |
| Add-on | `badge` (Extra 타입만 허용) |

**Usage (구성 및 텍스트 규칙)**
* ✅ **필수 요소:** `Title`과 `Description`은 모두 필수로 작성해야 하며, 카드 하나당 최대 2줄까지만 작성할 것을 권장한다. (글자 수가 길어지면 카드의 높이가 가변적으로 늘어남).
* ✅ **Badge 활용:** 정보 식별을 돕기 위해 카드 내에 Badge를 추가할 수 있으나, 반드시 `Extra` 타입만 사용해야 한다. (`Basic`, `Using state` 타입 사용 불가)
* ✅ **텍스트 최소 높이 보장:** 텍스트 영역은 Title 1줄, Description 2줄이 들어갔을 때를 상정하여 최소 높이(Compact 132px, Wide 146px)를 보장해야 한다.

**Usage (버튼 및 다중 배치 규칙)**
* ✅ **Button 제한:** 화면 내에 카드가 1~2개 배치될 때는 우측 하단에 강조된 CTA 버튼을 사용할 수 있다. 그러나 카드가 **3개 이상 배치될 경우에는 복잡도를 줄이기 위해 CTA 버튼 대신 Link 스타일로 적용**해야 한다.
* ✅ **최대 높이 통일:** 한 행(Row)에 2개 이상의 카드가 나란히 표출될 때, 삽입된 텍스트의 양이 달라 높이가 다르더라도 가장 높은 카드를 기준으로 모든 카드의 **최대 높이를 통일**한다.

**Usage (이미지 및 반응형 규칙)**
* ✅ **이미지 비율:** * `Vertical` (세로형): Compact/Wide 관계없이 3:2 비율을 사용한다.
  * `Horizontal` (가로형): 텍스트 길이에 따라 높이가 다르므로 비율을 유연하게 적용한다. (한국어/중국어/일본어 등 짧은 텍스트는 4.3:5.7, 그 외 긴 다국어는 4.8:5.2 적용).
* ✅ **Compact (모바일) 반응형:** 여러 개의 카드가 나열될 때는 상하 1열로 배치하거나 `Carousel` 스와이프를 사용하여 화면 공간을 절약한다.
* ✅ **Wide (웹) 반응형:** * `Vertical` (세로형)은 1행에 최대 3개까지 배치할 수 있으며, 4개 이상부터는 `Carousel`을 적용한다.
  * `Horizontal` (가로형)은 1행에 1개씩만 단독 배치하며, 2개 이상일 경우 `Carousel`을 적용한다.

**접근성 (Accessibility)**
* 카드 전체가 클릭 가능한 요소(`Basic`)이거나 내부에 별도의 액션 요소(`Button`)가 포함되어 있으므로, 스크린 리더 사용자가 포커스 진입 시 카드의 목적과 이동 경로를 명확히 인지할 수 있도록 구조화된 마크업과 `aria-label`을 제공해야 한다.
---

#### Logo Card

#### Logo card

**정의**
브랜드 로고(또는 제휴사 로고)와 텍스트 레이블로 구성되어, 특정 브랜드나 제휴 서비스로의 이동을 유도하는 카드 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Size (Compact) | `sm` (1행 2개 배치), `lg` (1행 1개 배치) |
| Size (Wide) | `sm` (1행 4개 배치), `md` (1행 3개 배치), `lg` (1행 1개 단독/강조 배치) |
| Description | `true` (포함), `false` (생략) |
| State | `enabled` (default), `hovered`, `focused`, `pressed` |

**Usage (구성 및 텍스트 규칙)**
* ✅ **로고 영역 제한:** 브랜드 로고가 들어가는 이미지 영역은 전체 카드 높이의 **50%를 초과하지 않도록** 제한한다. (해상도 손실 방지를 위해 로고 이미지는 `SVG` 파일 사용을 권장한다.)
* ✅ **텍스트 분량 (Title):** Title은 최대 2줄까지 작성할 수 있다. 텍스트가 길어져 개행되면 카드의 전체 높이도 함께 늘어나므로 최대한 간결한 작성을 권장한다.
* ✅ **텍스트 높이 고정:** UI의 일관성을 위해 Title 텍스트가 1줄만 입력되더라도, 카드의 최소 높이는 **2줄이 입력되었을 때의 높이를 그대로 유지**한다.
* ✅ **Description 생략:** Description(보조 설명)은 선택적으로 생략할 수 있다. 단, 같은 행에 배치되는 카드 그룹 내에서는 생략 여부를 일관되게 통일해야 한다.

**Usage (레이아웃 및 반응형 규칙)**
* ✅ **최대 높이 통일:** 여러 개의 Logo card가 같은 행(Row)에 배치될 때, 각 카드의 텍스트 길이에 차이가 있어 높이가 달라지더라도 **가장 높은 카드를 기준으로 모든 카드의 높이를 통일**한다.
* ✅ **Compact (모바일) 배치:**
  * `sm` 사이즈: 화면 너비에 맞춰 1행에 2개씩 나란히 배치한다.
  * `lg` 사이즈: 화면 너비에 꽉 차게(Full) 1행에 1개씩 상하로 배치한다.
* ✅ **Wide (웹) 배치:**
  * `sm` 사이즈: 1행에 최대 4개까지 배치한다.
  * `md` 사이즈: 1행에 최대 3개까지 배치한다.
  * `lg` 사이즈: 화면 상단이나 특정 영역에서 단독으로 강조할 때 1행에 1개를 화면 너비에 맞게 배치한다.

**접근성 (Accessibility)**
* 카드 전체가 클릭 가능한 버튼이나 링크 역할을 하므로, `<a>` 또는 `<button>` 태그를 사용해 의미에 맞게 마크업한다.
* 로고 이미지 자체는 시각적 의미를 지니고 있으므로, 이미지에 `alt="{브랜드명} 로고"` 형태의 대체 텍스트를 제공하여 스크린 리더 사용자가 목적지를 명확히 인지할 수 있도록 한다.

---

#### Related Card

#### Related card

**정의**
사용자가 현재 보고 있는 화면과 연관된 주제나 페이지로 쉽게 이동할 수 있도록, 화면 하단에 제목과 설명 문구를 묶어 제공하는 링크(Link) 역할의 카드 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Layout | `compact` (상하 배치), `wide` (좌우 배치) |
| State | `enabled` (default), `hovered`, `focused`, `pressed` |

**토큰 매핑**
| 영역 | 토큰 / 스타일 |
|------|--------------|
| Background | `color/fill/surface/secondary` (Gray 계열 지정 색상) |
| Title | `color/text/title` |
| Subtitle | `color/text/body-secondary` |

**Usage (구성 및 텍스트 규칙)**
* ✅ **레이블 작성:** `Title`은 이동할 목적지 페이지의 실제 제목과 동일하게 작성하며, `Subtitle`은 해당 페이지의 핵심 내용을 축약한 한두 문장으로 작성한다.
* ✅ **긴 텍스트 표출:** 글자 수에 엄격한 제한은 없으나, 카드의 높이가 과도하게 길어지는 것을 방지하기 위해 최대한 간결하게 작성한다. (개행 시 카드의 높이가 가변적으로 늘어남)
* ✅ **배경색 지정:** 메인 콘텐츠 영역과 시각적으로 명확히 분리하기 위해 컨테이너 배경은 반드시 **Gray 색상**을 사용하며, White 배경은 사용하지 않는다.

**Usage (레이아웃 및 반응형 규칙)**
* ✅ **사용 개수:** 화면 해상도(Compact/Wide)와 관계없이 최소 1개에서 **최대 3개까지**만 사용한다.
* ✅ **최대 높이 및 텍스트 정렬:** 한 행에 2개 이상의 카드가 나란히 배치될 경우, 가장 내용이 많은 카드를 기준으로 **최대 높이를 통일**한다. 이때 내부의 텍스트 요소들은 컨테이너의 **상단(Top)을 기준으로 정렬**된다.
* ✅ **Compact (모바일) 배치:** 화면 너비에 꽉 차는 Full size로 1행에 1개씩 세로로 배치한다.
* ✅ **Wide (웹) 배치:**
  * 1행에 최대 3개까지 나란히 가로로 배치하며, 전체 카드의 합친 너비는 상단 콘텐츠 너비와 동일하게 맞춘다.
  * 카드가 1~2개인 경우, 좌측부터 순서대로 꽉 차게 배치하고 남은 우측 공간은 빈 여백으로 둔다.

**접근성 (Accessibility)**
* 카드 전체가 목적지 페이지로 이동하는 링크 역할을 수행하므로, 시맨틱 HTML인 `<a>` 태그를 사용하여 스크린 리더 사용자가 "링크"임을 명확히 인지할 수 있도록 마크업한다.
* `aria-labelledby`를 통해 카드의 `Title`을 링크의 접근성 이름(Accessible Name)으로 연결하여, 목적지를 명확히 안내한다.

---

#### Data Box

#### Data box

**정의**
레이블(Label)과 데이터(Data) 값을 쌍으로 구성하여, 사용자가 확인해야 할 핵심 데이터를 시각적으로 묶어 강조할 때 사용하는 박스형 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (일반 데이터 표출), `sum` (총합 및 세부 내역 확장/축소) |
| Orientation | `horizontal` (좌우 배치), `vertical` (상하 배치) |
| State (Sum) | `expanded` (확장됨), `collapsed` (축소됨) |
| Background | `gray` (`color/fill/surface/secondary` 등 지정된 배경색 사용) |

**Usage (텍스트 및 배치 규칙)**
* ✅ **레이블/데이터 길이 가변:** 레이블이나 데이터 값이 길어질 경우, 가독성을 위해 좌우(`horizontal`) 배치 대신 상하(`vertical`) 배치로 전환하여 사용한다.
* ❌ **단위 분리 개행 금지:** 데이터의 숫자 값과 단위(예: 원, 명, %, 등)가 서로 분리되어 개행(줄바꿈)되지 않도록 주의한다. 반드시 데이터와 단위는 한 줄에 함께 표출되어야 한다.

**Usage (강조 및 구분선 규칙)**
* ✅ **데이터 강조:** 데이터 값을 강조하기 위해 Bold(굵게) 처리를 할 수 있다. 단, 여러 데이터가 나열될 때 특정 1개의 데이터만 임의로 강조하는 것은 지양하며 일관된 기준을 적용한다.
* ✅ **Divider (구분선) 적용:** 표출해야 할 데이터 항목이 3개 이상일 경우, 정보의 가독성을 높이기 위해 `Divider`를 사용하여 섹션을 분리한다.
* ✅ **일관된 정렬:** Divider로 분리된 섹션 안에서는 텍스트 정렬(좌측, 중앙 등) 방식을 동일하게 통일하여 혼용하지 않는다.

**Usage (Sum 타입 및 반응형 규칙)**
* ✅ **Sum 타입 활용:** 총합(Sum) 데이터를 보여주는 타입은 상세 데이터를 확인할 수 있도록 확장/축소(Expand/Collapse) 기능을 제공한다. 필요 시 상세 데이터로 이동하는 링크(Link)나 버튼 기능을 추가할 수 있다.
* ✅ **Compact (모바일) 배치:** 화면 너비에 맞춰 `Horizontal`과 `Vertical` 형태를 모두 유연하게 사용할 수 있다.
* ✅ **Wide (웹) 배치:** `Horizontal`, `Vertical` 형태 모두 1행(Row)에 **최대 3개까지** 나란히 배치할 수 있다. (카드 간 간격은 32px 유지)

**접근성 (Accessibility)**
* 데이터와 레이블이 짝을 이루는 구조이므로, 스크린 리더 사용자가 레이블과 그에 해당하는 데이터 값을 명확히 연결하여 읽을 수 있도록 HTML 마크업(예: `<dl>`, `<dt>`, `<dd>` 활용 또는 `aria-labelledby`)을 논리적으로 구성한다.
* Sum 타입의 확장/축소 버튼에는 `aria-expanded="true/false"` 속성을 부여하여 현재 펼쳐짐 상태를 안내한다.
---

#### Content Data Box

#### Content data box

**정의**
가장 중요한 핵심 데이터를 비주얼 이미지와 함께 조합하여 사용자에게 직관적으로 강조할 때 사용하는 박스 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (데이터 위주), `image` (이미지 포함) |
| Layout | `horizontal` (좌우 배치), `vertical` (상하 배치) |
| Buttons | `0` (생략), `1` (CTA 단독), `2` (CTA + Secondary) |

**Usage (구성 및 텍스트 규칙)**
* ✅ **필수 및 선택 요소:** 핵심 정보인 **Data(데이터)**는 필수로 표출해야 하며, Icon, Tooltip, Button은 상황에 따라 선택적으로 사용할 수 있다.
* ✅ **버튼 구성:** 하단 액션 버튼은 최대 2개(Primary CTA, Secondary)까지 조합하여 사용할 수 있으며, 필요 없는 경우 생략할 수 있다.
* ✅ **데이터 배치 (방향성):**
  * 레이블과 데이터의 자리 수가 짧을 경우 `Horizontal`(가로형)을 사용할 수 있다.
  * 다국어 등 레이블이 길거나 데이터의 자리 수가 많은 경우 가독성을 위해 `Vertical`(세로형) 사용을 권장한다.
* ✅ **Divider 적용:** 여러 개의 데이터를 나열할 경우 데이터 사이에 `Divider`를 적용하여 시각적으로 구분한다. 단, 가장 마지막 데이터 항목 뒤에는 Divider를 사용하지 않는다.

**Usage (해상도 및 반응형 배치 규칙)**
* ✅ **Compact (모바일) 배치:**
  * 화면 너비의 한계로 인해 데이터 텍스트가 긴 경우, 가로형보다 글자 수에 유연하게 대응할 수 있는 `Vertical`(세로형) 배치를 권장한다.
  * 1행에 1개씩 꽉 차게(Full width) 배치한다.
* ✅ **Wide (웹) 배치:**
  * 텍스트 공간이 상대적으로 여유로우므로 `Horizontal`(가로형) 레이아웃을 폭넓게 사용할 수 있다. 반대로 텍스트가 너무 짧아 여백이 과도하게 발생할 경우 `Vertical`(세로형)로 전환하여 밸런스를 맞춘다.
  * `Vertical` 형태의 컴포넌트는 1행에 **최대 2개까지**만 나란히 배치하며, 3개 이상부터는 다음 행으로 내려서 배치한다.

**Usage (이미지 규칙)**
* ✅ **비율 및 크기:** 해상도와 타입에 따라 두 가지 이미지 비율을 다르게 적용한다.
  * `Compact-sm`: **3:2 비율**의 이미지를 사용한다.
  * `Compact-lg` 및 `Wide`: **1:1 비율**의 이미지를 사용한다.
* ✅ **Wide 환경 이미지 고정:** Wide 해상도에서 화면 너비가 길어지더라도 이미지의 최대 높이(230px)와 비율은 변하지 않으며, 컨테이너의 우측 하단에 고정된 상태로 컴포넌트의 전체 너비만 넓어진다.

**접근성 (Accessibility)**
* 데이터 레이블과 실제 데이터 값이 논리적으로 연결되도록 마크업을 구성하여, 스크린 리더 사용자가 각 숫자가 의미하는 바를 명확히 인지할 수 있도록 돕는다.
* 포함된 배경 이미지가 정보 전달 목적을 가질 경우 `alt` 텍스트를 제공한다.

---

#### Image-text Box

#### Image text box

**정의**
시각적으로 강조된 비주얼 이미지와 설명 텍스트, 그리고 다중 액션이 가능한 버튼으로 구성된 박스 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic`, `option` (Title 강조 및 그래픽 요소 추가형) |
| Layout | `horizontal` (좌우 배치), `vertical` (상하 배치) |
| Buttons | `0` (생략), `1` (CTA 단독), `2` (CTA + Secondary) |

**Usage (Image card와의 구분)**
* ✅ **클릭 영역 및 액션 수:** `Image card`는 카드 전체 영역이 클릭 가능한 단일 액션 요소인 반면, `Image text box`는 카드 전체를 클릭할 수 없고 **내부에 삽입된 버튼(Button) 영역만 클릭 가능**하며, 버튼의 개수만큼 여러 개의 개별 동작(액션)을 수행할 수 있다.

**Usage (이미지 및 텍스트 규칙)**
* ✅ **단일 이미지 대응:** 하나의 원본 이미지로 Compact, Wide 등 모든 해상도 레이아웃에 대응할 수 있도록 핵심 피사체를 고려하여 제작한다.
* ✅ **이미지 비율 및 영역:** * `Vertical` (세로형): 이미지 가로세로 비율을 **3:2**로 고정하여 사용한다.
  * `Horizontal` (가로형): 컨테이너 전체 너비의 **약 35%**를 이미지 영역으로 할당한다.
* ✅ **Option 타입 활용:** `Option` 타입은 Title과 Description 영역을 분리하고 그래픽 요소를 더해 특정 Title을 더욱 강하게 강조하고자 할 때 사용한다.

**Usage (버튼 및 레이아웃 규칙)**
* ✅ **버튼 제약:** 하단 버튼은 최대 2개(CTA + Secondary)까지 사용할 수 있으며 생략도 가능하다.
* ✅ **최대 높이 통일:** 여러 개의 박스가 같은 행(Row)에 나란히 배치될 경우, 텍스트 분량 차이로 높이가 다르더라도 **가장 높은 박스의 높이에 맞춰 모든 박스의 높이를 일괄 통일**한다.
* ✅ **다중 배치 시 버튼 스타일 (Wide - Vertical):**
  * Wide 해상도에서 CTA 버튼(버튼 형태)이 포함된 세로형 박스는 1행에 최대 2개(각 50%)까지만 배치 가능하다.
  * 만약 1행에 3개 이상을 배치해야 할 경우, 화면의 시각적 복잡도를 낮추기 위해 **버튼 형태가 아닌 텍스트 링크(Link) 스타일**로 변경하여 적용한다.

**Usage (해상도 및 반응형 배치 규칙)**
* ✅ **Compact (모바일):** 주로 `Vertical`(세로형) 배치를 사용하며, 너비를 꽉 채워(Full) 하단으로 나열한다.
* ✅ **Wide (웹):**
  * `Basic (Horizontal)`: 1행에 1개씩 전체 너비를 사용하여 배치한다.
  * `Basic (Vertical)`: 1행에 최대 3개까지 배치 가능하다. 1~2개만 배치할 때는 남는 공간을 여백으로 비워둔다.
  * `Option`: 1개 배치 시 100%(Full), 2개 배치 시 50%씩 분할하여 배치한다. 
  * 기준 영역을 초과하는 항목은 Carousel(캐러셀)을 적용하지 않고 자연스럽게 다음 행으로 개행하여 배치한다.

---

#### Text Box

#### Text box

**정의**
사용자가 반드시 인지해야 하는 중요한 텍스트 정보를 시각적으로 강조하기 위해 배경색상과 부가 요소(버튼, 이미지 등)를 조합하여 구성한 박스 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Background Color | `highlight` (최중요), `gray` (기본), `white-line` (외곽선) |
| Add-on Elements | `button`, `link`, `badge`, `image` (모두 선택 사항) |
| Layout | `compact` (모바일/수직형), `wide` (웹/수평형) |

**Usage (구성 및 텍스트 규칙)**
* ✅ **텍스트 필수:** Text box의 핵심 목적은 텍스트 강조이므로, 내부에 텍스트 없이 단독으로 사용할 수 없다. (Button, Badge, Image는 텍스트를 보조하는 수단이다.)
* ✅ **배경색 적용 기준:**
  * `Highlight`: 화면 내에서 가장 중요한 정보에만 사용하며, 반드시 **CTA 버튼과 함께** 사용해야 한다.
  * `Gray` & `White-line`: 일반적인 강조 시 사용하며, 두 가지 옵션 중 `Gray` 배경을 우선적으로 사용한다.
* ✅ **최대 높이 통일:** 여러 개의 텍스트 박스가 같은 행(Row)에 배치될 때 내부 텍스트 분량이 다르더라도 **가장 높은 박스를 기준으로 모든 박스의 높이를 통일**한다. (Wide 환경 최소 높이는 텍스트 2줄 기준 128px 보장).

**Usage (버튼 및 링크 규칙)**
* ✅ **버튼 개수 및 배치:**
  * 버튼은 최대 2개(Primary + Secondary 조합)까지 사용할 수 있다.
  * 일관된 경험을 위해 CTA(Primary) 버튼은 **Compact 해상도에서는 우측 상단**에, **Wide 해상도에서는 우측 하단**에 배치한다.
* ✅ **화면 내 CTA 제한:** Text box에 CTA 버튼이 포함된 경우, 해당 박스는 한 화면에 **최대 2개**까지만 배치한다. (2개 배치 시 화면 너비의 50%씩 분할하여 나란히 배치).
* ✅ **링크 스타일:** Text box 내부에서 `Link`를 사용할 때는 반드시 Underline(밑줄) 스타일을 적용한다.

**Usage (이미지 규칙)**
* ✅ **투명 이미지 사용:** 이미지 요소는 텍스트를 부각시키는 장식용이므로 배경이 투명하게 외곽선이 따진 이미지(PNG/SVG)만 사용한다.
* ✅ **해상도별 이미지 동작:**
  * `Compact`: 이미지 비율의 변화 없이 우측 하단에 고정되며, 320~1059px 구간에서 동일한 크기로 표출된다.
  * `Wide`: 최대 높이 210px 제한 내에서, 컨테이너 영역을 기준으로 비율을 유지한 채 유동적으로 확장된다.

**Usage (해상도 및 반응형 규칙)**
* ✅ **Compact (모바일):** 1행에 1개씩 꽉 차게(Full) 배치하며, 2개 이상 사용할 경우 하단 행으로 개행하여 나열한다.
* ✅ **Wide (웹):** 1행에 전체 너비(100%)로 1개만 배치하거나, 절반 너비(50%)로 2개까지 나란히 배치할 수 있다.

**접근성 (Accessibility)**
* 강조된 텍스트가 시각적인 형태뿐만 아니라 스크린 리더 사용자에게도 중요도가 전달될 수 있도록 `<strong>` 태그를 적절히 사용하거나, 내용에 따라 `role="note"` 또는 `role="region"`을 적용하고 `aria-label`을 제공한다.

---

#### Boarding Pass

**정의**
항공 탑승권 정보를 표시하는 대한항공 핵심 도메인 카드 컴포넌트.

**목적**
- 디지털 탑승권으로 탑승에 필요한 모든 정보를 표시한다.

**포함 요소**
- 출발지 IATA 코드 + 도시명 + 출발 시간
- 목적지 IATA 코드 + 도시명 + 도착 시간
- 항공편명 (예: KE 001)
- 탑승 날짜 및 시간
- 탑승구 (Gate)
- 좌석 번호 (Seat)
- 탑승 마감 시간
- 승객명
- 좌석 등급
- 바코드 또는 QR코드

**Variants**
| Property | Values |
|----------|--------|
| Class | `economy`, `prestige`, `first` |
| Status | `active`, `used`, `cancelled` |

**토큰 매핑**
| Class | Background | Text |
|-------|-----------|------|
| Economy | `color/fill/surface/economy` (#FFFFFF) | `color/text/body` |
| Prestige | `color/fill/surface/prestige` (#051766) | `color/text/inverse` |
| First | `color/fill/surface/first` (#5E5E5E) | `color/text/inverse` |

---

#### Voucher

#### Voucher

**정의**
기프트카드, 쿠폰, 바우처 등 사용자가 받을 수 있는 혜택 정보를 직관적인 문구와 시각적 요소로 간결하게 제공하는 카드 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `gift-card` (기프트카드), `coupon` (바우처/쿠폰) |
| State | `enabled` (사용 가능), `hovered`, `focused`, `pressed`, `aria-disabled` (기간 만료/사용 완료) |
| Columns | `1-col`, `3-col`, `4-col` (해상도에 따라 반응형 적용) |

**Usage (구성 및 텍스트 규칙)**
* ✅ **간결한 정보 제공:** 사용자가 어떤 혜택을 받을 수 있는지 직관적인 핵심 문구만 표출한다. 유효기간이나 상세 사용처 등 복잡한 정보는 상세 보기 화면(Bottom sheet 등)으로 위임하여 카드 내부를 간결하게 유지한다.
* ✅ **Badge 조합:** 카드 우측 상단에 최대 3개까지 Badge를 조합하여 사용할 수 있다. 배치는 정보 제공 목적의 `Extra` 타입을 먼저 두고, 사용 상태를 나타내는 `Using state` 타입을 그 뒤에 배치한다.
* ✅ **긴 텍스트 표출:** 하단에 표출되는 기간 등 보조 텍스트는 1줄 이내 작성을 권장한다. 텍스트가 길어질 경우 자동 개행되며 카드의 높이가 확장된다.

**Usage (레이아웃 및 반응형 규칙)**
* ✅ **최대 높이 통일 및 확장 영역:** 여러 개의 Voucher가 같은 행(Row)에 배치될 때, 텍스트 분량 차이로 높이가 다르더라도 **가장 높은 카드를 기준으로 모든 카드의 높이를 통일**한다. 이때 텍스트가 있는 하단 영역을 늘리는 것이 아니라, **상단 이미지/배경 영역의 높이를 확장**하여 맞춘다.
* ✅ **최소 높이 보장:** 해상도별로 최소 높이를 보장하여 터치 영역 및 시각적 안정감을 유지한다. (Compact: 152px / Wide: 196px)
* ✅ **해상도별 단(Column) 배치:**
  * `Compact-sm`: 1행 1열 (세로 1줄로 나열)
  * `Compact-lg` & `Wide-sm`: 1행 3열 (가로 3개씩 배치)
  * `Wide-lg`: 1행 4열 (가로 4개씩 배치)

**Usage (상태 표출 규칙)**
* ✅ **만료 및 사용 완료 상태:** '기간 만료' 또는 '사용 완료'된 바우처는 '사용 가능' 상태와 명확히 구분되도록 비활성화 색상(Dimmed/Gray)으로 처리한다. 상태 표시를 위해 상단에 별도의 탭(Tab) 형태 상태 인디케이터를 부착하여 안내한다.

**접근성 (Accessibility)**
* 카드 전체가 상세 정보로 진입하는 상호작용 요소이므로, 시맨틱 `<button>` 태그를 사용하거나 `role="button"`을 적용한다.
* '기간 만료'나 '사용 완료' 상태의 카드에는 `aria-disabled="true"` 속성을 부여하여 스크린 리더 사용자가 현재 사용할 수 없는 혜택임을 명확히 인지할 수 있도록 한다.

---

### 3.7 리스트 & 테이블 (List & Table)

---

#### List

#### List

**정의**
순서가 있거나 순서가 없는 여러 개의 문장(항목)을 체계적으로 나열하여 설명할 때 사용하는 텍스트 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `ordered` (순서 있음), `unordered` (순서 없음) |
| Size | `sm`, `md` |
| Columns | `1-column` (Compact/Wide 공통), `2-column` (Wide 전용) |
| Add-on | `link`, `disclaimer` |

**Usage (유형 및 뎁스 규칙)**
* ✅ **Ordered (순서형):** 절차, 우선순위 등 순서가 중요한 목록에 사용하며, 뎁스(1~3 Depth)에 따라 시스템에 지정된 숫자/알파벳 기호를 사용한다.
* ✅ **Unordered (비순서형):** 순서가 중요하지 않은 항목을 병렬로 나열할 때 사용하며, 뎁스(1~3 Depth)에 따라 지정된 불릿(Bullet) 기호를 사용한다.
* ✅ **Paragraph 대체:** 원래 단일 문장은 `Paragraph`를 사용하는 것이 원칙이나, 주변에 그룹핑된 다른 항목들이 모두 `List`로 작성되어 있어 시각적 통일성이 필요한 경우에는 예외적으로 단일 문장도 List 형태로 대체하여 사용할 수 있다.

**Usage (텍스트 및 조합 규칙)**
* ✅ **텍스트 강조:** 목록 내의 특정 단어에 시선을 유도하고 싶을 때 **Bold(굵게)** 스타일을 적용할 수 있다.
* ✅ **Link 조합:** 리스트 항목 하단에 관련된 Link를 추가할 수 있다.
  * 외부로 이동하는 경우 '새 창 열림' 아이콘을 함께 제공해 시각적으로 구분한다.
  * 링크가 **2개 이상**일 경우, 가로로 나열하지 않고 **상하(세로)로 4px 간격**을 두고 배치한다.
* ✅ **Disclaimer 조합:** 리스트 항목에 부가적인 제약 사항이나 설명이 필요할 경우 하단에 Disclaimer를 조합하여 표출할 수 있다.

**Usage (레이아웃 및 반응형 규칙)**
* ✅ **간격(Spacing):** 항목 간의 수직 간격은 콘텐츠 밀도에 따라 4px 또는 8px을 적용한다.
* ✅ **Compact (모바일):** 1단(1-column) 배치만 허용되며, 하단으로 길게 나열한다.
* ✅ **Wide (웹):** 텍스트의 길이나 화면의 여백에 따라 1단(1-column) 또는 2단(2-column) 배치를 유연하게 선택하여 사용할 수 있다.

**접근성 (Accessibility)**
* 스크린 리더가 목록의 총 항목 개수와 현재 읽고 있는 위치를 정확히 파악할 수 있도록 반드시 시맨틱 마크업(Ordered: `<ol>`, Unordered: `<ul>`, 각 항목: `<li>`)을 준수해야 한다.
* 스크린 리더는 `<li>` 태그 내부의 불릿 기호나 숫자를 자동으로 인식하여 읽어주므로, 텍스트 소스 자체에 불릿이나 번호를 중복해서 타이핑(하드코딩)하지 않도록 주의한다.

---

#### Listbox

#### Listbox

**정의**
사용자가 여러 개의 옵션 리스트 중에서 한 개 이상의 옵션을 확인하고 선택할 수 있도록 제공하는 목록형 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| State | `enabled` (default), `hovered`, `focused`, `pressed`, `selected`, `disabled` |

**Usage (텍스트 및 정렬 규칙)**
* ✅ **항목 정렬:** 사용자가 원하는 옵션을 빠르게 탐색할 수 있도록, 리스트 내 옵션들은 기본적으로 **가나다순(다국어의 경우 알파벳순)**으로 정렬하여 제공한다.
* ✅ **긴 텍스트 표출:** 옵션의 텍스트가 리스트 컨테이너의 최대 너비 값을 초과할 경우, 말줄임표(...)로 잘리지 않고 **아래로 자동 개행(줄바꿈)**되어 전체 텍스트가 표출되도록 처리한다.

**Usage (스크롤 및 레이아웃 규칙)**
* ✅ **최대 표출 개수:** 화면의 공간 효율성을 위해 한 번에 **최대 8개**의 옵션까지만 노출하는 것을 권장한다.
* ✅ **스크롤 바 제공:** 옵션이 8개를 초과할 경우, 컴포넌트 높이를 고정하고 내부에 **세로 스크롤 바(Scroll bar)**를 생성하여 나머지 옵션을 탐색할 수 있도록 한다.
* ✅ **반응형 최대 너비 (Max-width):** 해상도별로 지정된 최대 너비 제약을 준수하여 과도하게 늘어나지 않도록 방어한다.
  * `Compact`: 모바일 기기 크기에 따라 최대 335px ~ 1059px 적용
  * `Wide`: 최대 1736px 적용

**접근성 (Accessibility)**
* 스크린 리더 사용자가 목록임을 인지할 수 있도록 컨테이너에 `role="listbox"`를, 개별 옵션에 `role="option"`을 부여한다.
* 선택된 항목에는 `aria-selected="true"` 속성을 적용하여 상태 변화를 명확히 전달한다.
* 마우스뿐만 아니라 키보드의 상/하 방향키(Up/Down Arrow)를 통해서도 옵션을 탐색하고 `Enter`나 `Space`로 선택할 수 있도록 키보드 접근성을 지원해야 한다.

---

#### Data Table

**정의**
행과 열로 구성된 데이터를 표시하는 테이블 컴포넌트.

**목적**
- 운임 비교, 예약 내역, 마일리지 적립 내역 등 구조화된 데이터를 제공한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic`, `sortable`, `selectable` |
| Density | `comfortable`, `compact` |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Header background | `color/fill/surface/secondary` |
| Row background | `color/fill/surface/primary` |
| Row hover | `color/fill/interaction/selected-item` |
| Border | `color/border/divider-secondary` |#### Data table

**정의**
여러 개의 행(Row)과 열(Column)로 구성된 데이터를 표출하여, 사용자가 데이터 간의 차이를 쉽게 비교하고 탐색할 수 있도록 돕는 표 형태의 컴포넌트. (반드시 표 형태의 비교가 필요한 데이터에만 제한적으로 사용한다.)

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic (fluid)`, `horizontal-scroll`, `stack` |
| Row Height | `normal` (넓게 보기), `narrow` (좁게 보기) |
| Stack Style | `box`, `line` |

**Usage (유형 및 반응형 규칙)**
* ✅ **Basic (Fluid):** 3개 이하의 열로 구성된 비교적 단순한 테이블에 사용한다. 해상도(Compact/Wide)에 관계없이 화면 너비에 맞춰 유동적으로 동일한 경험을 제공한다.
* ✅ **Horizontal scroll:** 열(Column)의 개수가 많은 테이블에 사용한다. 좌측의 제목 열을 고정하고 우측의 데이터 열 영역만 가로로 스크롤하여 탐색하도록 구성한다.
* ✅ **Stack:** 열과 행이 모두 많아 모바일 등 좁은 화면에서 가로 스크롤로 감당하기 어려운 경우 사용한다. 행과 열의 주요 정보를 상하로 그룹화(Stack)하여 가로 스크롤 없이 수직적으로 보여준다.

**Usage (데이터 정렬 및 표출 규칙)**
* ✅ **텍스트 정렬 (Left):** 헤더(Header)를 포함한 일반적인 텍스트 데이터의 기본 정렬은 **좌측 정렬**을 사용하여 탐색의 편의성을 높인다.
* ✅ **수치 정렬 (Right):** 통화(금액), 퍼센트 등 숫자의 크기 비교가 중요한 수치 데이터는 **우측 정렬**을 사용하여 자릿수와 크기를 빠르게 비교할 수 있게 한다.
* ✅ **데이터 정렬 (Sort):** 정렬 기능이 제공되는 열의 경우, 초기 진입 시 **내림차순**을 기본으로 하며 다시 누르면 **오름차순**으로 변경된다.
* ✅ **행 높이 (Row Height):** 데이터의 성격에 따라 넓게(`Normal`- 복잡한 데이터 탐색) 또는 좁게(`Narrow` - 한눈에 많은 데이터 확인) 설정하여 가독성을 조절한다.

**Usage (부가 요소 및 Stack 규칙)**
* ✅ **부가 정보 표출:** 테이블의 보조 설명(Subtitle)은 제목 하단에, 단위와 같은 부가 정보는 테이블 우측 상단에 배치하며 최대 2개까지만 표출한다.
* ✅ **Stack 타입 정렬 및 버튼:** Stack 타입 내에서도 일반 텍스트는 좌측, 수치 데이터는 우측 정렬 기준을 동일하게 준수한다. 필요 시 Stack의 헤더 상단 영역에 제어용 버튼을 배치할 수 있다.

**접근성 (Accessibility)**
* 스크린 리더 사용자가 데이터의 구조를 이해할 수 있도록 시맨틱 HTML 테이블 태그(`<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`)를 엄격하게 준수한다.
* 제목 셀(`<th>`)에는 반드시 `scope="row"` 또는 `scope="col"` 속성을 제공하여 데이터 셀과의 관계를 명확히 선언한다.
* 테이블 캡션(`<caption>`)을 제공하여 테이블이 어떤 데이터를 담고 있는지 화면 낭독기가 먼저 읽어줄 수 있도록 구성한다.

---

#### Board List

**정의**
게시판 형태로 제목, 날짜, 카테고리 등을 표시하는 리스트.

**목적**
- 공지사항, FAQ, 이벤트 목록 등 게시판형 콘텐츠를 나열한다.

---

#### Board View

**정의**
게시판 상세 내용을 표시하는 컴포넌트.

**목적**
- Board List에서 선택한 항목의 상세 콘텐츠를 표시한다.

---

#### Link Group

#### Link group

**정의**
동등한 레벨이나 서로 연관된 성격의 Link(링크)들을 세 개 이상 묶어, 시각적인 그룹으로 사용자에게 제공하는 네비게이션 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (로고/아이콘 + 레이블 텍스트 조합), `logo` (로고/아이콘 단독) |
| State | `enabled` (default), `hovered`, `focused`, `pressed` |

**Usage (구성 및 레이블 규칙)**
* ✅ **그룹 레이블 사용:** 묶여 있는 링크들의 공통된 성격(예: 소셜 미디어, 패밀리 사이트 등)을 설명하는 텍스트 레이블(Group Label)을 상단 또는 좌측에 선택적으로 제공할 수 있다.
* ✅ **레이블 생략 (Logo 타입):** 아이콘이나 로고 이미지만으로도 사용자가 해당 링크의 목적지를 명확히 인지할 수 있는 경우(예: 인스타그램, 유튜브 등 유명 로고), 시각적인 텍스트 레이블을 생략하고 로고 단독으로만 구성하여 화면을 깔끔하게 유지한다.

**Usage (해상도 및 반응형 배치 규칙)**
* ✅ **Compact (모바일):** 화면 너비가 좁은 모바일이나 태블릿 환경에서는 각 링크 항목을 **1단(1-column)**으로 세로 배치하여 스크롤 탐색이 용이하도록 한다.
* ✅ **Wide (웹):** 화면 여유 공간이 넓은 데스크탑 환경에서는 링크 항목들을 가로로 나열하는 **2단(2-column) 이상**의 다단 레이아웃으로 배치하여 공간 효율성을 높인다.

**접근성 (Accessibility)**
* 논리적으로 연관된 링크의 묶음이므로 `<ul>`과 `<li>`를 사용해 목록 형태로 마크업하고, 전체 그룹을 `<nav>` 태그로 감싸 시맨틱 구조를 명확히 한다.
* **Logo 타입(텍스트 생략):** 시각적 텍스트가 생략된 로고 전용 링크의 경우, 스크린 리더 사용자가 목적지를 알 수 있도록 `aria-label`이나 `<span class="sr-only">인스타그램</span>`과 같은 숨김 텍스트를 반드시 제공해야 한다.

---

#### Order List

#### Order list

**정의**
사용자가 수행해야 할 절차나 순서가 있는 단계를 리스트 형태로 구성하여 시각적으로 안내하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (제목 + 간략한 설명), `detail` (상세 설명 포함) |
| Orientation | `horizontal` (가로형 - Wide 전용), `vertical` (세로형) |
| Add-on | `expander` (Detail 전용), `button` (하단 CTA) |

**Usage (구성 및 텍스트 규칙)**
* ✅ **아이콘 필수:** 각 단계를 직관적으로 이해하는 데 도움을 주는 아이콘을 반드시 포함해야 하며 생략할 수 없다.
* ✅ **상세 설명 (Detail):** 각 단계에 대한 설명은 `Paragraph` 또는 `List` 컴포넌트를 활용하여 작성한다. 단, 복잡도를 낮추기 위해 상세 설명은 1-depth(1단 구조)로만 제한하여 사용한다.
* ✅ **Expander 활용:** `Detail` 타입에서 설명이 지나치게 길어지는 경우, 간결한 인터페이스 유지를 위해 `Expander` 컴포넌트를 적용하여 텍스트를 확장/축소할 수 있도록 구성한다.
* ✅ **긴 텍스트 개행:** 텍스트가 길어지면 자동으로 개행되며, 전체 컨테이너의 높이가 유동적으로 늘어난다.

**Usage (해상도 및 반응형 배치 규칙)**
* ✅ **Compact (모바일):** `Vertical`(세로형) 배치만 사용하며, 하단에 CTA 버튼을 배치할 경우 화면 전체 너비(Full-width)로 적용한다.
* ✅ **Wide (웹) 방향성:** Title의 길이가 길면 `Vertical`(세로형)을, 비교적 짧으면 `Horizontal`(가로형) 배치를 권장한다.
* ✅ **Wide (웹) 가로형 다중 배치 룰:**
  * **5단계 이하:** 1행에 최대 5개까지 나란히 배치한다.
  * **6단계 이상:** 최대 2행까지 분할하여 배치한다.
  * **홀수/짝수 분배:** 전체 단계 개수가 짝수면 각 행에 동일한 개수를 배치하고, 홀수인 경우 첫 번째 행에 더 많은 개수를 배치하여 시각적 안정감을 준다. (예: 7단계 = 1행 4개 + 2행 3개)

**접근성 (Accessibility)**
* 시각적인 단계뿐만 아니라 스크린 리더 사용자도 순서를 명확히 인지할 수 있도록 시맨틱 HTML인 `<ol>`과 `<li>`를 사용하여 마크업한다.
* `Expander`를 사용해 상세 설명을 숨김/노출하는 경우, 제어 버튼에 `aria-expanded` 속성을 제공하여 현재 열림/닫힘 상태를 스크린 리더에 전달해야 한다.
---

#### Order List Tab

#### Order list tab

**정의**
순서가 있는 여러 단계를 탭(Tab) 형태로 구성하여, 각 탭 버튼을 누를 때마다 해당 단계의 상세 설명(콘텐츠)을 패널 영역에 표출하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Layout | `compact` (탭과 패널 상하 배치), `wide` (탭과 패널 좌우 또는 상하 배치) |
| State | `enabled`, `hovered`, `focused` (selected / unselected 각각 존재) |

**Usage (탭 버튼 및 텍스트 규칙)**
* ✅ **단계 표기 자동화:** 단계 레이블은 모든 언어에서 일관되게 `"Step N/N"` (예: Step 1/3) 형식으로 자동 표출된다. 순서는 항상 좌측에서 우측으로 진행된다.
* ✅ **텍스트 개행 제한:** 탭 버튼의 제목 텍스트가 최대 너비를 초과할 경우 개행되어 표출되며, 가독성을 위해 `Compact`는 최대 3줄, `Wide`는 최대 2줄까지만 허용한다.
* ✅ **정렬 (Alignment):** 탭 버튼 내부의 화살표(Arrow) 아이콘은 버튼 높이 기준 수직 중앙에 배치하며, 설명 텍스트는 하단 정렬을 적용한다.

**Usage (탭 패널 및 콘텐츠 규칙)**
* ✅ **콘텐츠 구성:** Tab 패널 내부에는 각 단계를 상세히 설명하기 위해 Image, Button, List, Paragraph 등 다양한 컴포넌트를 복합적으로 사용할 수 있다. 단, 일관성을 위해 각 단계별 Tab 패널의 구성 항목과 레이아웃은 가급적 통일하는 것을 권장한다.
* ✅ **이미지 비율:** 단계별 화면 스크린샷 등 이미지를 삽입할 경우, 사용자의 시청 환경을 고려하여 `Compact`는 모바일 비율(세로형) 이미지를, `Wide`는 데스크톱 비율(가로형) 이미지를 적용할 수 있다.

**Usage (인터랙션 및 반응형 규칙)**
* ✅ **자동 스크롤 (중앙 이동):** 활성화(선택)된 Tab 버튼은 항상 화면에 노출되어야 한다. 사용자가 스와이프하여 화면 밖으로 가려진 탭 버튼을 클릭/터치하면, 해당 탭 버튼이 화면의 중앙으로 자동 스크롤(이동)되며 활성화된다.

**접근성 (Accessibility)**
* 키보드 및 스크린 리더 사용자가 탭과 탭 패널의 관계를 명확히 인지할 수 있도록 WAI-ARIA `role="tablist"`, `role="tab"`, `role="tabpanel"` 패턴을 엄격하게 적용한다.
* 탭 버튼에 `aria-controls`를 제공하여 패널과 연결하고, 현재 선택된 탭에는 `aria-selected="true"`를 부여하여 상태를 안내한다.

---

### 3.8 복합 & 도메인 (Complex & Domain)

---

#### Accordion

#### Accordion

**정의**
여러 개의 제목(Heading)과 상세 콘텐츠를 수직으로 쌓아 구조화하고, 사용자가 원하는 항목만 확장(Expand)하거나 축소(Collapse)하여 볼 수 있도록 제어하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (일반 콘텐츠용), `faq` (Q&A 목록용) |
| State | `collapse` (축소됨), `expand` (확장됨) |
| Status | `enabled` (default), `hovered`, `focused` |
| Add-on | `icon` (제목 앞 아이콘), `switch` (모두 펼치기/접기 버튼) |

**Usage (동작 및 인터랙션 규칙)**
* ✅ **클릭 영역:** 제목 영역(헤더)의 어느 곳을 누르더라도 콘텐츠 섹션이 확대/축소되어야 한다. 이를 위해 헤더 내에는 확장 제어 외의 다른 인터랙티브 요소(버튼, 링크 등)를 배치하지 않는다.
* ✅ **초기 상태:** 화면 진입 시 초기 상태는 축소(Collapse)를 기본으로 하나, 중요도에 따라 특정 항목을 확장(Expand) 상태로 표출할 수도 있다.
* ✅ **확장 방식:** 인터랙션 정책에 따라 1개의 섹션만 열리게 제한(하나가 열리면 나머지는 닫힘)하거나, 여러 개의 섹션이 동시에 확장되도록 허용할 수 있다.
* ✅ **모두 펼치기:** 여러 섹션을 한 번에 확장/축소할 수 있는 제어 스위치(Switch) 컴포넌트를 최상단 우측에 선택적으로 배치할 수 있다.

**Usage (구성 및 텍스트 규칙)**
* ✅ **FAQ 필수 요소:** `FAQ` 타입에서는 "Q(질문)"와 "A(답변)"를 나타내는 Heading을 생략 없이 필수로 사용해야 한다. (`Basic` 타입에서는 Heading 생략 가능)
* ✅ **긴 텍스트 개행:** 모바일(Compact) 등에서 제목 텍스트가 길어질 경우, 자동 개행되며 우측의 확장/축소 화살표(Switch) 아이콘은 하단으로 이동하지 않고 항상 상단(Top) 기준을 유지한다.
* ✅ **아이콘 통일:** 제목 좌측에 아이콘을 사용할 경우, 특정 섹션만 단독으로 사용하지 않고 전체 그룹의 모든 항목에 일관되게 적용하여 시각적 통일성을 맞춘다.

**Usage (콘텐츠 및 다중 표출 규칙)**
* ✅ **콘텐츠 확장성:** 확장된 하위 패널 안에는 Text(Paragraph), List, Image 등 다양한 컴포넌트를 자유롭게 포함하여 구성할 수 있다.
* ✅ **Load more 연계:** 아코디언 항목(섹션)의 개수가 너무 많아 한 화면에 전부 표출하기 부담스러운 경우, `Load more` 컴포넌트와 연계하여 리스트를 단계적으로 불러오도록 구성한다.

**접근성 (Accessibility)**
* 헤더 역할을 하는 `<button>`에는 `aria-expanded="true/false"` 속성을 부여하여 현재 아코디언 패널이 열려 있는지 닫혀 있는지를 스크린 리더 사용자에게 실시간으로 안내한다.
* 아코디언 버튼(`aria-controls`)과 상세 콘텐츠 패널(`id`)의 고유 속성값을 서로 매칭하여 두 요소가 논리적으로 연결되어 있음을 보장한다.

---

#### Expander

#### Expander

**정의**
제한된 공간에서 세부 정보를 효율적으로 표시하기 위해, 단일 제목과 콘텐츠를 세트로 묶어 확장(Expand) 또는 축소(Collapse)할 수 있도록 제공하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (일반 콘텐츠용), `segment` (작은 영역 또는 컴포넌트 내부용) |
| State | `collapse` (축소됨), `expand` (확장됨) |
| Color | `white` (중요도 상), `gray` (중요도 하) |

**Usage (Accordion과의 구분)**
* ✅ **단독 사용:** `Expander`는 **독립적인 단일 항목**의 확장/축소가 필요할 때 사용한다. 여러 개의 확장/축소 세트를 논리적인 계층 구조로 그룹화해야 할 경우에는 `Expander`를 나열하지 않고 반드시 `Accordion` 컴포넌트로 대체하여 사용한다.

**Usage (구성 및 색상 규칙)**
* ✅ **초기 상태:** 기본적으로 축소(Collapse) 상태로 제공하며, 사용자가 버튼(제어 영역)을 누르면 콘텐츠가 확장된다. (축소 상태에서는 상세 내용을 볼 수 없으므로, 즉시 노출되어야 하는 매우 중요한 콘텐츠에는 적용하지 않는다.)
* ✅ **배경 색상 적용 (중요도 분기):**
  * `White`: 마일리지, 결제 금액 데이터 등 **비교적 중요도가 높은 콘텐츠**를 표출할 때 사용한다.
  * `Gray`: 유의사항 등 **텍스트 위주의 중요도가 낮은 보조 콘텐츠**를 표출할 때 사용한다.
* ✅ **콘텐츠 패널 조합:** 패널 영역 내부에는 단순 텍스트(Paragraph)뿐만 아니라 Data, List, Image, Video, Button 등 상황에 맞는 다양한 컴포넌트를 조합하여 활용할 수 있다.

**Usage (Segment 타입 규칙)**
* ✅ `Segment` 타입은 여백이 좁은 특정 컴포넌트(예: Order list 등) 내부에서 부분적인 확장/축소가 필요할 때 제한적으로 사용한다.

**접근성 (Accessibility)**
* 사용자가 확장/축소를 제어하는 버튼에 `aria-expanded="true/false"` 속성을 부여하여 현재 콘텐츠 패널이 열려 있는지 닫혀 있는지를 스크린 리더 사용자에게 실시간으로 안내한다.
* 제어 버튼(`aria-controls`)과 상세 콘텐츠 패널(`id`)의 고유 속성값을 서로 매칭하여 두 요소가 논리적으로 연결되어 있음을 보장한다.

---

#### Carousel (Swiper)

#### Carousel

**정의**
여러 개의 이미지나 카드 컴포넌트를 슬라이드 형태로 묶어, 한정된 공간 안에서 이전/다음으로 회전하며 탐색할 수 있도록 제공하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `dot` (화면당 1개 슬라이드 노출), `arrow` (화면당 다중 슬라이드 노출) |
| State | `enabled`, `hovered`, `focused`, `disabled` (Arrow 한정) |
| Auto-play | `play`, `pause` (Dot 타입 한정) |

**Usage (구성 및 타입 규칙)**
* ✅ **적용 대상:** `Button card`, `Image`, `Image card`, `Content visual card`, `Ribbon banner` 컴포넌트가 2개 이상 나열될 때 Carousel로 묶어서 적용할 수 있다.
* ✅ **권장 개수:** 사용자의 인지 부하를 줄이고 탐색의 어려움을 방지하기 위해 슬라이드 수는 **최대 5개 이하**로 제한하는 것을 권장한다.
* ✅ **타입 선택 기준:**
  * `Dot` 타입: 해상도에 관계없이 **한 화면에 1개의 항목**만 단독으로 표출될 때 사용한다. (항목이 2개 이상일 때부터 노출)
  * `Arrow` 타입: 해상도에 따라 **한 화면에 여러 개의 항목**이 나란히 표출될 때 사용한다. 이전/다음 화살표를 눌러 숨겨진 영역을 탐색한다.

**Usage (자동 재생 및 모션 규칙)**
* ✅ **자동 재생(Auto-play):** `Dot` 타입에 한하여 자동 재생 기능을 사용할 수 있다. 단, 사용자가 화면 제어권을 가질 수 있도록 **정지(Pause)/재생(Play) 토글 버튼을 반드시 함께 제공**해야 한다. `Arrow` 타입에서는 자동 재생을 사용하지 않는다.
* ✅ **모션 (Motion):**
  * `Compact` (모바일): Duration 500ms / Delay 2000ms / Easing decel
  * `Wide` (웹): Duration 1000ms / Delay 3000ms / Easing decel

**접근성 (Accessibility)**
* 자동 재생되는 콘텐츠는 인지 및 시각 장애 사용자에게 방해가 될 수 있으므로, 반드시 키보드로 조작 가능한 멈춤/재생(Play/Pause) 컨트롤을 제공해야 한다. (WCAG 2.2.2 Pause, Stop, Hide 기준 준수)
* 스크린 리더 사용자가 현재 어떤 슬라이드를 보고 있는지 알 수 있도록 Dot 인디케이터에 `aria-label` (예: "슬라이드 1/5") 및 선택된 항목에 `aria-current="true"` 속성을 제공한다.

---

#### Load More

*#### Load more

**정의**
정보의 양이 많아 한 번에 모든 데이터를 표출할 경우 발생하는 초기 로딩 지연을 방지하기 위해, 사용자의 요청이나 스크롤 위치에 따라 데이터를 부분적으로 나누어 이어서 불러오는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (수동 클릭형 버튼), `infinite-scroll` (자동 로드형 스피너) |
| State | `enabled`, `hovered`, `focused`, `pressed` (Basic 전용) / `loading` (Infinite scroll 전용) |

**Usage (타입 선택 및 Pagination 구분)**
* ✅ **Pagination vs Load more:** Load more는 목록의 개수가 비교적 적을 때 적합하다. 만약 더보기(Load more) 동작을 **10회 이상** 반복해야 할 정도로 데이터가 방대하다면, 사용자 탐색 피로도를 줄이기 위해 `Pagination` 컴포넌트 사용을 권장한다.
* ✅ **Infinite scroll 사용:** 텍스트 위주의 복잡한 데이터보다는 갤러리와 같은 이미지 콘텐츠나, 새롭게 불러오는 데이터의 단위 양이 비교적 적을 때 `Infinite scroll` 타입이 적합하다.

**Usage (동작 및 텍스트 규칙)**
* ✅ **진행 상태 표출 (Basic):** 버튼 텍스트에는 전체 데이터 중 현재 어디까지 불러왔는지를 명확히 알 수 있는 수치 정보(예: 현재 로드된 개수/전체 개수)를 필수로 포함하여 사용자의 예측 가능성을 높인다.
* ✅ **자동 숨김:** 마지막 데이터까지 로드가 모두 완료되어 더 이상 불러올 데이터가 없다면, 컴포넌트를 화면에서 즉시 숨김(Hide) 처리한다.
* ✅ **스크롤 유지:** 컴포넌트 작동 시, 화면이 상단으로 튕기는 현상 등 별도의 스크롤 작동 없이 기존 콘텐츠 바로 아래에 데이터를 자연스럽게 이어서 렌더링한다.
* ✅ **긴 텍스트 표출:** 다국어 환경 등에서 텍스트가 버튼의 최대 너비를 초과할 경우, 말줄임표(...)를 사용하지 않고 아래로 개행하여 표출한다. 이때 내부 아이콘은 컨테이너 중앙에 정렬된다.

**Usage (레이아웃 및 모션 규칙)**
* ✅ **배치:** 두 타입 모두 데이터를 로드하는 목록의 **가장 하단 중앙**에 배치한다.
* ✅ **Motion (Infinite scroll):** 데이터가 완전히 로드될 때까지 Spinner 컴포넌트의 회전 모션이 무한 반복(Loop)된다.

**접근성 (Accessibility)**
* `Basic` 타입은 반드시 `<button>` 태그를 사용하여 키보드(Tab, Enter, Space)로 접근 및 실행이 가능해야 한다.
* 데이터를 새로 불러왔을 때, 시각 장애 사용자가 화면 갱신을 인지할 수 있도록 `aria-live="polite"`를 적용한 메시지 영역을 통해 "N개의 항목이 추가되었습니다"와 같은 피드백을 시스템적으로 제공하는 것을 권장한다.
* `Infinite scroll`의 경우 키보드 사용자가 Footer 등 하단 영역에 도달하기 어렵게 만드는 '키보드 트랩' 현상을 유발할 수 있으므로, 접근성이 중요한 핵심 서비스에서는 가급적 수동 제어가 가능한 `Basic` 타입 사용을 우선적으로 고려한다.

---

#### Chart

#### Chart

**정의**
사용 목적에 따라 수치 데이터를 그래픽으로 시각화하여, 사용자가 정보를 직관적으로 이해하고 비교할 수 있도록 돕는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (현재/목표 데이터 및 총합), `donut` (데이터 점유율), `several` (2개 이상의 데이터 비교) |
| Orientation | `horizontal` (가로형), `vertical` (세로형) - *Several 타입 한정* |

**Usage (시각적 구분 및 표출 규칙)**
* ✅ **패턴 조합 (접근성):** 데이터를 시각적으로 구분할 때 색상에만 의존하지 않고, 모양이나 패턴 등을 조합하여 색각 이상 사용자도 명확히 인지할 수 있도록 구성한다.
* ✅ **Basic (목표 우선 표출):** 마일리지 달성 등 특정 목표 수치에 도달해야 하는 차트의 경우, 현재까지 누적된 수치보다 **앞으로 남은(달성해야 하는) 수치를 우선적으로 표출**하여 사용자의 목표 의식을 돕는다.
* ✅ **Several (비교 및 강조):**
  * 해상도와 데이터 성격에 따라 `Horizontal` 또는 `Vertical` 배치를 선택적으로 적용할 수 있다.
  * 여러 데이터 중 특정 값을 부각(Emphasize)하여 다른 값과의 대비를 명확히 할 수 있다.
* ✅ **Several (막대 구성 규칙):** 각 데이터의 막대(Bar)는 반드시 **일정한 너비와 간격**을 유지해야 하며, 데이터의 값이 시각적으로 서로 겹치지 않도록 표출해야 한다.

**Motion (인터랙션 및 모션 규칙)**
* ✅ **모션 트리거 시점:** 차트의 애니메이션 모션은 페이지 초기 진입 시 무조건 실행되는 것이 아니라, 사용자가 화면을 스크롤하여 **해당 차트 영역이 화면에 노출되었을 때 시작**하며 **최초 1회**만 동작한다.
* ✅ **Type별 모션 스펙:**
  * `Basic`: 막대 길이 확장(Scale)은 1000ms(Decel) 적용, 남은 데이터 수치 이동(Position)은 1000ms(Standard)를 적용한다.
  * `Several`: 막대 길이 확장(Scale)은 300ms(Slow)를 적용한다.

**접근성 (Accessibility)**
* 복잡한 그래픽을 시각적으로 인지할 수 없는 스크린 리더 사용자를 위해, 차트 주변이나 하단에 데이터 값을 표 형태(`Table`) 등으로 풀어쓴 **대체 콘텐츠를 반드시 함께 제공**해야 한다.

---

#### Itinerary

#### Itinerary

**정의**
사용자의 항공 여정 정보(출도착 도시, 시간, 터미널, 편명 등)를 예약, 조회, 비교 등 사용 목적과 화면 맥락에 맞춰 최적화된 형태로 제공하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (요약형), `timeline` (시간 흐름형), `ticket` (상세 정보형), `flight-time` (시간 비교형) |
| Journey | `one-way` (편도), `round-trip` (왕복) |
| Transfer | `true` (경유), `false` (직항) |
| Status | `normal` (정상), `delayed/canceled` (지연/결항 등 비정상 상태) |

**Design Principles (데이터 표기 원칙)**
* ✅ **날짜 증감 표기:** 비행 중 날짜가 변경되어 도착일이 늘어나는 경우(`+1d` 등)는 반드시 **초록색 텍스트**로 강조하여 표현한다.
* ✅ **공항 코드 위치:** ICN, JFK 등 3 letter 공항 코드는 정보 구조의 일관성을 위해 항상 **도시/공항명 뒤에 배치**한다.
* ✅ **경유지 (Transfer):** 경유지가 포함된 여정의 경우 점 아이콘(○, ●)을 사용하여 시각적으로 중간 지점을 명확히 분리하고 표출한다.
* ✅ **비정상 운항 (지연/결항):** 항공편 지연 및 결항 시 좌측 상단에 상태 Badge를 표출한다. **새롭게 변경된 날짜/시간 정보를 우선 표출**하고, 기존(정상) 운항 정보는 그 뒤에 **취소선**을 적용하여 배치한다.

**Usage (타입별 사용 가이드)**
* **Basic (요약형):** 출도착 도시/공항명을 가장 강조한 기본 형태. 결제 화면 등에서 여정 요약으로 사용하며, 필요 시 아이콘(편도/왕복)과 항공사 로고를 조합한다.
* **Timeline (타임라인형):** 시간의 흐름에 따른 여정(출발-경유-도착)을 수직 점선(Line)으로 연결하여 순서대로 표출한다. 부가서비스 화면 등에서는 도시/공항명을 더 부각하는 '강조형(Accent)'을 사용할 수 있다.
* **Ticket (티켓형):** 예약 상세 화면 등에서 사용하는 가장 구체적인 형태. 전체 소요 시간, 터미널, 편명, 기종, 탑승 클래스, 공동 운항(Codeshare) 정보 등을 모두 포함한다.
* **Flight time (비행 시간형):** 항공편 선택/비교 화면에서 출도착 시간과 소요 시간을 가로 구조로 배치하여 빠르게 비교할 수 있도록 제공하는 형태. (상세 보기 버튼 포함)

**Usage (레이아웃 및 반응형 규칙)**
* ✅ **긴 텍스트 처리:** 도시명 등 텍스트가 길어져 컨테이너의 최대 너비를 초과할 경우, 아래로 자연스럽게 자동 개행되며 박스 영역의 전체 높이가 늘어난다.
* ✅ **반응형 클릭/포커스 영역 (`Flight time` 기준):**
  * `Compact (모바일)`: 화면이 좁으므로 사용자 편의를 위해 Itinerary **영역 전체를 탭(Click)** 할 수 있도록 넓게 적용한다.
  * `Wide (웹)`: 마우스 조작 환경을 고려하여 우측의 **'상세 보기' 버튼에만 포커스 링(Focus-ring) 및 클릭 영역을 제한**하여 적용한다.

**접근성 (Accessibility)**
* 스크린 리더 사용자가 출도착 여정을 혼동하지 않도록 화살표(→) 아이콘이나 시각적 구조를 `aria-label="에서"`, `aria-label="으로 출발"` 등 논리적인 텍스트 흐름으로 변환하여 제공한다.
* 취소선이 적용된 지연/결항 이전의 스케줄은 시각적으로만 취소된 것이 아니라, 스크린 리더에서도 "취소된 일정"임을 명확히 읽을 수 있도록 `<s>` 또는 `<del>` 태그, 혹은 숨김 텍스트 처리를 병행한다.
---

#### FromTo

#### From to

**정의**
항공권 구매를 위한 Booking Tool UI 패턴 중 하나로, 사용자가 여정의 출발지(From)와 도착지(To)를 선택하고 서로 위치를 바꿀 수 있도록 제공하는 버튼 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (3자리 공항 코드 + 도시명), `short` (공항 코드 또는 도시명 단독) |
| Size | `sm`, `lg` |
| Layout | `vertical` (상하 배치), `horizontal` (좌우 배치) |
| State | `enabled`, `hovered`, `focused`, `disabled`, `error` |

**Usage (구성 및 아이콘 규칙)**
* ✅ **타입 선택:** 공간적 여유가 있을 때는 3자리 공항 코드와 도시명이 함께 표출되는 `Basic` 타입을 사용하고, 좁은 공간에서는 직관성을 위해 공항 코드 또는 도시명 중 하나만 표출하는 `Short` 타입을 사용한다.
* ✅ **스왑(바꾸기) 아이콘 적용 기준:**
  * **변경 가능 (왕복/편도):** 출도착지 스왑이 가능한 경우 `swap-horizontal` 아이콘을 사용하여 방향 전환 기능을 제공한다. (버튼의 Disabled 상태 등에 따라 아이콘 색상도 동기화되어 비활성화 처리됨)
  * **변경 불가 (다구간):** 다구간 여정처럼 출도착지를 서로 바꿀 수 없는 경우에는 스왑 기능이 제거되며, 단순 방향 안내를 위해 `flight`(비행기) 아이콘으로 대체하여 표출한다.

**Usage (상호작용 및 텍스트 규칙)**
* ✅ **초기 상태 제어:** 출발지와 도착지를 모두 선택하기 전(초기 상태)에는 중앙의 바꾸기(Swap) 버튼이 `Disabled` 상태로 유지된다. 출/도착지 중 한 곳 이상을 선택해야만 스왑 기능이 활성화(`Enabled`)된다.
* ✅ **긴 텍스트 개행 처리:** 도시명 등이 길어져 버튼의 최대 너비를 초과할 경우, 말줄임표(...)로 숨기지 않고 **하단으로 자연스럽게 개행(줄바꿈)**하여 전체 텍스트를 표출한다. (텍스트가 개행되어 영역이 높아져도 중앙의 아이콘은 컨테이너의 수직 중앙 정렬을 유지한다.)

**Usage (해상도 및 반응형 규칙)**
* ✅ **Compact (모바일):** 좁은 화면 너비를 고려하여 출발지와 도착지를 위아래로 배치하는 `Vertical` 레이아웃 사용을 권장한다.
* ✅ **Wide (웹):** 넓은 가로 공간을 효율적으로 활용하기 위해 출발지와 도착지를 좌우로 나란히 배치하는 `Horizontal` 레이아웃 사용을 권장한다.
---

#### Passenger

#### Passenger

**정의**
항공권 구매를 위한 Booking Tool UI 패턴 중 하나로, 사용자가 여정에 포함될 탑승객(성인, 소아, 유아)의 인원수 또는 탑승객 정보를 선택하고 확인할 수 있도록 제공하는 버튼 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Ticket Type | `book` (유상 항공권 - 인원수 표출), `book-with-miles` (마일리지 항공권 - 텍스트 표출) |
| State | `enabled`, `hovered`, `focused`, `read-only`, `disabled` |

**Usage (유상 항공권 - Book 타입 규칙)**
* ✅ **초기 상태:** 사용자의 선택 번거로움을 줄이기 위해, 초기 진입 시 기본값은 항상 **"성인 1명"**으로 설정하여 표출한다.
* ✅ **탑승객 표출:** 사용자가 인원수를 선택하면 성인, 소아, 유아의 각 인원수를 지정된 전용 아이콘(`adult`, `child`, `infant`)과 함께 숫자로 표출한다. (지정된 아이콘 외 임의의 아이콘 사용 불가)

**Usage (마일리지 무상 항공권 - Book with miles 타입 규칙)**
* ✅ **텍스트 표출:** 마일리지 예매 시에는 성인/소아/유아 구분 아이콘을 사용하지 않고 텍스트를 중심으로 표출한다.
* ✅ **본인 1명 탑승 시:** 본인 단독 탑승일 경우 탑승자의 **"이름(Name)"**을 직접 표출한다.
* ✅ **2명 이상 탑승 시:** 본인을 포함하거나 가족 등 여러 명이 함께 탑승하는 경우, 이름 대신 **"탑승객 숫자(N명)"**를 텍스트로 표출한다.
* ✅ **긴 이름 표출:** 탑승객의 이름이 버튼의 최대 너비를 초과할 경우, 말줄임표(...)를 사용하여 텍스트를 말끔하게 생략 처리한다.

**Usage (기타 및 레이아웃 규칙)**
* ✅ **레이블 생략:** 항공편 선택 화면 상단의 여정 변경 영역처럼 공간이 협소하거나 맥락상 분명한 위치에서는 상단 "탑승객" 레이블을 생략하여 간결하게 표출할 수 있다.
* ✅ **버튼 상태 동기화:** `Disabled`나 `Read-only` 상태가 될 경우, 텍스트뿐만 아니라 내부의 아이콘 색상도 해당 상태의 비활성화 색상으로 동일하게 변경되어 시각적 일관성을 유지해야 한다.

**접근성 (Accessibility)**
* 유상 항공권에서 제공하는 성인/소아/유아 아이콘은 단순한 장식이 아닌 핵심 정보를 담고 있으므로, 각 아이콘 요소에 `aria-hidden="true"`를 무작정 사용하지 않고 스크린 리더 사용자가 각 연령대별 인원수를 명확하게 읽을 수 있도록 숨김 텍스트(예: `<span class="sr-only">성인</span> 1, <span class="sr-only">소아</span> 0...`)를 논리적으로 제공한다.
---

#### Class

#### Class

**정의**
항공권 구매를 위한 Booking Tool UI 패턴 중 하나로, 사용자가 일반석, 프레스티지석, 일등석 등 좌석 등급을 선택하거나 마일리지 승급 옵션을 선택할 때 사용하는 버튼 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `class` (일반 좌석 등급 선택), `upgrade` (좌석 승급 선택) |
| Selection | `unselected` (선택 전), `selected` (선택 후) |
| State | `enabled`, `hovered`, `focused`, `read-only`, `disabled`, `error` |

**Usage (구성 및 텍스트 규칙)**
* ✅ **버튼 차별화:** Booking Tool 내의 핵심 기능 버튼이므로 다른 일반 버튼들과 시각적으로 명확히 구분되어야 한다.
* ✅ **선택 전/후 텍스트 표출:** * `Unselected` (선택 전): "좌석 등급"과 같은 Placeholder 성격의 기본 안내 문구를 표출한다.
  * `Selected` (선택 후): 사용자가 실제 선택한 "프레스티지석" 등의 데이터 값으로 텍스트가 변경되어 표출된다.
* ✅ **긴 텍스트 말줄임 처리:** "일반석 -> 프레스티지석 승급" 등 선택된 문구가 버튼의 지정된 최대 너비를 초과할 경우, 아래로 개행하지 않고 말줄임표(...)를 사용하여 한 줄로 처리한다.

**Usage (아이콘 및 상태 규칙)**
* ✅ **지정 아이콘 사용:** 목적에 따라 시스템에 지정된 전용 아이콘만 사용해야 한다. (임의의 아이콘 사용 불가)
  * 좌석 선택: `icon/seat`
  * 좌석 승급: `icon/seat-upgrade`
* ✅ **버튼 상태 동기화:** `Disabled`나 `Read-only` 상태가 적용될 경우, 버튼의 텍스트뿐만 아니라 좌측 아이콘의 색상도 비활성화 상태에 맞춰 동일하게 변경되어야 한다.
* ❌ **무상(보너스) 항공권 처리 주의:** 무상 항공권 등 사용자가 임의로 좌석을 선택하거나 변경할 수 없는 상황에서는 `Read-only` 상태로 표출하여 정보만 제공해야 하며, `Disabled` 상태로 표출하여 인지도를 떨어뜨려서는 안 된다.

**접근성 (Accessibility)**
* 좌석 선택 요소가 화면 내에서 버튼 역할을 하므로, 시맨틱 HTML인 `<button>` 요소로 구현한다. 
* 팝업이나 Bottom sheet 등 추가 옵션 선택 창을 띄우는 역할을 하므로 `aria-haspopup="true"` 또는 `aria-expanded="true/false"` 속성을 활용하여 스크린 리더 사용자에게 동작 방식을 안내한다.

---

### 3.9 미디어 (Media)

---

#### Image

#### Image

**정의**
사진이나 일러스트레이션 등의 그래픽 요소를 화면에 표현하여 텍스트의 이해를 돕고 시각적 완성도를 높이는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic` (단일 이미지 표출), `carousel` (다중 이미지 슬라이드 표출) |
| Feature | `expandable` (확대 기능 제공 여부) |
| State | `enabled`, `hovered`, `focused` |

**Usage (구성 및 인터랙션 규칙)**
* ✅ **링크 사용 금지:** 이미지 자체(이미지 요소 단독)에는 직접 Link 속성을 걸거나 삽입하여 클릭/터치 시 외부나 다른 페이지로 이동하도록 만들 수 없다. 링크 이동이 필요할 경우 텍스트, 버튼, 카드 등 명확한 액션 요소를 조합하여 구성해야 한다.
* ✅ **확대 기능:** 사용자가 이미지의 디테일을 확인해야 하는 경우 선택적으로 **확대 기능**을 제공할 수 있다. 기능이 켜진 경우, 이미지 전체 영역이 클릭/터치 가능하며 누르면 이미지가 화면에 맞게 확대(Full-screen 또는 모달 형태)되어 표출된다.
* ✅ **모서리 곡률 (Radius):** 이미지 컨테이너의 모서리를 둥글게 처리해야 할 경우 지정된 토큰 값인 **16px**을 일괄 적용하여 시각적 통일성을 유지한다.

**Usage (다중 이미지 및 Carousel 규칙)**
* ✅ **Carousel 연계:** 하나의 영역에서 2개 이상의 이미지를 보여주어야 할 경우, 화면 공간을 절약하기 위해 반드시 `Carousel` 컴포넌트로 묶어 슬라이드 형태로 제공한다.
* ✅ **Carousel 인디케이터(Indicator) 분기:**
  * `Dot`: 해상도에 맞춰 이미지의 너비가 가변되어 **한 화면(뷰포트)에 이미지가 1개씩만 꽉 차게 노출**될 경우 사용한다.
  * `Arrow`: 이미지에 고정 너비를 적용하여 **해상도에 따라 한 화면에 보여지는 이미지의 개수가 여러 개로 달라지는 경우** 사용한다.

**Usage (해상도 및 반응형 배치 규칙)**
* ✅ **비율 및 너비:**
  * 해상도와 화면 레이아웃에 맞춰, 이미지의 높이를 원본 비율대로 가변(가로가 줄면 세로도 함께 줄어듦)하게 두거나 특정 높이로 고정하여 크롭(Crop)할 수 있다.
  * `Compact` (모바일): 화면의 좌우 너비에 맞춰 **Full Width(최대 1059px 내외)**로 꽉 차게 표출한다.
  * `Wide` (웹): 그리드(Grid) 시스템이나 콘텐츠 영역에 맞춰 지정된 **최대 너비(Max-width)** 값을 초과하여 이미지가 깨지거나 과도하게 늘어나지 않도록 방어한다.

---

#### Video

**정의**
동영상 콘텐츠를 재생하는 미디어 컴포넌트.

**목적**
- 기내 엔터테인먼트 소개, 목적지 홍보 영상 등을 제공한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `inline`, `fullscreen`, `background` |
| Autoplay | `true` (음소거 필수), `false` |

**Usage**
- ✅ 자동 재생은 음소거 상태로만 허용한다
- ✅ 자막(CC) 옵션을 제공한다

**접근성**
- `<video>` + `<track kind="captions">` 제공
- `prefers-reduced-motion` 미디어 쿼리 적용

---

## 4. Design Rules (설계 규칙)

### 4.1 토큰 사용 규칙
- Primitive 토큰 (`color/brand/*`, `color/neutral/*`)을 컴포넌트에 직접 사용하지 않는다.
- 반드시 Semantic 토큰 (`color/text/*`, `color/fill/*`, `color/border/*`)을 사용한다.
- 임의의 hex 값을 컴포넌트에 직접 사용하지 않는다.

### 4.2 컴포넌트 조합 규칙
- Button Solid Primary: 한 화면에 1개만 허용
- FAB: 한 화면에 1개만 허용
- Dialog + Bottom Sheet: 동시 표시 불가
- Snack Bar: 동시에 1개만 표시
- Nudge: 동시에 1개만 표시
- Tooltip + Nudge: 동일 요소에 동시 적용 불가

### 4.3 접근성 필수 규칙
- 색상만으로 정보를 전달하지 않는다 (색상 + 아이콘 또는 텍스트 병행)
- 텍스트-배경 명암비: WCAG AA 기준 4.5:1 이상
- 모든 인터랙티브 요소는 키보드로 조작 가능해야 한다
- 최소 터치 영역: 44×44px
- 이미지에는 반드시 alt 텍스트를 제공한다

### 4.4 다국어 지원 규칙
- 기본 폰트: Hanjin Group Sans (한국어)
- 일본어 노출 시: Yu Gothic UI
- 중국어 간체: Microsoft YaHei / 번체: Microsoft JhengHei
- 텍스트 길이 변화에 대응하는 유연한 레이아웃을 사용한다

### 4.5 반응형 규칙
- 모바일 (375px~): compact 타이포그래피, 4컬럼 그리드
- 태블릿 (768px~): 8컬럼 그리드
- 웹 (980px~): 16컬럼 그리드, wide 타이포그래피
- Dialog → 모바일에서는 Bottom Sheet로 대체 고려
- Pagination → 모바일에서는 Load More 또는 Infinite Scroll 고려

---

## 5. Brand Assets

> **Claude 사용 지침**: 아래 SVG 코드를 직접 참조하여 로고와 심볼을 정확하게 재현한다. 색상 변경, 변형, 효과 추가는 금지한다.

---

### 5.1 Primary Logo

#### Dark Blue (기본, 밝은 배경용)
- **사용 배경**: 흰색, 밝은 회색 등 밝은 배경
- **색상**: `#051766` (color/brand/darkblue/100)
- **ViewBox**: 0 0 3090.59 614.58

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 3090.59 614.58"><defs><style>.cls-1{fill:#051766;}</style></defs><path class="cls-1" d="m113.73,416.78l-1.78,1.23c36.34,67.01,105.14,112.28,183.63,112.28,116.74,0,211.29-99.9,211.29-223,0-33.9-14.05-62.44-30.66-84.07-22.08-28.77-53.52-42.59-84.85-42.82-25.87-.22-52.63,8.47-71.47,25.53-21.52,19.51-26.31,44.6-31.89,85.3-6.13,44.6-42.04,75.37-88.2,75.37-59.76,0-96.78-36.79-94.33-93.1.22-3.9.56-7.8,1.23-11.6,11.26-66.45,82.73-135.03,190.22-134.8,72.14,0,126.33,16.17,180.52,70.69l1.78-1.23c-36.35-67-105.03-112.27-183.64-112.27-116.63,0-211.29,99.9-211.29,223,0,33.9,14.05,62.44,30.66,84.07,21.97,28.77,53.52,42.48,84.85,42.82,25.87.33,52.63-8.47,71.47-25.53,21.52-19.51,26.31-44.6,31.89-85.3,6.13-44.6,42.15-75.37,88.2-75.37,59.88,0,96.89,36.79,94.44,93.1-.22,3.9-.56,7.8-1.23,11.6-11.48,66.45-82.62,135.03-190.33,134.8-72.14-.01-126.33-16.18-180.51-70.7Z"/><path class="cls-1" d="m687.3,180.86h50.29v252.87h-50.29v-252.87Zm217.1,236.39c6.61,6.97,12.63,12.46,18.06,16.47h-34.35c-12.04,0-22.55-2.12-31.52-6.37-8.98-4.25-17.71-11.57-26.21-21.96l-85.35-106.6,110.14-117.93h56.66l-110.5,115.81,76.85,90.66c10.87,12.99,19.6,22.96,26.22,29.92Z"/><path class="cls-1" d="m986.92,421.5c-20.54-10.98-36.66-26.38-48.34-46.22-11.69-19.83-17.53-42.5-17.53-68s5.84-48.16,17.53-68c11.69-19.83,27.8-35.24,48.34-46.22,20.54-10.98,43.56-16.47,69.06-16.47s48.16,5.49,68.71,16.47c20.54,10.98,36.66,26.45,48.34,46.39,11.69,19.95,17.53,42.56,17.53,67.82s-5.84,47.87-17.53,67.82c-11.69,19.95-27.8,35.42-48.34,46.39-20.54,10.98-43.44,16.47-68.71,16.47-25.5.02-48.52-5.47-69.06-16.45Zm111.91-33.82c12.51-7.08,22.31-17.47,29.39-31.17,7.08-13.69,10.62-30.1,10.62-49.23s-3.54-35.53-10.62-49.23c-7.08-13.69-16.88-24.08-29.39-31.17-12.52-7.08-26.8-10.62-42.85-10.62s-30.69,3.54-43.21,10.62c-12.52,7.08-22.31,17.48-29.4,31.17-7.08,13.69-10.62,30.1-10.62,49.23s3.54,35.54,10.62,49.23c7.08,13.7,16.88,24.08,29.4,31.17,12.51,7.08,26.92,10.62,43.21,10.62,16.05.01,30.33-3.53,42.85-10.62Z"/></svg>
```

#### White (어두운 배경용)
- **사용 배경**: `#051766` (darkblue), 어두운 이미지 위
- **색상**: `#FFFFFF` (color/neutral/10)
- **ViewBox**: 0 0 3090.6 614.6

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 3090.6 614.6"><style>.st0{fill:#FFFFFF;}</style><g><g><g><path class="st0" d="M113.7,416.8l-1.8,1.2c36.3,67,105.1,112.3,183.6,112.3c116.7,0,211.3-99.9,211.3-223c0-33.9-14-62.4-30.7-84.1c-22.1-28.8-53.5-42.6-84.9-42.8c-25.9-0.2-52.6,8.5-71.5,25.5c-21.5,19.5-26.3,44.6-31.9,85.3c-6.1,44.6-42,75.4-88.2,75.4c-59.8,0-96.8-36.8-94.3-93.1c0.2-3.9,0.6-7.8,1.2-11.6c11.3-66.5,82.7-135,190.2-134.8c72.1,0,126.3,16.2,180.5,70.7l1.8-1.2c-36.3-67-105-112.3-183.6-112.3c-116.6,0-211.3,99.9-211.3,223c0,33.9,14,62.4,30.7,84.1c22,28.8,53.5,42.5,84.9,42.8c25.9,0.3,52.6-8.5,71.5-25.5c21.5-19.5,26.3-44.6,31.9-85.3c6.1-44.6,42.1-75.4,88.2-75.4c59.9,0,96.9,36.8,94.4,93.1c-0.2,3.9-0.6,7.8-1.2,11.6c-11.5,66.5-82.6,135-190.3,134.8C222.1,487.5,167.9,471.3,113.7,416.8z"/></g></g><g><path class="st0" d="M687.3,180.9h50.3v252.9h-50.3V180.9z M904.4,417.3c6.6,7,12.6,12.5,18.1,16.5h-34.4c-12,0-22.5-2.1-31.5-6.4c-9-4.2-17.7-11.6-26.2-22L745,298.8l110.1-117.9h56.7L801.3,296.7l76.9,90.7C889.1,400.3,897.8,410.3,904.4,417.3z"/><path class="st0" d="M986.9,421.5c-20.5-11-36.7-26.4-48.3-46.2c-11.7-19.8-17.5-42.5-17.5-68s5.8-48.2,17.5-68c11.7-19.8,27.8-35.2,48.3-46.2c20.5-11,43.6-16.5,69.1-16.5c25.3,0,48.2,5.5,68.7,16.5c20.5,11,36.7,26.4,48.3,46.4c11.7,20,17.5,42.6,17.5,67.8c0,25.3-5.8,47.9-17.5,67.8c-11.7,20-27.8,35.4-48.3,46.4c-20.5,11-43.4,16.5-68.7,16.5C1030.5,438,1007.5,432.5,986.9,421.5z"/></g></g></svg>
```

---

### 5.2 Taeguk Symbol (태극 심볼)

#### Dark Blue
- **사용 배경**: 흰색, 밝은 배경
- **색상**: `#051766` (color/brand/darkblue/100)
- **ViewBox**: 0 0 1167.82 1213.33

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1167.82 1213.33"><defs><style>.cls-1{fill:#051766;}</style></defs><path class="cls-1" d="m230.54,819.43l-3.46,2.39c70.62,130.21,204.31,218.18,356.83,218.18,226.85,0,410.58-194.13,410.58-433.33,0-65.87-27.3-121.33-59.58-163.36-42.91-55.91-104-82.76-164.88-83.21-50.27-.43-102.27,16.46-138.88,49.61-41.82,37.91-51.13,86.67-61.97,165.75-11.91,86.67-81.69,146.46-171.39,146.46-116.13,0-188.06-71.49-183.3-180.91.43-7.58,1.09-15.16,2.39-22.54,21.88-129.13,160.76-262.39,369.64-261.94,140.18,0,245.48,31.42,350.79,137.36l3.46-2.39c-70.64-130.19-204.09-218.16-356.85-218.16-226.64,0-410.58,194.13-410.58,433.33,0,65.87,27.3,121.33,59.58,163.36,42.69,55.91,104,82.55,164.88,83.21,50.27.64,102.27-16.46,138.88-49.61,41.82-37.91,51.13-86.67,61.97-165.75,11.91-86.67,81.91-146.46,171.39-146.46,116.36,0,188.28,71.49,183.52,180.91-.43,7.58-1.09,15.16-2.39,22.54-22.31,129.13-160.55,262.39-369.85,261.94-140.18-.02-245.48-31.44-350.77-137.38Z"/></svg>
```

#### White
- **사용 배경**: `#051766` (darkblue), 어두운 이미지 위
- **색상**: `#FFFFFF` (color/neutral/10)

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1167.82 1213.33"><defs><style>.cls-1{fill:#fff;}</style></defs><path class="cls-1" d="m230.54,819.43l-3.46,2.39c70.62,130.21,204.31,218.18,356.83,218.18,226.85,0,410.58-194.13,410.58-433.33,0-65.87-27.3-121.33-59.58-163.36-42.91-55.91-104-82.76-164.88-83.21-50.27-.43-102.27,16.46-138.88,49.61-41.82,37.91-51.13,86.67-61.97,165.75-11.91,86.67-81.69,146.46-171.39,146.46-116.13,0-188.06-71.49-183.3-180.91.43-7.58,1.09-15.16,2.39-22.54,21.88-129.13,160.76-262.39,369.64-261.94,140.18,0,245.48,31.42,350.79,137.36l3.46-2.39c-70.64-130.19-204.09-218.16-356.85-218.16-226.64,0-410.58,194.13-410.58,433.33,0,65.87,27.3,121.33,59.58,163.36,42.69,55.91,104,82.55,164.88,83.21,50.27.64,102.27-16.46,138.88-49.61,41.82-37.91,51.13-86.67,61.97-165.75,11.91-86.67,81.91-146.46,171.39-146.46,116.36,0,188.28,71.49,183.52,180.91-.43,7.58-1.09,15.16-2.39,22.54-22.31,129.13-160.55,262.39-369.85,261.94-140.18-.02-245.48-31.44-350.77-137.38Z"/></svg>
```

---

### 5.3 로고 사용 규칙

| 규칙 | 내용 |
|------|------|
| 최소 크기 | 디지털 80px 이상, 인쇄 20mm 이상 |
| 여백 (클리어스페이스) | 로고 높이의 50% 이상 사방 확보 |
| 배경 | 흰색/밝은 배경 → Dark Blue 버전, 어두운 배경 → White 버전 |
| 금지 | 색상 변경, 비율 변형, 회전, 그림자/효과 추가, 부분 사용 |
| 단독 사용 | 태극 심볼은 공간이 충분하지 않을 때만 단독 사용 |

---

### 5.4 Icon System

#### 개요
| 항목 | 내용 |
|------|------|
| 총 아이콘 수 | 약 600개 |
| 포맷 | SVG |
| 크기 체계 | 16px / 20px / 24px / 32px |
| 기본 색상 | `color/icon/primary` (#051766) |
| 파일 위치 | `assets/icons/{category}/{name}.svg` |

#### 카테고리 구조
```
assets/icons/
├── 기호-도형/       # 화살표, 체크, 별, 도형 등 기본 UI 기호
├── 여행-예약/       # 항공기, 좌석, 여권, 수하물, 일정 등 항공 도메인
├── 동식물-행위/     # 사람, 동물, 식물, 행동 관련 아이콘
├── 장소-의식주/     # 건물, 음식, 의류, 숙소, 지역 관련
├── 사물/           # 가전, 가구, 도구, 물건 등
└── etc/            # 분류 외 기타 아이콘
```

#### 색상 사용 규칙
| 상황 | 적용 토큰 | 값 |
|------|----------|-----|
| 기본 아이콘 | `color/icon/primary` | `#051766` |
| 보조 아이콘 | `color/icon/secondary` | `#5E5E5E` |
| 비활성 | `color/icon/disabled` | `#A4A4A4` |
| 어두운 배경 위 | `color/icon/inverse` | `#FFFFFF` |
| 성공 상태 | `color/icon/positive` | `#28794E` |
| 경고 상태 | `color/icon/warning` | `#BD5814` |
| 오류 상태 | `color/icon/negative` | `#DA291C` |

#### 크기별 사용 가이드
| 크기 | 사용 상황 |
|------|----------|
| 16px | 캡션, Badge 내부, 인라인 텍스트 옆 |
| 20px | 버튼 내부, 인풋 필드 Adornment |
| 24px | Navigation Bar, Top Bar, List 아이템 |
| 32px | Empty State 일러스트, 대형 강조 표시 |

#### 접근성 규칙
- 장식적 아이콘: `aria-hidden="true"` 필수
- 의미 있는 아이콘 (텍스트 없이 단독 사용): `aria-label` 또는 `<title>` 제공
- 색상만으로 의미 전달 금지 → 텍스트 또는 다른 시각적 단서 병행

#### 카테고리별 주요 아이콘 예시

**기호/도형**
체크마크, X (닫기), 화살표 (상/하/좌/우), 검색, 필터, 더보기, 공유, 즐겨찾기(하트/별), 홈, 설정, 알림, 정보(i), 경고(!), 플러스/마이너스, 달력, 시계

**여행/예약**
항공기, 좌석, 여권, 수하물(기내/위탁), 탑승권, 공항, 목적지 핀, 마일리지, SKYPASS, 기내식, 라운지, 환승, 좌석 등급(이코노미/비즈니스/퍼스트)

**동식물/행위**
탑승객(성인/소아/유아), 휠체어, 반려동물, 걷기, 달리기, 먹기

**장소/의식주**
호텔, 레스토랑, 쇼핑, 지도, 건물, 관광지

**사물**
스마트폰, 카메라, 카드, 지갑, 가방, 우산
