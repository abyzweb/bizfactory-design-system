# 가이드 HTML 전용 컴포넌트

퍼블로그 디자인 시스템 가이드 HTML 내부에서만 사용하는 컴포넌트입니다.
publog.co.kr 실서비스에는 사용하지 않습니다.

---

## Tinted Card (색상 강조 카드)

정보를 색상으로 구분해 표시하는 카드 컴포넌트. 아이콘·타이틀·설명이 중앙 정렬됩니다.

| 변형 | 클래스 | 배경 | 테두리 |
|------|--------|------|--------|
| 파랑 | `.tinted-card.blue` | `#f0f7ff` | `1.5px solid #89b4fa` |
| 노랑 | `.tinted-card.yellow` | `#fffbea` | `1.5px solid var(--friendly)` |
| 빨강 | `.tinted-card.red` | `#fef3f3` | `1.5px solid #f38ba8` |

```css
.tinted-card { border-radius: 12px; padding: 22px 18px; text-align: center; }
.tinted-card.blue   { background: #f0f7ff; border: 1.5px solid #89b4fa; }
.tinted-card.yellow { background: #fffbea; border: 1.5px solid var(--friendly); }
.tinted-card.red    { background: #fef3f3; border: 1.5px solid #f38ba8; }

.card-icon  { font-size: 26px; margin-bottom: 10px; }
.card-title { font-size: 13.5px; font-weight: 700; color: var(--stability); margin-bottom: 7px; }
.card-desc  { font-size: 12px; color: var(--text-muted); line-height: 1.75; }
```

**사용 예시**

```html
<div class="tinted-card blue">
  <div class="card-icon">⚡</div>
  <div class="card-title">타이틀</div>
  <div class="card-desc">설명 텍스트</div>
</div>
```

---

## Version Card (버전 구분 카드)

버전 관리 규칙을 Major·Minor·Patch로 구분해 표시하는 카드.

| 변형 | 클래스 | 배경 | 테두리 |
|------|--------|------|--------|
| Major | `.version-card.major` | `#fef3f3` | `1.5px solid #f38ba8` |
| Minor | `.version-card.minor` | `#f0f7ff` | `1.5px solid #89b4fa` |
| Patch | `.version-card.patch` | `var(--belief)` | `1.5px solid var(--border)` |

```css
.version-cards { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; }
.version-card  { border-radius: 10px; padding: 18px 20px; text-align: center; }
.version-card.major { background: #fef3f3; border: 1.5px solid #f38ba8; }
.version-card.minor { background: #f0f7ff; border: 1.5px solid #89b4fa; }
.version-card.patch { background: var(--belief); border: 1.5px solid var(--border); }

.v-label   { font-family: 'Montserrat', sans-serif; font-size: 10px; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase; margin-bottom: 6px; color: var(--text-muted); }
.version-card.major .v-label { color: #c0392b; }
.version-card.minor .v-label { color: #2980b9; }
.v-example { font-family: 'Montserrat', sans-serif; font-size: 15px; font-weight: 800; color: var(--stability); margin-bottom: 8px; }
.v-desc    { font-size: 12px; color: var(--text-muted); line-height: 1.5; }
```

---

## Tip 박스

보조 안내 문구를 강조 표시하는 박스.

```css
.tip {
  background: #fffbea;
  border: 1.5px solid var(--friendly);
  border-radius: 8px;
  padding: 14px 18px;
  font-size: 13px;
  color: var(--text-body);
  line-height: 1.7;
}
```
