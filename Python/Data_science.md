# Pythonデータ解析

## ライブラリ読み込み

```python
import pandas as pd
import numpy as np
from matplotlib import pyplot as plt
%matplotlib inline

# 解析で使用
from sklearn.linear_model import LinearRegression as LR
```

## データの読み込み

```python
data = pd.read_csv('Path_to_CSV')
```

## 変数指定

```python
data['変数名']
```

## データ出力

### 先頭のみ出力

```python
data.head()
```

### 最終のみ出力

```python
data.tail()
```

### 列数・行数表示

```python
data.shape
```

### 基礎統計量表示

```python
data.describe()
```

### 欠損値カウント

```python
data.isnull().sum()
```

### 値ごとにカウント

```python
data['y'].value_counts()
```

### クロス集計

```python
pd.crosstab(data['x'], data['y'], margins=True)
```

### 行列を範囲指定

```python
data.iloc[:, 1:]
```

### コピー

```python
data.copy()
```

### 型とnullじゃないセルの数を出力

```python
data.info()
```

### グラフ出力

```python
data.plot(figsize=(12,4))
```

### CSVに出力

```python
sample[1] = pred
sample.to_csv('Path.csv', index=None, header=None)
```

## データ加工

### 特徴量作成

```python
data["変数"] = train["変数"].apply(lamda x:変数or条件)
```

### 型変換

```python
data["year"] = data["year"].astype(np.int64)
```

### 並び替え

```python
data.sort_values(by="変数")
```

### ビニング

```python
age_binning = pd.cut(data['age'], [0, 10, 20, 30, 40, 50, 60, 70, 80, 90])
```

## 回帰モデル作成

### モデル宣言

```python
model = LR()
model1.fit(説明変数, 目的変数)
```

### 傾き

```python
model1.coef_
```

### 切片

```python
model1.intercept_
```

### ダミー変数を作成

```python
pd.get_dummies(testX)
```

### 作成したモデルで予測する

```python
model1.predict(testX)
```

## 決定木

### 決定木モデル宣決定木言

```python
clf1 = DT()
clf1.fit(説明変数, 目的変数)
```

### dotファイル作成

```python
export_graphviz(clf1, out_file='tree.dot', feature_names=trainX.columns, class_names=['0', '1'], filled=True, rounded=True)
```
