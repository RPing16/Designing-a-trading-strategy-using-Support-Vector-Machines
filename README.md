# Designing a trading strategy using Support Vector Machines(SVM)
使用過去6天報酬率的漲跌預測明天股價漲跌
## Support Vector Machines(SVM)
監督式機器學習算法，用於分類和迴歸分析，主要方法是找到一個超平面將所有數據點有效分開
## code重點說明
1.  **計算過去lag天漲跌##
- np.sign(data['Return'].shift(lag)) -> 1 = 上漲；-1 = 下跌
2.  **使用SVM用意**
- Y = 明天股價漲跌，X = 過去6天漲跌，使用X預測Y
- 依據X使用SVM進行分類，在依據今天的X資料預測明天股價漲跌
