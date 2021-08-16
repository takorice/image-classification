# image-classification

## 概要
麺類の食べ物(うどん、蕎麦、ラーメン)の入力画像に対して、画像分類を行う画像分類器です。  
少ない訓練データにおいても高い精度を出すようにするため、学習済みモデル (VGG16) のファインチューニングをする方式としています。  

なお、使用に当たっての注意点は以下の通りです。  
- 事前に画像分類モデルを構築する必要があります。
- Google Colaboratory を利用します。


## 技術要素
- Python
- tensorflow
- keras
- numpy


## 学習用の画像データセットの内容
- 訓練データ : 302 ファイル
- 検証データ : 111 ファイル

```bash
dataset
├── train
│   ├── ramen
│   ├── soba
│   └── udon
└── validation
    ├── ramen
    ├── soba
    └── udon
```

## 利用方法
1. Googleドライブに以下のファイルをアップロードする。
  - classification.ipynb
  - create_model.ipynb
  - dataset.zip を解凍したディレクトリ
2. Google Colaboratory で create_model.ipynb を開き、順次実行してモデルを作成する
3. Google Colaboratory で classification.ipynb を開く。
4. ドライブに画像をアップロードし、コード内の画像ファイル名を変更する。
5. 順次実行すると、読み込んだ画像と推論結果が表示される。
