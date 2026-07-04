---
name: antigravity-video-specs
description: |
  三類影片製作規範與自動工作流。說「啟動 claude-video-specs」「我要做影片」「製作教學影片」「按照影片規範做」時載入。
---

# 影片製作規範與自動工作流

本技能基於 `claude-video-specs` 專案，提供三類影片（活動紀錄影片、教學影片、社群科普影片）的製作標準規範與 5 階段自動工作流。

## 觸發情境

當使用者下達以下指令時，應啟動此工作流：
- 「啟動 claude-video-specs」
- 「我要做影片」
- 「按照三類影片規範做⋯」
- 涉及「活動紀錄影片」、「教學影片」或「社群科普影片」製作時

## 執行流程

1. **環境檢查**：
   - 檢查 Python, pip, edge-tts, Node.js, ffmpeg, Playwright 以及源石黑體。
   - 缺少的元件引導使用者安裝，或透過 `install/` 內的腳本自動安裝。
2. **介紹三類影片**：
   - 簡短呈現 01 活動紀錄、02 教學影片、03 社群科普影片的定位，並請使用者選擇要製作哪一類。
3. **試作**：
   - 依據 `specs/` 內的規範，複製 `examples/` 的範本，執行 Edge-TTS 旁白生成與 Playwright / FFmpeg 影片渲染。
4. **調整**：
   - 引導使用者微調字幕、視覺、動畫與素材。
5. **打包技能**：
   - 詢問是否將工作流打包為獨立的專屬技能。

詳細引導細節請直接讀取 [AGENTS.md](file:///d:/Antigravity/20260704%20Antigravity%20ep3/skills/08-video-specs/AGENTS.md)。
