# 使用M5Stack訂閱主題
在編程訂閱主題訊息到創客雲前，使用者必先學習如何令M5Stack連接創客雲MQTT，連接方法可根據硬件參考上面的教學。  
[使用M5Stack連接創客雲](../../ch4_connect/m5stack/connect_m5stack.md)

[TOC]

## 訂閱積木
利用UiFlow中的MQTT訂閱積木，配合MakerCloud Custom的資料處理積木便可以完整地接收及處理創客雲上的MQTT訊息。

**UiFlow訂閱積木**  
![img_1.png](img/img_1.png){:width="50%"}  
在連接創客雲後，訂閱創客雲主題。當收到MQTT訊息，便會運行此積木。

**UiFlow取得數據**  
![img_2.png](img/img_2.png){:width="20%"}  
當收到MQTT訊息後，使用此積木取得MQTT訊息的數據。

**處理創客雲數據**  
![img_3.png](img/img_3.png){:width="30%"}  
將收到的創客雲MQTT訊息處理，並分成鍵值對。

**取得值**  
![img_4.png](img/img_4.png){:width="15%"}  
因應鍵取得值

## 訂閱鍵值對訊息
#### 學習重點
- 學習如何透過AI2從訂閱的主題收到鍵值對訊息

#### 目標
- 訂閱主題
- 從創客雲接收MQTT鍵值對訊息

在此練習，使用者將會接收在發布練習中的隨機數字，所以開始前請先參考M5Stack發布隨機數字。  
[M5Stack發布隨機數字](../../../ch5_publish/m5stack/publish_m5stack/#_2)

**程式設計**

1. M5Stack連接Wi-Fi，然後把M5Stack連接到UiFlow
2. 加入創客雲 UiFlow Custom  
   [下載創客雲 UiFlow Custom](https://cutt.ly/makercloud)
3. 加入連接到創客雲所需的積木
4. 加入當按Button B，發布隨機數字到創客雲所需的積木  
![img_7.png](img/img_7.png){:width="70%"}
5. 加入「UiFlow訂閱積木」，輸入需訂閱的主題名稱
6. 在「訂閱積木」中，加入「處理創客雲數據」積木。然後把「UiFlow取得數據」積木加到「Topic data」
7. 在M5Stack的介面上加入「lable0」  
![img_6.png](img/img_6.png){:width="40%"}
8. 因為傳送到創客雲的鍵是「num」，所以「data key」是「num」。把「label0」的文字設為「取得值」積木，輸入「num」到「data key」  
![img_5.png](img/img_5.png)

完成編程後，把編程下載到M5Stack中。當按下「Button B」後，M5Stack會發布隨機數字到創客雲。
同時，M5Stack會從同一主題接收隨機數字並在屏幕中顯示。
