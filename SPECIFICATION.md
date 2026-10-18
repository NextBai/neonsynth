# 專案規格書：NeonSynth 賽博龐克復古音樂合成器 (Web App)

## 1. 專案概述 (Overview)
- **專案名稱**：NeonSynth 80s - Cyberpunk Music Studio
- **目標**：打造一個兼具極致視覺張力與高度互動性的「純單一 HTML 檔案」賽博龐克風格音樂合成器與節奏創作站。
- **目標受眾**：喜愛 Synthwave、復古電子樂、賽博龐克美學的網路使用者與音樂愛好者。
- **最終交付**：單一檔案 `index.html`（CSS 與 JavaScript 完整內嵌），無外部依賴，可直接本機點擊開啟或託管於 GitHub Pages。

---

## 2. 核心功能模組 (Core Features)

### 2.1 雙八度合成器鍵盤 (Polyphonic Synth Keyboard)
- **鍵盤佈局**：
  - 提供兩組八度（C3 ~ B4）鋼琴式鍵盤（白鍵與黑鍵）。
  - 支援滑鼠/觸控點擊與**電腦鍵盤快速鍵**（下排 `A S D F G H J K`、上排黑鍵 `W E T Y U`，高音階使用第二排）。
  - 鍵盤按壓時具備流暢的「霓虹微亮與下沉」發光反饋。
- **音色控制 (Synthesizer Engine)**：
  - **振盪器波形選擇 (Waveform)**：Sine（柔和正弦波）、Square（8-bit方波）、Sawtooth（復古鋸齒波）、Triangle（三角波）。
  - **ADSR 包絡控制**：Attack（起音）、Decay（衰減）、Sustain（延音）、Release（釋放時長）。
  - **低通濾波器 (Low-Pass Filter)**：Cutoff 頻率與 Resonance 共振強度控制。
  - **八度切換 (Octave Shift)**：-1 / 0 / +1 快速升降八度。

### 2.2 16 步進節奏鼓機 (16-Step Beat Sequencer)
- **音軌配置 (Tracks)**：
  - 4 個經典打擊樂軌道：
    1. **Kick**：重低音大鼓（合成低頻滑音衝擊）
    2. **Snare**：清脆小鼓（白噪波 + 音調複合）
    3. **Hi-Hat**：高頻金屬踩鈸（閉合/開合細節）
    4. **Cyber Synth / Bass Hit**：重低音貝斯點音
- **步進操作與控制**：
  - 16 步進發光按鈕，點擊可即時開關觸發點。
  - **BPM 調節**：60 ~ 180 BPM 滑桿與即時顯示。
  - **播放控制**：Play（播放）、Pause（暫停）、Clear（清空步進）、Randomize（隨機生成靈感節奏）。
  - **預設節奏庫 (Presets)**：內建多組預設節奏（如 Synthwave Drive、Cyber Attack、Chill Neon）。
  - **動態跑馬指示**：流暢的發光掃描線即時指示目前步進拍點。

### 2.3 即時音訊畫布視覺化 (Audio Visualizer Canvas)
- **音訊分析**：透過 Web Audio `AnalyserNode` 即時提取頻率與時域波形數據。
- **雙重視覺化模式切換**：
  1. **Neon Waveform (示波器雷射光波)**：流動的霓虹光暈波形。
  2. **Frequency Spectrum (賽博頻譜柱狀圖)**：發光跳動的漸層立體柱狀頻譜。
- **視覺氛圍特效**：
  - 背景 3D 視角復古透視網格動畫（Retro Grid）。
  - 微微發光的 CRT 復古螢幕掃描線（Scanlines）與邊緣暗角。

### 2.4 音效處理與錄音匯出 (Master FX & Recording)
- **總控音量 (Master Volume)** 與一鍵靜音。
- **復古音效特效開關**：
  - **Delay (回音效果)**：時間與反饋比例。
  - **Drive / Distortion (過載飽和度)**：營造 80 年代錄音帶微破音質感。
- **即時錄音與重播 (Recording & Playback)**：
  - 支援使用者按下「Record」，即時錄下自己彈奏與節奏鼓機混音的音樂，可即時重播或下載音訊檔。

---

## 3. UI/UX 視覺設計與互動規範 (Design System)

- **主題風格**：**賽博龐克霓虹暗黑風 (Cyberpunk Dark Neon)**
- **配色系統 (Color Palette)**：
  - 主背景色：`#0a0b10` 深邃曜石黑
  - 輔助面板色：`#12131c` 半透明深藍黑毛玻璃（Glassmorphism + 1px 霓虹微邊框）
  - 主霓虹青綠：`#00f0ff` (Cyan Neon / Cyber Blue)
  - 副霓虹粉紫：`#ff007f` (Hot Pink / Magenta)
  - 亮黃琥珀：`#ffe600` (Electric Amber / Alert)
  - 發光陰影：`box-shadow: 0 0 15px rgba(0, 240, 255, 0.4)`
- **字型與排版**：
  - 搭配 Google Fonts（如 `Orbitron` 科技標題字體 + `Inter` / `JetBrains Mono` 參數數值字體）。
- **互動反饋**：
  - 滑鼠懸停光暈微調、按鍵發光、旋鈕拖曳平滑順暢、提示音符標籤（C, D, E...）。

---

## 4. 技術架構與相容性 (Technical Specifications)

1. **架構模式**：純前端單檔案（Single-file `index.html`）。
2. **無外部構建**：不需 Node.js、Vite 或 Webpack，點擊即可在任何主流瀏覽器（Chrome, Edge, Safari, Firefox）執行。
3. **音訊架構**：
   - 瀏覽器原生 `AudioContext`（相容使用者初次互動解鎖機制）。
   - 音色純以演算法合成（Oscillator + Noise buffer + BiquadFilter），不依賴外部龐大音檔載入，加載速度 0 秒延遲。
4. **響應式支援 (Responsive)**：支援電腦桌面（全鍵盤快捷鍵體驗）與平板/手機觸控操作。

---

## 5. 實作與交付里程碑 (Milestones)

- [x] **步驟一**：需求討論與確定專案規格書（本文件）。
- [ ] **步驟二**：根據規格書完成單一 `index.html` 網頁程式碼（包含現代精美 UI、Web Audio 合成器引擎、鼓機步進器與 Canvas 視覺化特效）。
- [ ] **步驟三**：上傳至 GitHub 並啟用 GitHub Pages，提供公開展示網址。
