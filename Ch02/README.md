# 第2章用サンプルデータ集

## ファイル説明

- `ch02.RData`：第2章のサンプルデータ集

## 使い方

- `load()`関数で読み込んでください。
- たとえば、`data`フォルダー内の`ch02.RData`を読み込む場合、以下のようにコードを入力します。

```r
load("data/ch02.RData")
```

- ファイルをダウンロードせず、以下のようにURLから直接読み込むこともできる（インターネット環境が必要）。

```r
load(url("https://github.com/JaehyunSong/r4ss-dataset/raw/refs/heads/main/Ch02/ch02.RData"))
```