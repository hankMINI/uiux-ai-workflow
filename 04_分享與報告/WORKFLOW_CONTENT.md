# UI/UX AI 混合工作流 (WORKFLOW_CONTENT.md)

## 1. 搜尋資料找亮點 (策略階段)
- **狀態**: ✅ 已驗證
- **工具**: Google NotebookLM
- **作法**: 匯入競品資料、PDF，AI 提煉亮點。
- **Action Prompt**: `「根據以下競品資料，列出 3 個最具競爭力的功能亮點與 UX 策略。」`

## 2. 提案簡報 (排版階段)
- **狀態**: 🔄 優化中
- **工具**: NotebookLM + Gemini -> Google Slides
- **作法**: NotebookLM 整理重點 -> Gemini 生成大綱 -> 一鍵轉 Slides。
- **Action Prompt**: `「請將上述亮點轉化為 5 頁簡報大綱，格式需包含標題與內文點列。」`

## 3. 人天預估 (報價階段)
- **狀態**: ✅ 已驗證 (自建 Skill)
- **工具**: Project Architect Skill
- **作法**: 輸入一句話需求，自動生成 WBS 與 CSV 報價單。
- **Action Prompt**: `「幫我估算一個寵物電商 App 的工時，並產出 CSV 報價單。」`

## 4. 快速建立 Design System (規範階段)
- **狀態**: ✅ 已驗證
- **工具**: Design System Gen + Figma AI
- **作法**: 填寫 Brief，AI 生成 Prompt，貼入 Figma 一鍵繪製。
- **Action Prompt**: `「根據品牌色 #7c3aed，生成一套醫療風格的 Figma Make 指令。」`

## 5. 高擬真提案交付 (確認階段)
- **狀態**: ✅ 已驗證
- **工具**: Figma Make (AI)
- **作法**: 用詳細 Prompt 直接生成高保真畫面，包含真實文案。
- **Action Prompt**: `「生成一個簡約風的結帳頁面，需包含信用卡輸入與 Apple Pay 選項。」`

## 6. 全程 AI 製作 UIUX Flow (急件開發)
- **狀態**: ✅ 已驗證
- **工具**: Pencil.dev + Claude MCP
- **作法**: MCP 協定指揮 AI 畫 UI 並同步產出 Flex CSS 代碼。
- **Action Prompt**: `「使用 MCP 在 Pencil 中建立後台管理列表，並產出 Tailwind CSS。」`
