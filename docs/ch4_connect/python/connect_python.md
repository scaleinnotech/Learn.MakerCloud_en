# 使用Python連接創客雲
Python的用途廣泛，不少控制板支援使用Python。而其中最為人熟悉的Raspberry Pi便可以利用Python使用MQTT。
當然不只是Raspberry Pi，只要是支援Python和網路連接的裝置都可以連接MQTT。

[TOC]

## 創客雲 Python MakerCloudMQTT
雖然Python有支援MQTT的Library，但普遍使用上均有一定的難道。為了方便使用者連接創客雲，我們編寫了MakerCloudMQTT Library。

首先，下載創客雲 Python Library:  
[MakerCloudMQTT Library](library/MakerCloudMQTT.zip)

#### 安裝方法
在使用MakerCloudMQTT之前必須**預先安裝**:

1. Python
2. Paho MQTT

##### 安裝Python
使用者可到Python官方網站下載安裝程式: [下載Python](https://www.python.org/downloads/)  
下載後，開啟安裝程式並按指示完成安裝。

##### 安裝Paho MQTT
MakerCloudMQTT 使用了Paho MQTT，因此需要先安裝Paho MQTT。  
按系統開啟Terminal或DOS程式，然後輸入
```
pip install paho-mqtt
```
## 連接創客雲
1. 創建"main.py"
2. 解壓縮「MakerCloudMQTT.zip」
3. 複製「MakerCloudMQTT.py」，貼上在「main.py」的同一目錄中
4. 導入MakerCloudMQTT
5. 設定使用者名稱

#### 連接編程示範
```python
import MakerCloudMQTT

MakerCloudMQTT.username = 'Max' 
```
