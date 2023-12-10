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

### 作成したモデルで予測する

```python
model1.predict(testX)
```
