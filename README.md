# Artist Recognition with CNN - 藝術名畫作者辨識

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red.svg)

## 📌 專案簡介
本專案為 **國立中央大學（National Central University）資訊管理系** 課程作業。目標是利用卷積神經網路（CNN）技術，從 50 位世界知名畫家的作品資料集中，訓練出一個能夠自動辨識畫作作者的 AI 模型。

專案的核心挑戰在於**複雜的資料前處理**：原始資料的標籤（Label）隱藏在圖片檔名之中，必須透過程式化流程進行提取、清洗與轉換，才能進入模型訓練階段。

## 📊 資料集說明
- **名稱**: [Best Artworks of All Time](https://www.kaggle.com/ikarus777/best-artworks-of-all-time) (Kaggle)
- **內容**: 包含 50 位最具影響力的畫家作品，總計數千張圖片。
- **特點**: 資料集存在類別不平衡問題（不同畫家的作品數量差異大），且標籤需從檔名中解析。

## 🛠 我完成的核心任務 (TODO 1-7)

在本專案中，我獨立完成了從環境建置到模型評估的完整 Pipeline：

1.  **TODO 1: 封包導入 (Dependencies Import)**
    - 配置開發環境，導入 `TensorFlow`, `Keras`, `OpenCV`, `Pandas` 等核心數據科學與深度學習庫。
2.  **TODO 2: 資料集下載與解析 (Dataset Acquisition)**
    - 透過程式化指令下載並解壓大型圖片資料集。
    - 讀取 `artists.csv` 並進行結構化處理，格式化畫家名稱以利後續標籤比對。
3.  **TODO 3: 資料夾遍歷與標籤提取 (Data Crawling & Labeling)**
    - 撰寫 Python 腳本遍歷訓練集與測試集資料夾。
    - **核心邏輯**：利用字串處理從圖片檔名中精確提取畫家姓名，並建立圖片路徑與標籤的映射關係。
4.  **TODO 4: 圖像預處理 Pipeline (Image Preprocessing)**
    - 實作圖像縮放功能，將所有圖片統一調整為模型輸入所需的解析度。
    - 進行像素歸一化（Normalization），提升模型收斂速度。
5.  **TODO 5: 標籤編碼 (Label Encoding)**
    - 將類別標籤（畫家名稱）進行 One-hot Encoding，轉化為模型可運算的數值格式。
6.  **TODO 6: CNN 模型架構設計 (CNN Architecture)**
    - 建構卷積神經網路模型，包含：
        - 多層卷積層 (Convolutional Layers) 提取視覺特徵。
        - 池化層 (Pooling Layers) 降低運算維度。
        - 密集連接層 (Dense Layers) 與 Dropout 防止過擬合。
7.  **TODO 7: 模型訓練與效能評估 (Training & Evaluation)**
    - 設定損失函數 (Loss Function) 與優化器 (Optimizer)。
    - 執行模型訓練並輸出 **Testing Accuracy** 與 **Loss**，驗證模型對未知畫作的辨識精度。

## 🚀 學習成果
- 掌握了處理非結構化資料（檔名中含標籤）的開發技巧。
- 深入理解 CNN 在多分類問題（50 類別）中的架構配置。
- 學習如何透過 Data Augmentation 或 Class Weight（可選）處理類別不平衡問題。

---
*註：本專案程式碼參考自 [TensorFlow 官方文件](https://www.tensorflow.org/) 並根據作業需求進行大量客製化實作。*