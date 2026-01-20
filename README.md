心血管健康數據分析與 BMI 計算器

這是一個基於 Python 的小型數據分析專案，旨在處理心血管健康相關資料夾，進行 BMI 指數的分類統計、視覺化呈現，並提供一個互動式的 BMI 計算工具。


📋 專案功能

本專案包含三大核心功能：

1.數據分類與統計：自動讀取 CSV 資料，計算所有樣本的 BMI 值，並根據標準將其歸類為「過輕」、「健康」、「過重」或「肥胖」。

2.資料視覺化：使用圓餅圖（Pie Chart）直觀展示不同 BMI 族群的佔比分佈。

3.互動式計算器：提供一個簡易的 UI 介面，讓使用者輸入身高體重後，即時獲得 BMI 數值與健康建議。


🛠 使用技術

Python 3：核心程式語言。

Pandas：用於資料處理與 CSV 檔案讀取。

Matplotlib：用於產生統計圓餅圖。

ipywidgets：用於建立 Jupyter Notebook 中的互動式輸入介面。


📊 BMI 分類標準本程式採用的 BMI 計算公式如下：

<img width="258" height="75" alt="image" src="https://github.com/user-attachments/assets/91b71643-22ee-4641-be5c-2d37f0ab724a" />

分類級距參考：

| BMI 範圍 | 分類 |

體重過輕 (Underweight)：BMI < 18.5

健康體重 (Normal Range)：18.5 ≦ BMI < 24

體重過重 (Overweight)：24 ≦ BMI < 27

肥胖 (Obesity)：BMI ≥ 27

輕度肥胖：27 ≦ BMI < 30

中度肥胖：30 ≦ BMI < 35

重度肥胖：BMI ≥ 35 

🚀 如何開始使用
1. 安裝必要套件在執行程式前，請確保你的環境中已安裝相關函式庫：
   pip install pandas matplotlib ipywidgets
2. 準備資料請確保專案目錄下存有 心血管100健康資料練習檔_學生.csv 檔案，且編碼格式為 utf-8。
3. 執行程式你可以按順序執行以下三段程式碼：
   Step 1: 讀取資料並列印各類別總人數。
   Step 2: 產生 BMI 分佈圓餅圖。
   Step 3: 啟動互動式小工具（需在 Jupyter Notebook 或 Google Colab 環境下執行）。

🔍 程式碼說明

資料處理：透過 pd.read_csv 讀取資料，並使用 for 迴圈與 if-elif 邏輯進行條件篩選。

視覺化配置：plt.pie 中設定了 autopct="%1.1f%%" 以顯示百分比，並透過 plt.axis('equal') 確保圓餅圖不會變形。

互動功能：使用 interact_manual 建立按鈕觸發機制，避免每次修改數值時重複運算。
