# Using M5Stack to publish messages to MakerCloud
Before publishing messages to Maker Cloud, users must first learn how to connect M5Stack to MakerCloud via MQTT. For instructions on connecting, please refer to the following link.
[Using M5Stack to connect to Maker Cloud](../../ch4_connect/m5stack/connect_m5stack.md)

[TOC]

## Publish message programing block

Users can use the programming blocks of MakerCloud from Custom to publish messages to Maker Cloud.

**Publishing a  key-value pair message**
![img_2.png](img/img_2.png){:width="30%"}

- Publishes a key-value pair or key message to the topic on Maker Cloud.
- If the data sent is a number, a corresponding line chart will be automatically created on MakerCloud.

## Publishing a key-value pair message
#### Learning Focus
-Learn how to use M5Stack to publish key-value pairs to a topic on MakerCloud
-Learn to create a line graph on Maker Cloud that displays and records key-value messages

#### Exercise: Post random numbers
- Make a button that publishes a random key-value message when clicked.
- Create a line graph on Maker Cloud to display and record key-value messages

**Before programming on UiFlow, we need to prepare on MakerCloud:**

1. Create a project
2. Create a topic

**Then you can program on UiFlow:**

1. Connect M5Stack to Wi-Fi, then connect M5Stack to UiFlow
2. Add Maker Cloud UiFlow Custom
   [Download Maker Cloud UiFlow Custom](https://cutt.ly/makercloud)

3. Double-click the B Button of M5Stack in UiFlow to add the "Button B wasPressed" block
   ![img_3.png](img/img_3.png){:width="100%"}
   </br></br>
4. In the "Button B wasPressed" building block, add the key-value pair message block from MakerCloud Custom.
   ![img_5.png](img/img_5.png){:width="60%"}
   </br></br>
5. Copy the topic name in Maker Cloud
   ![img_topic_randNum.png](img/img_topic_randNum.png){:width="80%"}
   </br></br>
6. Paste the topic name in "Topic", enter "num" in "key", and add a "random integer from 0 to 10" block in "value"
   ![img_6.png](img/img_6.png){:width="65%"}
   </br></br>
   
When finished, return to the project homepage of Maker Cloud.
   When you press the button, you can see the key-value pair message from your app in the real-time data viewer.
   ![img_7.png](img/img_7.png){:width="70%"}

Then refresh the project home page and go to the chart home page.
![img_tochartpage.png](img/img_tochartpage.png){:width="100%"}

Maker Cloud will automatically record the name of the key and create a chart to display and record the key-value pair.
![img_8.png](img/img_8.png){:width="80%"}
