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
사용자가 텍스트를 직접 입력하는 단일 라인 입력 필드.

**목적**
- 이름, 이메일, 항공권 번호 등 짧은 텍스트 데이터를 수집한다.

**Variants**
| Property | Values |
|----------|--------|
| State | `default`, `focused`, `filled`, `error`, `disabled`, `readonly` |
| Type | `text`, `password`, `number`, `search` |
| Size | `lg`, `md` |
| Adornment | `none`, `leading-icon`, `trailing-icon`, `both` |

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

**Usage**
- ✅ 레이블은 항상 표시한다 (placeholder만으로 대체 불가)
- ✅ 에러 메시지는 필드 하단에 즉시 표시한다
- ❌ 여러 줄 입력은 Textarea를 사용한다

**접근성**
- `<label>`과 `for`/`id`로 연결 필수
- 에러 시: `aria-invalid="true"`, `aria-describedby`로 에러 메시지 연결

---

#### Textarea

**정의**
여러 줄의 텍스트를 입력할 수 있는 멀티라인 입력 필드.

**목적**
- 특별 요청사항, 메모, 피드백 등 긴 텍스트 입력에 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| State | `default`, `focused`, `filled`, `error`, `disabled`, `readonly` |

**Usage**
- ✅ 최대 글자 수 표시 (예: "0/300")
- ✅ 최소 높이: 120px
- ❌ 단일 라인 입력에는 Input Box를 사용한다

---

#### Checkbox

**정의**
여러 옵션 중 하나 이상을 선택할 수 있는 입력 컴포넌트.

**목적**
- 약관 동의, 필터 다중 선택, 옵션 추가 선택에 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| State | `unchecked`, `checked`, `indeterminate`, `disabled` |
| Size | `lg` (24px), `md` (20px) |

**토큰 매핑**
| State | Box Background | Box Border | Check Icon |
|-------|--------------|-----------|-----------|
| Unchecked | `color/fill/surface/primary` | `color/border/tertiary` | - |
| Checked | `color/fill/interaction/primary` | `color/border/primary` | `color/icon/inverse` |
| Indeterminate | `color/fill/interaction/primary` | `color/border/primary` | `color/icon/inverse` |
| Disabled | `color/fill/interaction/disabled` | `color/border/disabled` | `color/icon/disabled` |

- `radius/checkbox` (2px) 적용

**Usage**
- ✅ 독립적으로 켜고 끌 수 있는 옵션에 사용한다
- ❌ 하나만 선택해야 하는 경우 Radio group을 사용한다

**접근성**
- `type="checkbox"`, `<label>` 연결
- 그룹: `<fieldset>` + `<legend>`로 묶기

---

#### Radio Group

**정의**
여러 옵션 중 반드시 하나만 선택하는 입력 컴포넌트.

**목적**
- 좌석 등급, 탑승객 유형, 결제 수단 등 상호 배타적인 선택에 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| State | `unselected`, `selected`, `disabled` |
| Layout | `vertical`, `horizontal` |

**토큰 매핑**
| State | Outer Ring | Inner Dot | Label |
|-------|-----------|----------|-------|
| Unselected | `color/border/tertiary` | - | `color/text/body` |
| Selected | `color/border/primary` | `color/fill/interaction/primary` | `color/text/body` |
| Disabled | `color/border/disabled` | `color/fill/interaction/disabled` | `color/text/disabled` |

**Usage**
- ✅ 옵션이 2~5개일 때 적합하다
- ❌ 6개 이상은 Select Box를 사용한다

---

#### Select Box

**정의**
미리 정의된 목록에서 하나를 선택하는 드롭다운 컴포넌트.

**목적**
- 국가, 공항, 언어 등 선택지가 많을 때 공간 효율적으로 옵션을 제공한다.

**Variants**
| Property | Values |
|----------|--------|
| State | `default`, `focused`, `filled`, `error`, `disabled` |

**Usage**
- ✅ 옵션이 5개 이상일 때 사용한다
- ❌ 날짜/시간 선택은 Date Picker를 사용한다

**접근성**
- `role="listbox"`, `role="option"` 사용
- `aria-expanded`로 열림/닫힘 상태 전달

---

#### Switch

**정의**
설정이나 기능을 즉시 켜고 끄는 토글 컴포넌트.

**목적**
- 알림 설정, 마케팅 수신 동의 등 즉각 반영되는 on/off 전환에 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| State | `off`, `on`, `disabled-off`, `disabled-on` |

**토큰 매핑**
| State | Track Background | Thumb |
|-------|----------------|-------|
| Off | `color/fill/interaction/enabled-switch-basic` (#5E5E5E) | `color/fill/surface/primary` |
| On | `color/fill/interaction/primary` (#051766) | `color/fill/surface/primary` |
| Disabled | `color/fill/interaction/disabled` | `color/fill/surface/primary` |

**Usage**
- ✅ 변경 즉시 반영되는 설정에 사용한다
- ❌ 폼 제출 후 반영되는 항목은 Checkbox를 사용한다

**접근성**
- `role="switch"`, `aria-checked="true/false"`

---

#### Autocomplete

**정의**
텍스트 입력 시 관련 추천 항목을 실시간으로 제안하는 입력 컴포넌트.

**목적**
- 공항 코드, 도시명, 항공편 번호 등 방대한 목록에서 빠르게 검색하고 선택할 수 있도록 돕는다.

**Variants**
| Property | Values |
|----------|--------|
| State | `default`, `focused`, `typing`, `dropdown-open`, `selected`, `error`, `disabled` |
| Type | `airport`, `city`, `flight`, `general` |

**토큰 매핑**
| 영역 | 토큰 |
|------|------|
| Dropdown background | `color/fill/surface/primary` |
| Hover/Selected item | `color/fill/interaction/selected-item` |

**Usage**
- ✅ 2글자 이상 입력 시 추천 목록을 표시한다
- ✅ 공항 선택 시 IATA 코드와 도시명을 함께 표시한다

**접근성**
- `role="combobox"`, `aria-autocomplete="list"`

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

**정의**
날짜를 직접 텍스트로 입력하는 컴포넌트.

**목적**
- 생년월일, 여권 만료일 등 사용자가 날짜를 정확히 알고 있는 경우 빠른 입력을 지원한다.

**Variants**
| Property | Values |
|----------|--------|
| Format | `YYYY-MM-DD`, `DD/MM/YYYY`, `MM/YYYY` |
| State | `default`, `focused`, `filled`, `error`, `disabled` |

---

#### Spinbutton

**정의**
숫자 값을 증가/감소 버튼으로 조절하는 컴포넌트.

**목적**
- 탑승객 수, 수하물 개수 등 범위가 정해진 숫자 입력에 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| State | `default`, `min-reached`, `max-reached`, `disabled` |

**Usage**
- ✅ 최솟값/최댓값 도달 시 해당 방향 버튼을 비활성화한다

**접근성**
- `role="spinbutton"`, `aria-valuenow`, `aria-valuemin`, `aria-valuemax`

---

#### File Upload

**정의**
로컬 파일을 선택하여 업로드하는 입력 컴포넌트.

**목적**
- 여권 사진, 증명서, 영수증 등 파일 첨부가 필요한 경우 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `button`, `drag-and-drop` |
| State | `default`, `hover`, `uploading`, `success`, `error` |

**토큰 매핑**
| State | Background | Border |
|-------|-----------|--------|
| Default | `color/fill/surface/secondary` | `color/border/tertiary` (dashed) |
| Hover | `color/fill/surface/highlight` | `color/border/primary` (dashed) |
| Error | `color/fill/surface/negative` | `color/border/negative` |

---

#### Consent

**정의**
약관 동의 등 사용자의 명시적 동의를 받는 컴포넌트.

**목적**
- 법적 동의 절차를 UI적으로 명확하게 구현한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `all-agree`, `single`, `required`, `optional` |
| State | `unchecked`, `checked` |

**Usage**
- ✅ 필수/선택 항목을 명확히 구분하여 표시한다
- ✅ "전체 동의"는 개별 항목 체크와 연동한다

---

### 3.3 탐색 (Navigation)

---

#### Tab

**정의**
같은 레벨의 콘텐츠를 그룹화하여 전환하는 탐색 컴포넌트.

**목적**
- 항공권 검색(편도/왕복/다구간), 예약 내역(예정/완료/취소) 등 관련 콘텐츠를 공간 효율적으로 구성한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `underline`, `filled`, `chip` |
| Size | `lg`, `md`, `sm` |
| Scroll | `fixed`, `scrollable` |
| State | `default`, `selected`, `disabled` |

**토큰 매핑**
| Variant | Selected BG | Selected Text | Indicator |
|---------|------------|--------------|-----------|
| Underline | transparent | `color/text/body` | `color/border/divider-top` (#051766) |
| Filled | `color/fill/interaction/primary` | `color/text/inverse` | none |
| Chip | `color/fill/interaction/primary` | `color/text/inverse` | none |

**Usage**
- ✅ 탭은 2~7개를 권장한다
- ❌ 순서가 중요한 단계별 흐름에는 Progress Indicator를 사용한다

**접근성**
- `role="tablist"`, `role="tab"`, `role="tabpanel"` 적용
- 선택된 탭: `aria-selected="true"`

---

#### Navigation Bar

**정의**
앱의 주요 섹션 간 이동을 위한 하단 고정 탐색 바.

**목적**
- 홈, 예약, 마이페이지 등 앱의 핵심 기능에 항상 접근할 수 있도록 한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `icon-only`, `icon+label` |
| Item count | 3, 4, 5 |

**토큰 매핑**
| 상태 | Icon | Label |
|------|------|-------|
| Default | `color/icon/secondary` | `color/text/body-secondary` |
| Selected | `color/icon/primary` | `color/text/body` |

**접근성**
- `<nav>` + `aria-label="주요 탐색"`
- 현재 탭: `aria-current="page"`

---

#### Top Bar

**정의**
화면 최상단에 고정되는 헤더 바.

**목적**
- 현재 화면의 제목을 표시하고 주요 탐색 액션을 제공한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `default`, `transparent`, `search` |
| Left | `back`, `close`, `logo`, `none` |
| Right | `icon-buttons`, `text-button`, `none` |

**토큰 매핑**
| Type | Background | Title | Icon |
|------|-----------|-------|------|
| Default | `color/fill/surface/primary` | `color/text/title` | `color/icon/primary` |
| Transparent | transparent | `color/text/inverse` | `color/icon/inverse` |

---

#### LNB (Left Navigation Bar)

**정의**
좌측에 위치하는 계층형 탐색 메뉴.

**목적**
- 웹 또는 태블릿 환경에서 다수의 메뉴를 계층 구조로 탐색할 수 있도록 한다.

**Variants**
| Property | Values |
|----------|--------|
| Mode | `expanded`, `collapsed`, `overlay` |
| Depth | `1depth`, `2depth` |

**토큰 매핑**
| 상태 | Background | Text |
|------|-----------|------|
| Default | `color/fill/canvas/secondary` | `color/text/body` |
| Selected | `color/fill/interaction/selected-item` | `color/text/body` |
| Hover | `color/fill/surface/tertiary` | `color/text/body` |

---

#### Menubar

**정의**
웹 화면 상단에 위치하는 가로 탐색 메뉴 바.

**목적**
- 웹 서비스의 주요 카테고리(항공, 여행, SKYPASS 등)에 대한 글로벌 탐색을 제공한다.

**토큰 매핑**
| 상태 | Background | Text |
|------|-----------|------|
| Default | `color/fill/surface/primary` | `color/text/body` |
| Hover | `color/fill/interaction/enabled-menubar` | `color/text/body` |
| Active | `color/fill/surface/primary` | `color/text/title` |

---

#### Pagination

**정의**
대량의 콘텐츠를 페이지 단위로 나누어 탐색하는 컴포넌트.

**목적**
- 검색 결과, 게시판 목록 등 긴 콘텐츠를 페이지 단위로 분할한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `numbered`, `simple` |

**토큰 매핑**
| State | Background | Text |
|-------|-----------|------|
| Default | transparent | `color/text/body` |
| Selected | `color/fill/interaction/primary` | `color/text/inverse` |
| Disabled | transparent | `color/text/disabled` |

---

#### Sticky

**정의**
스크롤 시 특정 위치에서 화면에 고정되는 영역 컴포넌트.

**목적**
- 필터 바, 하단 CTA 등 스크롤 중에도 항상 노출이 필요한 콘텐츠에 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| Position | `top`, `bottom` |

---

### 3.4 피드백 (Feedback)

---

#### Badge

**정의**
상태, 카테고리, 수량을 짧게 표시하는 레이블 컴포넌트.

**목적**
- 예약 상태(완료/취소/대기), 알림 수, 등급 태그 등을 한눈에 파악할 수 있도록 한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `status`, `count`, `label`, `dot` |
| Size | `lg`, `md`, `sm` |
| Color | `primary`, `positive`, `warning`, `negative`, `neutral` |

**토큰 매핑**
| Color | Background | Text |
|-------|-----------|------|
| Primary | `color/fill/interaction/primary` | `color/text/inverse` |
| Positive | `color/fill/surface/positive-accent` | `color/text/inverse` |
| Warning | `color/fill/surface/warning` | `color/text/warning` |
| Negative | `color/fill/surface/accent` | `color/text/inverse` |
| Neutral | `color/fill/surface/tertiary` | `color/text/body-secondary` |

**Usage**
- ✅ 텍스트는 최대 10자 이내
- ✅ Count Badge는 최대 "99+"로 표시
- ❌ 색상만으로 의미를 전달하지 않는다

---

#### Chip

**정의**
필터, 태그, 선택 항목을 표현하는 인터랙티브 요소.

**목적**
- 항공편 필터(직항/경유), 부가서비스 선택 등에 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `filter`, `input`, `suggestion` |
| State | `default`, `selected`, `disabled` |

**토큰 매핑**
| State | Background | Border | Text |
|-------|-----------|--------|------|
| Default | `color/fill/interaction/enabled-chip` | `color/border/tertiary` | `color/text/body` |
| Selected | `color/fill/interaction/selected-item` | `color/border/primary` | `color/text/body` |
| Disabled | `color/fill/interaction/disabled-on` | `color/border/disabled` | `color/text/disabled` |

- `radius/md` (12px) 적용

---

#### Notice Bar

**정의**
페이지 상단에 고정되어 중요 공지를 지속적으로 표시하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `info`, `positive`, `warning`, `negative` |

**토큰 매핑**
| Type | Background | Text | Icon |
|------|-----------|------|------|
| Info | `color/fill/surface/highlight` | `color/text/body` | `color/icon/primary` |
| Positive | `color/fill/surface/positive` | `color/text/positive` | `color/icon/positive` |
| Warning | `color/fill/surface/warning` | `color/text/warning` | `color/icon/warning` |
| Negative | `color/fill/surface/negative` | `color/text/negative` | `color/icon/negative` |

---

#### Snack Bar

**정의**
사용자 액션의 결과를 화면 하단에 일시적으로 표시하는 피드백 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `default`, `positive`, `negative`, `action` |
| Duration | `short` (3초), `long` (5초) |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Background | `color/fill/surface/snackbar` (#252525CC) |
| Text | `color/text/inverse` |
| Action text | `color/brand/lightblue/100` (#57BBEB) |

---

#### Tooltip

**정의**
UI 요소에 호버 또는 포커스할 때 보조 설명을 표시하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Position | `top`, `bottom`, `left`, `right` |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Background | `color/fill/surface/inverse` (#051766) |
| Text | `color/text/inverse` (#FFFFFF) |
| Radius | `radius/sm` (8px) |

---

#### Dialog

**정의**
현재 작업을 중단하고 사용자의 확인 또는 입력을 요청하는 모달 오버레이.

**Variants**
| Property | Values |
|----------|--------|
| Type | `confirm`, `alert`, `form`, `custom` |
| Size | `sm`, `md`, `lg`, `full` |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Background | `color/fill/surface/primary` |
| Scrim | `color/fill/canvas/scrim` (#25252580) |
| Border Radius | `radius/lg` (16px) |

**접근성**
- `role="dialog"`, `aria-modal="true"`
- 열릴 때 포커스 내부로 이동, ESC로 닫기

---

#### Bottom Sheet

**정의**
화면 하단에서 슬라이드업되는 패널.

**Variants**
| Property | Values |
|----------|--------|
| Height | `fixed`, `flexible`, `full` |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Background | `color/fill/surface/primary` |
| Scrim | `color/fill/canvas/scrim` |
| Radius (top) | `radius/lg` (16px) |

---

#### Progress Indicator

**정의**
작업 진행 상태 또는 완료 단계를 시각적으로 표시하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `linear`, `circular`, `step` |
| Style | `determinate`, `indeterminate` |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Track | `color/fill/interaction/disabled` |
| Fill | `color/fill/interaction/primary` |

**접근성**
- `role="progressbar"`, `aria-valuenow`, `aria-valuemin`, `aria-valuemax`

---

#### System Message

**정의**
입력 필드 등 특정 컴포넌트 하단에 맥락에 맞는 안내 메시지를 표시하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `helper`, `positive`, `warning`, `negative` |

**토큰 매핑**
| Type | Text | Icon |
|------|------|------|
| Helper | `color/text/body-secondary` | `color/icon/secondary` |
| Positive | `color/text/positive` | `color/icon/positive` |
| Warning | `color/text/warning` | `color/icon/warning` |
| Negative | `color/text/negative` | `color/icon/negative` |

---

#### Nudge

**정의**
특정 UI 요소 주변에 표시하는 작은 안내 말풍선.

**목적**
- 신규 기능 소개, 온보딩, 중요 기능 강조에 사용한다.

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Background | `color/fill/surface/bubble` (#DDF1FB) |
| Border | `color/border/divider-highlight-blue` |

---

#### Result Box

**정의**
검색 결과 없음, 오류 발생 등 빈 상태를 안내하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `empty`, `error`, `no-result`, `network-error` |
| Action | `none`, `retry`, `go-home`, `custom` |

---

#### Loading

**정의**
데이터 로딩 또는 처리 중임을 표시하는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `spinner`, `skeleton`, `overlay` |

**토큰 매핑**
| Type | 색상 |
|------|------|
| Spinner | `color/fill/interaction/primary` |
| Skeleton | `color/fill/surface/tertiary` → `color/fill/surface/secondary` (shimmer) |

---

#### Ribbon Banner

**정의**
카드 모서리에 대각선으로 표시되는 띠 형태의 배너.

**목적**
- 특가, 신규, 마감임박 등 콘텐츠의 특별한 상태를 강조한다.

**Variants**
| Property | Values |
|----------|--------|
| Position | `top-left`, `top-right` |
| Color | `primary`, `negative`, `positive`, `warning` |

**토큰 매핑**
| Color | Background | Text |
|-------|-----------|------|
| Primary | `color/fill/interaction/primary` | `color/text/inverse` |
| Negative | `color/fill/surface/accent` | `color/text/inverse` |
| Positive | `color/fill/surface/positive-accent` | `color/text/inverse` |

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

**정의**
페이지 및 섹션의 제목을 표시하는 텍스트 컴포넌트.

**Variants**
| Level | Token | Size | Weight |
|-------|-------|------|--------|
| H1 | `font/wide/title-lg` | 42px | Bold |
| H2 | `font/wide/title-sm` | 36px | Bold |
| H3 | `font/wide/subtitle-lg-bold` | 28px | Bold |
| H4 | `body-xl-bold` | 21px | Bold |
| H5 | `body-lg-bold` | 18px | Bold |
| H6 | `body-md-bold` | 16px | Bold |

**토큰 매핑**
- Color: `color/text/title` (#051766)

**접근성**
- 시맨틱 HTML 태그 (`<h1>`~`<h6>`) 사용 필수
- 페이지당 `<h1>`은 1개만 사용

---

#### Paragraph

**정의**
본문 텍스트를 표시하는 컴포넌트.

**Variants**
| Token | Size | 용도 |
|-------|------|------|
| `body-lg` | 18px | 강조 본문 |
| `body-md` | 16px | 기본 본문 |
| `body-sm` | 14px | 보조 설명 |
| `body-xs` | 12px | 캡션, 주석 |

**토큰 매핑**
| 역할 | 토큰 |
|------|------|
| 기본 | `color/text/body` (#051766) |
| 보조 | `color/text/body-secondary` (#5E5E5E) |

---

#### Link

**정의**
클릭 시 다른 페이지 또는 외부 URL로 이동하는 텍스트 링크.

**Variants**
| Property | Values |
|----------|--------|
| Type | `inline`, `standalone`, `external` |
| State | `default`, `hover`, `visited`, `disabled` |

**접근성**
- `<a>` 태그 사용
- 외부 링크: `target="_blank"` + `rel="noopener noreferrer"`

---

#### Divider

**정의**
콘텐츠 영역을 시각적으로 구분하는 선 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Direction | `horizontal`, `vertical` |
| Weight | `thick` (2px), `thin` (1px) |

**토큰 매핑**
| Type | Color |
|------|-------|
| Primary | `color/border/divider-primary` (#D9D9D9) |
| Secondary | `color/border/divider-secondary` (#EDEDED) |
| Top (강조) | `color/border/divider-top` (#051766) |

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

**정의**
아이콘과 텍스트를 결합한 컴포넌트.

**목적**
- 서비스 특징, 부가서비스 항목 등 아이콘과 설명을 함께 표시한다.

**Variants**
| Property | Values |
|----------|--------|
| Icon position | `left`, `top` |
| Size | `lg`, `md`, `sm` |

---

#### Icon-text Information

**정의**
아이콘, 레이블, 값을 조합하여 키-값 형태의 정보를 표시하는 컴포넌트.

**목적**
- 항공편 정보(출발 시간, 소요 시간 등), 예약 상세 정보 표시에 사용한다.

**Variants**
| Property | Values |
|----------|--------|
| Layout | `horizontal`, `vertical` |

---

#### Legend

**정의**
차트, 좌석 배치도 등 시각적 요소의 색상 의미를 설명하는 범례 컴포넌트.

**목적**
- 색상만으로 의미를 전달할 수 없는 시각 요소에 텍스트 설명을 추가하여 접근성을 높인다.

**Usage**
- ✅ 좌석 선택 화면, 차트 등 색상 구분이 있는 모든 시각 요소에 범례를 제공한다

---

### 3.6 카드 & 컨테이너 (Card & Container)

공통 토큰:
- Card Radius: `radius/card` (16px)
- Card Background: `color/fill/surface/primary`
- Card Border: `color/border/tertiary`

---

#### Bottom Card

**정의**
화면 하단에 고정되어 요약 정보와 주요 CTA를 함께 표시하는 카드.

**목적**
- 항공권 선택 후 가격 요약 및 "예약하기" 버튼을 항상 노출한다.

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Top border | `color/border/divider-primary` |
| Price | `color/text/title`, `body-lg-bold` |

---

#### Content Visual Card

**정의**
이미지/영상과 텍스트가 결합된 콘텐츠 카드.

**목적**
- 여행지 소개, 프로모션, 기내 서비스 등 비주얼 중심 콘텐츠를 표시한다.

**Variants**
| Property | Values |
|----------|--------|
| Image position | `top`, `left`, `right`, `background` |
| Aspect ratio | `16:9`, `4:3`, `1:1` |

---

#### Image Card

**정의**
이미지를 중심으로 구성된 카드.

**Variants**
| Property | Values |
|----------|--------|
| Caption | `none`, `overlay`, `below` |

---

#### Logo Card

**정의**
파트너사 로고 또는 브랜드를 표시하는 카드.

**목적**
- 스카이팀, 제휴 카드사, 파트너 호텔 등의 로고를 표시한다.

---

#### Related Card

**정의**
현재 콘텐츠와 관련된 추천 항목을 표시하는 카드.

**목적**
- "이런 항공편도 있어요" 등 관련 콘텐츠를 추천한다.

---

#### Data Box

**정의**
레이블과 값으로 구성된 정보 표시 컨테이너.

**목적**
- 예약 상세, 승객 정보 등 구조화된 데이터를 표시한다.

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Background | `color/fill/surface/secondary` |
| Label | `color/text/body-secondary`, `body-xs` |
| Value | `color/text/body`, `body-sm-bold` |

---

#### Content Data Box

**정의**
Data Box의 확장형. 아이콘과 레이블-값 조합을 함께 표시하는 컨테이너.

**목적**
- 좌석 정보, 수하물 규정, 서비스 혜택 등 아이콘과 함께 데이터를 표시한다.

---

#### Image-text Box

**정의**
이미지와 텍스트 정보를 좌우로 나란히 배치한 컨테이너.

**목적**
- 기내식 메뉴, 서비스 상품 등 이미지와 상세 정보를 함께 제공한다.

---

#### Text Box

**정의**
텍스트 콘텐츠만으로 구성된 정보 컨테이너.

**목적**
- 안내 문구, 약관 요약, 주의사항 등을 구조적으로 표시한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `info`, `warning`, `neutral` |

**토큰 매핑**
| Type | Background | Left Border |
|------|-----------|------------|
| Info | `color/fill/surface/highlight` | `color/border/primary` |
| Warning | `color/fill/surface/warning` | `color/border/warning` |
| Neutral | `color/fill/surface/secondary` | `color/border/tertiary` |

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

**정의**
쿠폰, 할인권, 이용권 등 혜택 정보를 표현하는 카드 컴포넌트.

**목적**
- 마일리지 쿠폰, 할인 코드, 라운지 이용권 등의 혜택을 표시한다.

**포함 요소**
- 혜택명 및 설명
- 할인율/금액 또는 혜택 내용
- 유효기간
- 적용 조건
- 쿠폰 코드 (해당 시)
- 사용하기 버튼

**Variants**
| Property | Values |
|----------|--------|
| Status | `available`, `used`, `expired` |
| Type | `discount`, `free`, `mileage`, `lounge` |

**토큰 매핑**
| Status | Background | Border |
|--------|-----------|--------|
| Available | `color/fill/surface/primary` | `color/border/primary` (dashed) |
| Used / Expired | `color/fill/surface/secondary` | `color/border/tertiary` |

---

### 3.7 리스트 & 테이블 (List & Table)

---

#### List

**정의**
항목을 세로로 나열하는 기본 리스트 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `basic`, `icon-leading`, `image-leading`, `trailing-control` |
| State | `default`, `selected`, `disabled` |

**토큰 매핑**
| State | Background | Text |
|-------|-----------|------|
| Default | `color/fill/surface/primary` | `color/text/body` |
| Selected | `color/fill/interaction/selected-item` | `color/text/body` |
| Disabled | `color/fill/surface/primary` | `color/text/disabled` |

---

#### Listbox

**정의**
드롭다운 또는 패널 내에서 항목을 선택하는 리스트.

**목적**
- Select Box, Autocomplete 등의 드롭다운 내 선택 목록으로 사용한다.

**접근성**
- `role="listbox"`, `role="option"`, `aria-selected`

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
| Border | `color/border/divider-secondary` |

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

**정의**
관련된 링크 목록을 그룹화하여 표시하는 컴포넌트.

**목적**
- Footer 링크, 관련 서비스 바로가기 등을 정리하여 제공한다.

---

#### Order List

**정의**
선택한 서비스(수하물, 기내식, 좌석 등)의 목록과 금액을 표시하는 도메인 특화 컴포넌트.

**목적**
- 예약 흐름 중 사용자가 선택한 서비스 항목과 가격을 요약하여 확인하게 한다.

**포함 요소**
- 서비스 카테고리 (수하물, 기내식, 좌석, 부가서비스)
- 서비스 명칭, 단가, 수량, 소계
- 총합계

**Variants**
| Property | Values |
|----------|--------|
| Type | `collapsed`, `expanded` |
| Editable | `true`, `false` |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Background | `color/fill/surface/secondary` |
| Item text | `color/text/body`, `body-sm` |
| Total price | `color/text/title`, `body-lg-bold` |

---

#### Order List Tab

**정의**
구간별 또는 승객별로 Order List를 탭으로 분리하여 표시하는 도메인 특화 컴포넌트.

**목적**
- 왕복 항공편이나 여러 탑승객의 선택 내역을 탭으로 구분하여 확인한다.

**포함 요소**
- Tab (구간명 또는 승객명)
- 각 탭 내 Order List

**Usage**
- ✅ 구간: "서울 → 파리", "파리 → 서울" 형태로 표기
- ✅ 승객: "성인 1", "성인 2", "소아 1" 형태로 표기

---

### 3.8 복합 & 도메인 (Complex & Domain)

---

#### Accordion

**정의**
클릭 시 콘텐츠를 펼치거나 접는 토글 패널 컴포넌트.

**목적**
- FAQ, 운임 규정, 수하물 정책 등 선택적으로 열람할 콘텐츠를 공간 효율적으로 구성한다.

**Variants**
| Property | Values |
|----------|--------|
| Mode | `single`, `multiple` |
| Style | `bordered`, `filled`, `ghost` |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Header text | `color/text/body`, `body-md-bold` |
| Expanded background | `color/fill/surface/secondary` |
| Border | `color/border/divider-primary` |

---

#### Expander

**정의**
콘텐츠 일부를 잘라 표시하고 "더보기" 클릭 시 전체를 펼치는 컴포넌트.

**목적**
- 긴 약관 텍스트, 상품 설명 등 전체를 보여줄 필요가 없는 경우 공간을 절약한다.

---

#### Carousel (Swiper)

**정의**
콘텐츠를 가로 슬라이드로 탐색하는 컴포넌트.

**목적**
- 프로모션 배너, 목적지 카드 등 다수의 콘텐츠를 좁은 공간에서 탐색하게 한다.

**Variants**
| Property | Values |
|----------|--------|
| Type | `banner`, `card`, `thumbnail` |
| Indicator | `dots`, `numbers`, `none` |
| Autoplay | `true`, `false` |

**접근성**
- `role="region"`, `aria-label="슬라이드 영역"`
- 자동 재생 시 정지 버튼 제공 필수 (WCAG 2.1)

---

#### Load More

**정의**
콘텐츠 목록 하단에서 추가 항목을 불러오는 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Type | `button`, `infinite-scroll` |
| State | `default`, `loading`, `end` |

---

#### Chart

**정의**
데이터를 시각적으로 표현하는 차트 컴포넌트.

**목적**
- 마일리지 적립 추이, 가격 변동 그래프 등 데이터를 시각화한다.

**Variants**
| Type | 용도 |
|------|------|
| Line | 시계열 추이 |
| Bar | 카테고리 비교 |
| Pie/Donut | 비율 표시 |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| Primary data | `color/brand/darkblue/100` (#051766) |
| Secondary data | `color/brand/lightblue/100` (#57BBEB) |
| Grid line | `color/border/divider-secondary` |

---

#### Itinerary

**정의**
항공 여정 정보를 요약하여 표시하는 대한항공 핵심 도메인 컴포넌트.

**목적**
- 출발지-목적지 구조, 편명, 출발/도착 시간, 소요 시간, 경유 정보 등 항공 여정의 핵심 정보를 한눈에 보여준다.

**포함 요소**
- 출발 공항 IATA 코드 + 도시명 + 출발 시간
- 목적지 공항 IATA 코드 + 도시명 + 도착 시간
- 항공편명 (예: KE 001)
- 총 비행 소요 시간
- 경유 횟수 (직항 / 1회 경유 / 2회 이상)
- 경유지 정보 (공항, 대기 시간)
- 날짜 변경 표시 (익일 도착 등)
- 좌석 등급

**Variants**
| Property | Values |
|----------|--------|
| Type | `search-result`, `booking-summary`, `itinerary-detail` |
| Trip | `oneway`, `roundtrip`, `multi-city` |
| Stops | `direct`, `1-stop`, `2-stop` |
| Class | `economy`, `premium-economy`, `prestige`, `first` |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| 공항 코드 | `color/text/title`, `body-lg-bold` |
| 시간 | `color/text/body`, `body-md-bold` |
| 경유/소요시간 | `color/text/body-secondary`, `body-sm` |
| 직항 표시 | `color/text/positive`, `body-xs-bold` |
| Card radius | `radius/card` (16px) |

---

#### FromTo

**정의**
출발지와 목적지를 입력하는 도메인 특화 복합 입력 컴포넌트.

**목적**
- 항공권 검색의 핵심 진입점. 출발지/목적지 선택 및 스왑 기능을 제공한다.

**포함 요소**
- 출발지 입력 필드 (Autocomplete)
- 목적지 입력 필드 (Autocomplete)
- 출발지↔목적지 스왑 버튼
- 선택된 공항 IATA 코드 + 도시명 표시

**Variants**
| Property | Values |
|----------|--------|
| Layout | `horizontal` (웹), `vertical` (모바일) |
| State | `default`, `departure-focused`, `arrival-focused`, `filled` |

**토큰 매핑**
| 요소 | 토큰 |
|------|------|
| 선택된 공항 코드 | `color/text/title`, `body-xl-bold` |
| 도시명 | `color/text/body-secondary`, `body-sm` |
| 스왑 버튼 bg | `color/fill/interaction/primary` |
| 포커스 보더 | `color/border/primary` |

---

#### Passenger

**정의**
탑승객 수(성인/소아/유아)와 좌석 등급을 선택하는 도메인 특화 복합 입력 컴포넌트.

**목적**
- 항공권 검색 시 탑승객 구성과 좌석 등급을 한 곳에서 설정한다.

**포함 요소**
- 성인 (만 12세 이상) Spinbutton
- 소아 (만 2~11세) Spinbutton
- 유아 (만 2세 미만) Spinbutton
- 좌석 등급 선택: Economy / Premium Economy / Prestige / First
- 총 탑승객 수 요약 표시

**제약 조건**
- 성인: 최소 1명, 최대 9명
- 소아/유아: 성인 수를 초과할 수 없음
- 총 탑승객: 최대 9명

**Variants**
| Property | Values |
|----------|--------|
| Display | `inline`, `popover`, `bottom-sheet` |

---

#### Class

**정의**
좌석 등급 정보를 시각적으로 표현하는 도메인 특화 컴포넌트.

**목적**
- 이코노미, 프리미엄 이코노미, 프레스티지(비즈니스), 일등석의 특징과 혜택을 비교하거나 선택된 등급을 표시한다.

**포함 요소**
- 좌석 등급명 (한국어/영어)
- 등급 대표 이미지 또는 아이콘
- 주요 혜택 요약 (수하물 허용량, 좌석 너비 등)
- 운임 정보
- 선택 버튼

**Variants**
| Property | Values |
|----------|--------|
| Class | `economy`, `premium-economy`, `prestige`, `first` |
| Type | `select-card`, `info-badge`, `comparison` |
| State | `default`, `selected`, `unavailable` |

**토큰 매핑**
| Class | Background | Text |
|-------|-----------|------|
| Economy | `color/fill/surface/economy` (#FFFFFF) | `color/text/body` |
| Premium Economy | `color/fill/surface/premium` (#57BBEB) | `color/text/inverse` |
| Prestige | `color/fill/surface/prestige` (#051766) | `color/text/inverse` |
| First | `color/fill/surface/first` (#5E5E5E) | `color/text/inverse` |

---

### 3.9 미디어 (Media)

---

#### Image

**정의**
이미지를 표시하는 기본 미디어 컴포넌트.

**Variants**
| Property | Values |
|----------|--------|
| Fit | `cover`, `contain`, `fill` |
| Aspect ratio | `16:9`, `4:3`, `1:1`, `3:4`, `free` |
| Radius | `none`, `sm`, `md`, `lg`, `full` |

**Usage**
- ✅ 항상 `alt` 텍스트를 제공한다
- ✅ 장식적 이미지는 `alt=""`로 설정한다
- ✅ WebP 포맷 우선 사용, JPEG/PNG 폴백 제공

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
