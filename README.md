# Fast-Timing-Model-Estimation-for-new-PVT-Novatek-Microelectronics
### 1.摘要
### 透過machine learning 方法加速設計standard cell library過程中需要產生新的PVT (Process, Voltage, Temperature) corners，取代原始需要使用SPICE並利用窮舉法非常耗時和耗運算資源的方法，用來加速在ASIC (Application-Specific Integrated Circuit) 及SoC (System on Chip) 設計流程。

### 2.方法
   ### (1) 特徵分類
   ### 將Type, Process, Voltage, Temperature, cell, transition, power分成共90種類型
   ### (2)刪除相同數值的index1_1~7, index2
   ### (3)新增特徵
   ### 在不同時間點輸入相同input會得到不同的output(落差1.5~3.5倍)，故新增輸入次數特徵，且不同output相關係數高達0.999
   ### (4) 使用XGBOOST進行訓練
### 3.結果
   ### (1)計算得分公式
   ### (2)Score：60.98 (優於目前公布成績的第四名)
