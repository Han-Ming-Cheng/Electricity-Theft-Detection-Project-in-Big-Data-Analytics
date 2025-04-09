# Electricity-Theft-Detection-Project-in-Big-Data-Analytics
# 🔌 Electricity Theft Detection Project in Big Data Analytics

本專案旨在透過機器學習與異常偵測技術，建立有效的電力竊盜偵測系統，協助電力公司提早發現可疑用戶，減少電力損失。

## 📌 專案簡介

- 全球每年因竊電造成的經濟損失高達數百億美元。
- 本研究以中國電網公司 (SGCC) 提供之資料集為基礎，進行竊電模式分析。
- 搭配視覺化分析、特徵工程與三種模型進行判斷。
- 另開發網頁應用介面，提供查詢與預測功能。

## 🧪 使用資料集

- **用戶數**：42,372
- **時間範圍**：2014/01/01 - 2016/10/31（共 1035 天）
- **標記欄位**：0（正常）/ 1（竊電）
- **挑戰**：
  - 資料缺失值高達 25%
  - 資料極度不平衡
  - 用戶用電差異大，需正規化處理

## 🛠️ 使用技術與方法

### 🧹 前處理

- 缺失值補全（週期性平均補值）
- 三西格瑪法修正離群值
- 標準化與排序調整
- 資料平衡（Random Under Bagging）

### 🧠 建立模型

1. **Wide & Deep CNN**
   - 寬層學習全域用電模式
   - 深度 CNN 捕捉周期性變化
   - AUC: 0.81，MAP@100: 0.91

2. **CLOF（Cluster-based LOF）**
   - 結合 K-means 與局部密度離群偵測
   - Accuracy: 0.87，但 Precision 與 Recall 偏低

3. **CBLOF（Cluster-based Local Outlier Factor）**
   - 基於群聚大小與距離評估離群值
   - MAP@50: 0.98，適合優先查詢可疑對象

### 📊 視覺化

- 每月/每週用電趨勢圖
- 正常用戶與竊電者用電圖像比對
- 以圖表強化差異辨識與模型可解釋性

### 🌐 系統開發

- 使用 Hugging Face Spaces 打造應用介面
- 提供：
  - 整體資料分析與可疑用戶排名
  - 特定用戶用電趨勢查詢與預測
- 三種模型均可於系統中切換使用

## 🧾 結論與貢獻

- 建立了三種竊電偵測模型，應用於大規模資料中
- 開發可即時預測的互動式系統
- 強調模型整合與使用彈性，具實務應用潛力

## 👨‍👩‍👧‍👦 專案成員分工

| 角色 | 成員 |
|------|------|
| Project Manager | 劉家維、陳雅柔 |
| Data Scientist | 邱奕銓、楊家瑋、羅然莉 |
| System Developer | 張子恩、韓明澄 |

## 💻 Demo & 使用說明

- [Colab 程式碼連結](https://colab.research.google.com/drive/14q_Yi6FcwT2aGlNRbvSl9VC-6HxZM0FT?usp=drive_link)
- [Hugging Face 展示系統](https://huggingface.co/spaces/peter572210355/demo_steal_electricity_detect)

---

歡迎 fork、討論與貢獻！🚀
