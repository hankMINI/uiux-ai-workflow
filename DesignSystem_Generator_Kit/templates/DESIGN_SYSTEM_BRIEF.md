<!-- @format -->

# Design System 需求規格書 (專業詳細版)

請填寫以下參數，以利生成符合團隊規範的 Design System。留空則由 AI 自動推薦。

## 1. 色彩系統 (Color System)

### 品牌色 (Brand Palette)

請填入 Hex Code，AI 將自動運算 10 階色票 (50-900)。

- **主要色 (Primary)**： #06C167 (用於按鈕、Logo、強調)
- **次要色 (Secondary)**： #000000 (用於輔助圖形、次要按鈕)
- **副次要色 (Tertiary)**： #F6F6F6 (用於標籤、裝飾)
- **提醒色 (Warning)**： #FFC043 (用於通知、Badge)
- **危險色 (Error)**： #E03E2F (用於刪除、警示)

### 中性色 (GrayScale) & 適用情境

請定義灰階色調偏向，AI 將生成 900-100 色階並定義用途 (如 900=標題, 500=Disable)。

- **色調偏向 (Tint)**： Cool (Pure / Cool / Warm / Slate)
- **背景色 (Background)**： Light Gray (White / Light Gray)

### 遮罩 (Overlay/Mask)

- **Mask-1 (一般遮罩)**： Opacity 40% (預設 50%，用於 Popup)
- **Mask-2 (深色遮罩)**： Opacity 70% (預設 80%，用於 Toast/Loading)

---

## 2. 字體系統 (Typography)

### 字體家族 (Font Family)

- **iOS/Mac**： PingFang TC (預設：PingFang TC)
- **Android**： Noto Sans TC (預設：Noto Sans TC)
- **Windows**： Microsoft JhengHei UI (預設：Microsoft JhengHei)
- **Engish**： Inter (預設：Inter / Roboto)

### 字級規範 (Type Scale)

請填入基準字級 (Body Text)，AI 將依此推算 Headline, Body, Caption 等完整規範。

- **基準字級 (Body Size)**： 16px (或 14px)
- **行高比例 (Line Height Ratio)**： 1.5 (標準) / 1.4 (緊湊) / 1.6 (寬鬆)

---

## 3. 介面物理 (UI Physics)

- **圓角 (Radius)**： 12px (例：4px / 8px / 16px)
- **間距基數 (Spacing)**： 4px (預設 8px)
- **陰影風格 (Shadows)**： Soft (Soft / Sharp / None)
