# Source 05：機器學習與釣魚網站偵測

## 一、資料基本資訊

- 研究主題：機器學習應用於釣魚網站偵測
    
- 英文名稱：Machine Learning-Based Phishing Website Detection
    
- 資料來源：UCI Machine Learning Repository
    
- 資料集名稱：Website Phishing
    
- 資料集作者：Rami Mohammad、Lee McCluskey
    
- 發布年份：2012
    
- DOI：10.24432/C51W2X
    
- 任務類型：監督式分類（Classification）
    

## 二、研究目的

本資料集提供正常網站與釣魚網站的特徵資料，可用於訓練機器學習模型。

主要目的：

1. 分析網站的可疑特徵。
    
2. 建立正常網站與釣魚網站分類模型。
    
3. 比較不同機器學習演算法。
    
4. 評估模型辨識釣魚網站的能力。
    

## 三、資料集內容

UCI Website Phishing 資料集包含：

- 總資料筆數：1,353 筆。
    
- 釣魚網站：702 筆。
    
- 正常網站：548 筆。
    
- 可疑網站：103 筆。
    
- 特徵欄位：9 個。
    
- 資料類型：整數型態。
    

注意：可疑網站不代表一定是詐騙網站，不能直接將其視為釣魚網站標籤。

## 四、重要網站特徵

資料集提供的特徵包括：

1. SFH：表單處理網址是否可疑。
    
2. popUpWindow：是否具有可疑彈出視窗。
    
3. SSLfinal_State：SSL 憑證相關狀態。
    
4. Request_URL：網頁是否從外部網址載入資源。
    
5. URL_of_Anchor：網頁連結網址的可疑程度。
    
6. web_traffic：網站流量特徵。
    
7. URL_Length：網址長度。
    
8. age_of_domain：網域年齡。
    
9. having_IP_Address：網址是否直接使用 IP 位址。
    

這些特徵可協助機器學習模型分析網站是否具有釣魚風險。

## 五、常見機器學習演算法

### 1. Logistic Regression（邏輯斯迴歸）

利用數學模型計算分類機率，適合建立簡單的分類基準。

### 2. Decision Tree（決策樹）

透過條件分支進行判斷，容易理解模型的分類規則。

### 3. Random Forest（隨機森林）

結合多棵決策樹進行分類，能降低單一決策樹過度擬合的風險。

### 4. SVM（支持向量機）

尋找不同類別之間的最佳分類邊界，適合處理多維度特徵。

注意：上述為可用於本資料集的候選演算法，不代表已完成模型實驗或確認哪一種表現最佳。

## 六、模型評估指標

### 1. Accuracy（準確率）

[  
Accuracy=\frac{TP+TN}{TP+TN+FP+FN}  
]

代表模型整體預測正確的比例。

### 2. Precision（精確率）

[  
Precision=\frac{TP}{TP+FP}  
]

代表模型判定為釣魚網站的結果中，真正屬於釣魚網站的比例。

### 3. Recall（召回率）

[  
Recall=\frac{TP}{TP+FN}  
]

代表所有真正的釣魚網站中，被模型成功找出的比例。

### 4. F1-score

[  
F1=2\times\frac{Precision\times Recall}{Precision+Recall}  
]

綜合考慮 Precision 與 Recall。

### 5. 混淆矩陣

- TP：正確辨識釣魚網站。
    
- TN：正確辨識正常網站。
    
- FP：將正常網站誤判為釣魚網站。
    
- FN：將釣魚網站誤判為正常網站。
    

在防詐系統中，FN 特別值得注意，因為它代表真正的釣魚網站沒有被偵測出來。

## 七、AI 偵測系統流程

本專題預計採用以下流程：

1. 蒐集正常網站與釣魚網站資料。
    
2. 整理及清洗資料。
    
3. 擷取網站特徵。
    
4. 將資料分成訓練集與測試集。
    
5. 使用不同機器學習演算法訓練。
    
6. 使用測試集評估模型。
    
7. 比較 Accuracy、Precision、Recall、F1-score。
    
8. 選擇適合的模型。
    
9. 輸出網站風險判斷結果。
    

## 八、與本專題的關係

本資料集可作為 AI 網路詐騙偵測系統的實作參考。

本專題可以先從釣魚網站分類開始，再延伸到詐騙簡訊及詐騙訊息的文字分析。

未來可整合 NLP 與機器學習，建立同時分析文字內容及網站特徵的防詐系統。

## 九、原始資料來源

資料集：Website Phishing

作者：Rami Mohammad、Lee McCluskey

平台：UCI Machine Learning Repository

DOI：  
10.24432/C51W2X

官方網址：  
[https://archive.ics.uci.edu/dataset/379/website+phishing](https://archive.ics.uci.edu/dataset/379/website+phishing)

相關研究：  
Comparative evaluation of machine learning algorithms for phishing site detection

PMC 原文：  
[https://pmc.ncbi.nlm.nih.gov/articles/PMC11232597/](https://pmc.ncbi.nlm.nih.gov/articles/PMC11232597/)

## 十、知識連結

- [[AI_Scam_Wiki_Home]]
    
- [[Source_01_網路詐騙基本概念]]
    
- [[Source_02_假投資詐騙案例]]
    
- [[Source_03_AI網路詐騙偵測技術]]
    
- [[Source_04_NLP自然語言處理]]
    
- [[AI_Detection]]
    
- [[Scam_Basics]]
    

## 十一、資料驗證紀錄

- 已取得 UCI 官方資料集頁面。
    
- 資料筆數、特徵數及分類數量依官方資料集整理。
    
- 演算法為本專題規劃的候選方法。
    
- 評估公式為標準分類評估指標。
    
- 尚未實際訓練模型，因此不宣稱任何實驗準確率。
    
- 相關研究可作為進一步比較的學術參考。
- 