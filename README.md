# Wing Design System — Foundation Tokens

Wing Design System(WDS)의 디자인 파운데이션 토큰 소스 저장소입니다.  
Figma Variables를 JSON 형식으로 관리하며, 디자이너와 프론트엔드 개발자가 함께 사용합니다.

---

## 📁 저장소 구조

```
wing-design-system/
├── tokens/
│   └── variables.json     # Figma Variables 원본 (KE Global 컬렉션)
├── docs/
│   └── foundation.md      # 토큰 사용 가이드 (추후 추가)
└── README.md
```

---

## 🎨 토큰 구성

`variables.json`은 **KE Global** 컬렉션 기준으로 다음 카테고리를 포함합니다.

| 카테고리 | 내용 |
|---|---|
| `color/brand/lightblue` | 브랜드 라이트블루 (#57BBEB 기준, 10~100 단계) |
| `color/brand/darkblue` | 브랜드 다크블루 (#051766 기준, 10~100 단계) |
| `color/neutral` | 그레이 스케일 (10~90 + alpha) |
| `color/system` | 시멘틱 컬러 (green, red, orange 및 light 계열) |
| `color/membership` | SKYPASS 등급별 컬러 (MillionMiler, Premium, Select, Morning Calm, SKYPASS) |
| `grid` | 반응형 그리드 (375 / 768 / 980 / 1200 / 1440 브레이크포인트) |

---

## 🔄 업데이트 방법

1. Figma에서 Variables를 수정합니다.
2. **Variables to JSON** 플러그인으로 `variables.json`을 다운로드합니다.
3. 이 저장소의 `tokens/variables.json`을 새 파일로 교체합니다.
4. Commit 메시지 예시: `tokens: 컬러 토큰 업데이트 (v1.x.x)`

---

## 🛠 개발자 연동 가이드

### JSON 구조 예시

```json
{
  "name": "color/brand/lightblue/100",
  "type": "color",
  "isAlias": false,
  "value": "#57BBEB"
}
```

### CSS 변수로 변환 (Style Dictionary 사용 시)

```css
:root {
  --color-brand-lightblue-100: #57BBEB;
  --color-brand-darkblue-100: #051766;
}
```

> Style Dictionary 설정 파일은 추후 `build/` 폴더에 추가될 예정입니다.

---

## 📌 관리 정책

- 이 저장소는 **BJ (WDS팀)** 이 단독 관리합니다.
- 토큰 추가/변경은 Figma Variables 수정 후 플러그인을 통해 내보냅니다.
- 직접 JSON을 편집하지 않습니다. (Figma가 단일 진실의 원천)
- 버전 관리는 Commit 이력으로 추적합니다.

---

## 📬 문의

WDS 관련 문의는 Wing Design System 팀으로 연락해 주세요.
