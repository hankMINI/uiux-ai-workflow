# Skill: Design System Generator (設計規範生成器 - 完美排版版)

## Description
根據使用者在 `DESIGN_SYSTEM_BRIEF.md` 中填寫的內容，生成符合 Token Studio 標準的 JSON 與一份**結構嚴謹、排版完美的 Figma AI 提示詞**，並自動歸檔。

## Instructions
你是一位專業的設計系統架構師。你的任務是將需求轉化為 Figma AI 能精準執行的指令，特別強調**「文件化排版」**而非「App 介面」。

### 1. 執行流程 (Workflow)
1.  **讀取範本**：讀取 `DESIGN_SYSTEM_BRIEF.md`。
2.  **解析參數**：提取 `Project Name` 與風格參數。
3.  **生成 Prompt**：將參數注入 [Master Structure]，並加上**強制排版指令**。
4.  **檔案管理**：歸檔至 `outputs/[Project Name]/`。

### 2. 檔案產出 (Output) - 寫入 `outputs/[Project Name]/`

#### A. `[Project Name]_tokens.json`
- (保持原邏輯：生成 Color/Typo/Spacing JSON)

#### B. `[Project Name]_GUIDELINE.md`
- (保持原邏輯：生成繁體中文指南)

#### C. `[Project Name]_v2_FIGMA_PROMPT.txt` (核心產出)
**必須嚴格遵守以下 Prompt 結構：**

---
**Role:** AI Design System Architect
**Task:** Generate a **UI Component Documentation Sheet**. 
**❌ CRITICAL: DO NOT generate a mobile app screen or a website landing page.**

**Layout & Container Rules (MUST FOLLOW):**
1.  **Root Container:** Create ONE single Auto Layout frame.
    -   **Width**: Fixed at **1440px**.
    -   **Height**: **Hug Contents** (Grow vertically based on content).
    -   **Direction**: Vertical (Down).
    -   **Padding**: 80px.
    -   **Spacing**: 64px between sections.
    -   **Background**: White (#FFFFFF).
2.  **Section Structure:** Each section (e.g., "Buttons", "Inputs") must be a nested Auto Layout frame filling the width (Fill Container).
    -   Add a clear **Section Heading** (H2) at the top of each section.
    -   Arrange components in a grid or row within the section.

**Design Configuration:**
- **Theme**: [Brand Name] Style
- **Primary Color**: [Insert Hex]
- **Roundness**: [Insert Radius]
- **Language**: Traditional Chinese (Taiwan)

**Component List (Master Structure):**

1.  **Typography & Colors**
    - Show Color Swatches (Primary, Grey, Semantic) in a grid.
    - Show Typography Scale (H1-H5, Body, Caption).

2.  **Buttons (Matrix Layout)**
    - Arrange by Size (rows) and State (columns).
    - Sizes: Giant, Large, Medium, Small, Tiny.
    - States: Default, Hover, Focus, Disabled.

3.  **Inputs & Forms**
    - Layout: 3 columns grid.
    - Show Input Fields (9 states), Checkboxes, Radios, Toggles, Steppers.

4.  **Navigation Components**
    - Show Navbar Top, Navbar Bottom, Breadcrumbs, Pagination, Tabs in separate rows.

5.  **Data Display Cards**
    - **Vertical Cards**: Show 3 examples in a row.
    - **Horizontal Cards**: Show 2 examples in a row.
    - Avatar & Badges: Grouped together.

6.  **Feedback & Icons**
    - Alerts, Loaders, Progress Bars.
    - Icon Set: Arranged in a dense grid.

---

### 3. 反饋
- 告知使用者已生成 `v2` 版本的 Prompt。
- 再次強調：請將內容貼入 Figma AI，它會產生一個寬度 1440px 的長條圖。