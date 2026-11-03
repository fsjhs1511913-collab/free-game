🎯 3D 射擊特訓學院 (Aim Academy 3D)
![Aim Academy 3D Cover](image_1a2cea.jpg)
> 一款基於 WebGL / Three.js 開發的網頁端第一人稱射擊（FPS）瞄準與身法訓練系統。擺脫槍戰描邊與拉槍迷惘，隨時隨地在瀏覽器中建立極致的肌肉記憶與戰術走位反應！
---
📖 專案簡介 (Introduction)
《3D 射擊特訓學院》 是一款專為 FPS 遊戲玩家（如 CS:GO/CS2, VALORANT, Apex Legends 等）設計的現代化網頁版 3D 訓練場。
無須下載龐大的遊戲用戶端，打開瀏覽器即可即時進行手腕微調、甩槍反擊、動態跟槍以及高強度 3D 敵火對攻訓練。系統提供毫秒級反應時間統計、命中率分析與 AI 槍法教練即時評語，協助玩家全面提升射擊表現。
---
✨ 核心特色 (Key Features)
1. 🎯 多元化循序漸進關卡 (Progressive Training Levels)
LEVEL 1: 靜態基礎定位 (Static Aim) — 練習手腕微調與精準爆頭能力。
LEVEL 2: 反射甩槍 (Flick Shot) — 敵目標停留時間極短，鍛鍊眼手同步的反應力。
LEVEL 3: 橫移平滑跟槍 (Tracking AD-Strafe) — 預判目標急停與左右橫移軌跡。
LEVEL 4: 空間高低差無人機 (3D Aerial Drones) — 全方位 3D 空中高低差視野打擊。
LEVEL 5: 實戰敵方對攻 (AI Counter-Attack) — 敵方電腦即時鎖定並發射能量彈反擊，結合掩體與走位。
LEVEL 6: 極限生存圍攻 (Hostile Siege) — 高強度多重敵火對攻，考驗掩體運用、急停與極限爆頭壓制。
2. 🧱 擬真戰術戰場環境 (Warzone Environment)
實體掩體系統：包含廢墟破敗房屋、毀損重型大卡車、沙包與水泥防浪塊。
自然生態地貌：高聳岩壁、動態下沖瀑布與氣泡粒子、立體樹木與雜草叢地表。
真實彈道遮擋：所有地形與掩體皆具備物理判定，能有效阻擋敵我雙方子彈。
3. 🕹️ 流暢的第一人稱控制與反饋 (FPS Mechanics)
完整身法支援：支援 `WASD` 平滑移動、`Shift` 疾跑、`Space` 跳躍與 `C / Ctrl` 蹲下。
精準物理系統：採用 3D 垂直射線偵測（Raycasting）實現順暢爬坡與高台下降，搭配 AABB Box 防穿牆碰撞檢測。
打擊反饋：全 3D 槍械模型、槍口火光、後座力震退、爆頭暴擊浮動傷害字樣與紅框受傷視覺特效。
4. 🎵 戰術網頁音效與音樂引擎 (Procedural WebAudio Synth)
內建純程式碼合成了打擊樂與背景戰術電子音樂，無需額外下載音檔即可享受流暢無縫的音效反饋。
---
💡 創作緣由與動機 (Motivation & Background)
在現代主流的競技型 FPS 遊戲中，「爆頭線拉槍（Crosshair Placement）」 與 「身法掩體運用（Movement & Cover）」 是決定勝負的核心關鍵。
許多玩家常面臨以下痛點：
練習成本高：傳統練習軟體佔用硬體資源大，啟動繁瑣。
缺乏真實對抗：傳統射擊訓練器往往只有靜態圓靶，缺乏「敵人會開槍反擊」的真實走位壓力。
開發動機：
希望能打造一款輕量化、開箱即用且高度擬真的 3D 網頁訓練軟體。結合實體掩體地形與會反擊的 AI 電腦，讓玩家能夠在瀏覽器中隨時進行「邊走位邊瞄準」的實戰化訓練，打造最具實用價值的肌肉記憶。
---
🚀 開發歷程與技術優化 (Development Journey)
本專案經過多個階段的迭代開發與物理重構：
```
[階段一：基礎 3D 渲染與準心建立] 
  └─ 使用 Three.js 搭建 3D 空間、Pointer Lock 視角鎖定與基礎射擊判定。

[階段二：物理碰撞與地形探測重構]
  └─ 導入 3D 垂直射線探測 (Downward Raycast Floor Detection) 解決斜坡無法行走問題。
  └─ 加入 AABB 碰撞箱 (Box3 Colliders) 阻止角色與子彈穿透建物與掩體。

[階段三：AI 對攻與 HP 血量系統]
  └─ 開發 AI 敵方自動轉向與發射能量彈邏輯。
  └─ 加入玩家 HP 血量條、受傷畫面紅框警告與鏡頭震動特效 (Camera Shake)。

[階段四：戰場場景與沉浸視覺升級]
  └─ 構建廢墟房屋、卡車、動態瀑布粒子、樹木與雜草地貌，全面升級戰場沉浸感。

[階段五：音效引擎與 UI 視覺優化]
  └─ 採用 Web Audio API 實現純程式碼背景音樂合成與槍聲，打造炫酷視覺封面與結算面板。
```
---
🛠️ 技術架構 (Tech Stack)
前端框架與樣式：HTML5, CSS3, Tailwind CSS
3D 渲染引擎：Three.js (WebGL)
圖標庫：FontAwesome 6
字體：Google Fonts (Orbitron, Inter)
音效技術：Web Audio API (Procedural Audio Synthesis)
---
🎮 操作說明 (Controls)
按鍵 (Key)	功能 (Action)
`W` `A` `S` `D`	角色前後左右移動
`Mouse Move`	控制第一人稱視角 (需要 Pointer Lock)
`Left Click`	開槍射擊
`Space`	跳躍 (Jump)
`Shift`	疾跑 (Sprint)
`C` / `Ctrl`	蹲下 (Crouch)
`Esc`	釋放視角鎖定
---
📂 專案目錄結構 (Project Structure)
```text
.
├── index.html               # 遊戲主程式 (包含 HTML, CSS, JavaScript 與 Three.js 邏輯)
├── image_1a2cea.jpg         # 遊戲封面展示圖片
└── README.md                # 專案說明文件
```
---
📝 授權條款 (License)
本專案採用 MIT License 進行授權，歡迎學習交流與二次開發。
