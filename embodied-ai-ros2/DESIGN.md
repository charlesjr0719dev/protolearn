---
source_url: https://www.robot.com
site_name: robot.com
extracted_at: 2026-09-09
theme: light
use_case: Embodied AI 技術學習教材（LLM × ROS 2 整合指南）
tags: [robotics, AI, education, technical-reference]
---

# robot.com — Embodied AI 教材設計系統

## 北極星

印刷風雜誌排版 + 螢光筆標記重點。暖色紙面、墨黑字、單一重點色。
教材不是軟體儀表板，是一本你會劃重點的技術雜誌。

## CSS 變數（直接複製到 HTML）

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Noto+Sans+TC:wght@400;500;700&display=swap');

:root {
  --bg: #ffffff;
  --surface: #f8f6f3;
  --surface-2: #d9d7d5;
  --border: #262626;
  --text: #262626;
  --text-dim: #727272;
  --text-muted: #8f8e8d;
  --accent: #ff9600;
  --accent-bg: #fff3e0;
  --dark-bg: #262626;
  --dark-surface: #2d2d2d;
  --dark-text: #ffffff;
}
```

## 色彩表

| Hex | Name | 用途 |
|-----|------|------|
| #ffffff | Bone White | 頁面底色、暗色區塊上的反白文字 |
| #f8f6f3 | Warm Parchment | 課程卡片底色、自我檢查區塊 |
| #d9d7d5 | Fog Gray | 分隔線、靜音背景 |
| #8f8e8d | Ash Gray | 來源標記文字、圖說 |
| #727272 | Stone Gray | 次要內文、補充說明 |
| #262626 | Ink Black | 標題、主要內文、暗色區塊背景 |
| #2d2d2d | Charcoal | 暗色卡片、code block 背景 |
| #ff9600 | Amber Accent | 重點標記、學習重點標籤、重要概念高亮（替代原設計黃色，白底上對比度足夠） |
| #fff3e0 | Amber Light | 重點區塊底色、學習重點背景 |
| #000000 | Pure Black | 主要行動按鈕（僅用一次） |

## 設計規則

### Do
- 用 Amber Accent (#ff9600) 作為唯一的彩色——單色 + 一色系統
- 標題用 Inter 600，負字距（-0.025em ~ -0.03em），營造編輯感
- 全寬區塊交替：白 → 暖紙色 → 墨黑 → 橘色，製造頁面節奏
- 按鈕和標籤用 pill 形（24-30px 圓角）
- 卡片用 10px 圓角，跟 pill 區分
- 深度靠色塊對比而非陰影
- code block 用 Charcoal (#2d2d2d) 背景 + 白色文字
- 來源可信度用色碼標籤：已驗證（Amber）/ 社群驗證（Stone Gray 邊框）/ 未驗證（Fog Gray）

### Don't
- 不用漸層
- 不用陰影做層次
- 不用第二個彩色
- 不用襯線字型
- 標題不要寬鬆字距

## 字型設定

```css
font-family: 'Inter', 'Noto Sans TC', -apple-system, 'PingFang TC', sans-serif;
```

## 按鈕樣式範本

```css
.btn-primary {
  background: #000000;
  color: #ffffff;
  font-family: 'Inter', 'Noto Sans TC', sans-serif;
  font-size: 16px;
  font-weight: 500;
  border: none;
  border-radius: 30px;
  padding: 12px 24px;
  cursor: pointer;
}

.btn-secondary {
  background: transparent;
  color: #262626;
  font-family: 'Inter', 'Noto Sans TC', sans-serif;
  font-size: 16px;
  font-weight: 500;
  border: 1px solid #262626;
  border-radius: 30px;
  padding: 12px 24px;
  cursor: pointer;
}

.tag {
  display: inline-block;
  background: #ff9600;
  color: #262626;
  font-size: 12px;
  font-weight: 600;
  padding: 4px 12px;
  border-radius: 9999px;
  letter-spacing: 0.02em;
  text-transform: uppercase;
}

.tag-outline {
  display: inline-block;
  background: transparent;
  color: #727272;
  font-size: 12px;
  font-weight: 500;
  padding: 4px 12px;
  border-radius: 9999px;
  border: 1px solid #d9d7d5;
}
```
