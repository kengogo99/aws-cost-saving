# AWS 環境のコスト削減計画

## 目標
AWS環境のコスト削減を実現するために、EC2およびRDSのインスタンスを以下の条件で停止します。

- **平日**：8時間停止
- **土日祝日**：終日停止

## 計算内容

### 1. すべての停止時間の算出

#### 平日の停止時間
- 平日：1日あたり8時間停止
- 年間の平日数：261日

計算式：8時間 × 261日 = 2,088時間


**平日の合計停止時間**：**2,088時間**

#### 土日祝日の停止時間
- 土日祝日：終日停止（24時間停止）
- 年間の土日数：104日
- 日本の祝日数：16日
- 土日祝日合計：120日

計算式：24時間 × 120日 = 2,880時間


**土日祝日の合計停止時間**：**2,880時間**

#### 合計停止時間
2,088時間 + 2,880時間 = 4,968時間


**年間の総停止時間**：**4,968時間**

---

### 2. 年間コスト削減率の算出

年間総稼働時間を8,760時間（365日 × 24時間）として、停止時間から削減率を算出します。

計算式：コスト削減率 = (停止時間 ÷ 年間の総稼働時間) × 100 コスト削減率 = (4,968時間 ÷ 8,760時間) × 100 ≈ 56.7%


**年間のコスト削減率**：**約56.7％**

---

## 結果まとめ
- **年間の総停止時間**：4,968時間
- **年間のコスト削減率**：56.7%
  
上記の計算結果に基づき、AWSのEC2およびRDSの運用を調整することで、年間で約56.7%のコスト削減が可能と見込まれます。




