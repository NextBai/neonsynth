# NeonSynth 80s ⚡ 賽博龐克復古音樂合成器

> 一款兼具極致視覺張力與高度互動性的「純單一 HTML 檔案」Web Audio 合成器與 16 步進節奏鼓機。

![NeonSynth Cyberpunk Audio Studio](https://images.unsplash.com/photo-1518709268805-4e9042af9f23?auto=format&fit=crop&w=1200&q=80)

---

## 🌟 核心特色 (Features)

- **雙八度合成器鍵盤 (Polyphonic Synth Keyboard)**：
  - 支援電腦鍵盤快速鍵即時彈奏（白鍵 `A S D F G H J K L ; '`，黑鍵 `W E T Y U O P ]`）。
  - 支援滑鼠點擊與行動裝置觸控。
  - 多種經典振盪器波形切換：鋸齒波 (Sawtooth)、方波 (Square)、正弦波 (Sine)、三角波 (Triangle)。
  - ADSR 尾音 (Release)、低通濾波 (Cutoff) 與空間回音 (Delay FX) 即時調節。
  - 八度升降切換（Octave - / +）。

- **16 步進節奏鼓機 (16-Step Beat Sequencer)**：
  - 4 個經典打擊樂軌道：大鼓 (Kick 808)、小鼓 (Snare)、踩鈸 (Hi-Hat)、重低音 (Cyber Bass)。
  - BPM (60 ~ 170) 速度即時無段調節。
  - 內建經典預設風格：**Synthwave**、**Cyber Beat**、**80s Chill**。
  - 隨機產生節奏與一鍵清空格點。

- **即時音訊示波視覺化 (Audio Visualizer Canvas)**：
  - 雙重視覺化模式：**示波器雷射光波 (Neon Waveform)** 與 **賽博頻譜立體長條 (Frequency Bars)**。
  - 3D 透視網格動畫與 CRT 螢幕掃描線質感。

- **錄製與作品匯出 (Recording & Export)**：
  - 支援一鍵錄製自己彈奏與節奏鼓機混音的音樂作品，並可直接下載為音訊檔。

---

## 🚀 快速開始 (Quick Start)

本專案為**純單檔案架構**，無任何外部構建工具（無需 Node.js、npm）：

1. 直接在瀏覽器中開啟 [index.html](index.html)。
2. 點擊「**⚡ 啟動音訊核心 (Start Engine)**」解鎖瀏覽器音效。
3. 點擊右上角「**🎵 播放示範曲**」或直接使用電腦鍵盤彈奏體驗！

---

## ⌨️ 鍵盤對照表 (Keyboard Shortcuts)

| 琴鍵音階 | 鋼琴音符 | 電腦鍵盤按鍵 |
| :--- | :--- | :--- |
| **低八度白鍵** | C4, D4, E4, F4, G4, A4, B4 | `A`, `S`, `D`, `F`, `G`, `H`, `J` |
| **低八度黑鍵** | C#4, D#4, F#4, G#4, A#4 | `W`, `E`, `T`, `Y`, `U` |
| **高八度白鍵** | C5, D5, E5, F5, G5, A5, B5 | `K`, `L`, `;`, `'`, `Z`, `C`, `B` |
| **高八度黑鍵** | C#5, D#5, F#5, G#5, A#5 | `O`, `P`, `]`, `X`, `V` |

---

## 🌐 部署至 GitHub Pages (GitHub Pages Deployment)

1. 將本專案 Push 至您的 GitHub 儲存庫。
2. 進入該 GitHub 專案的 **Settings** > **Pages**。
3. 在 **Build and deployment** 下的 **Branch** 選擇 `main` 分支並指定 `/ (root)` 資料夾。
4. 點擊 **Save**，幾分鐘後即可透過專屬網址公開瀏覽！
