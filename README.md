# Taipei-QA-BertForSequenceClassification
使用BertForSequenceClassification訓練台北市政府局處問答資料集

大部分程式架構的參考來源 : [p208p2002/taipei-QA-BERT](https://github.com/p208p2002/taipei-QA-BERT)

貢獻 : 修改了[p208p2002/taipei-QA-BERT/preprocess_data.py](https://github.com/p208p2002/taipei-QA-BERT/blob/master/preprocess_data.py)中關於input_masks的錯誤。

## 檔案說明
### Data
- data_split.py : 將Taipei_QA_new.txt切割成train、test和valid資料的程式
- core.py : 處理dataset和label的轉換
- preprocess_data.py : BertForSequenceClassification的前處理
- train.py : BertForSequenceClassification的訓練
- predict.py : BertForSequenceClassification的預測
- requestment.txt : 紀錄需要安裝的環境
## 使用說明
### train的順序
```
python data_split.py    # 如果已經存在train、test和valid資料，就可以跳過這步驟
python train.py         # 如果想用訓練好的model可以去release下載，並將資料放入trained_model內，就可以跳過這步驟
```
### Demo
```
python predict.py
```
## 環境需求
- python 3.6+
- pytorch 1.3+
- transformers 2.2+
- CUDA Version: 10.0
