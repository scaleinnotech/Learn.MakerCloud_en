# Use BBC micro:bit to publish messages
Before programming and publishing messages to MakerCloud, users must first connect micro:bit to MakerCloud via MQTT. For instructions, refer to the following link:

[Using BBC micro:bit to connect to MakerCloud](../../ch4_connect/microbit/connect_microbit.md)

[TOC]

## KittenWiFi
Even if you use different micro:bit expansion boards, they can use the same program blocks to program and publish messages as long as they are successfully connected to MakerCloud. The following uses Armour:bit as a demonstration.
**Note that each program must initially connect to Wi-Fi and MakerCloud MQTT. **
### publish message blocks
In the MakerCloud extension, there are different types of publishing program blocks, depending on the data type that is being sent.

**Publishing a text message**

![img_1.png](img/img_1.png){:width="45%"}

Publishes a text message to a topic via KittenWiFi on MakerCloud

**Publish a key text message**

![img_2.png](img/img_2.png){:width="60%"}

Publishes a key text message to a topic via KittenWiFi on MakerCloud

**Publish a  key-value pair message**

![img_3.png](img/img_3.png){:width="50%"}

Publishes a key-value message to a topic via KittenWiFi on MakerCloud, which automatically creates a corresponding line chart on MakerCloud

**Publishing latitude and longitude data points**

![img_4.png](img/img_4.png){:width="70%"}

Publish a latitude and longitude message to a topic via KittenWiFi on MakerCloud

### Publishing a text message
#### Learning Focus
- Learn how to publish text messages to a topic on MakerCloud via KittenWiFi
#### Exercise: Say hello to MakerCloud
##### Goal:
When you press "A" on your micro:bit, it will publish the text message "hello" to a topic on MakerCloud.

![img_9.png](img/img_9.png){:width="70%"}

**Preparation on MakerCloud:**

1. Create a project
2. Create a topic

**Programming on MakeCode:**

1. Create a project
2. Add the MakerCloud KittenWiFi extension:
   [https://github.com/maxwong-scale/pxt-makercloud-V2]()
3. On start:
   Update armour:bit port, connect WiFi and MakerCloud MQTT
4. When button "A" is pressed:
   Publish a text message
   
   ![img_5.png](img/img_5.png)
   </br></br>
5. Copy the topic name in MakerCloud
   
   ![img/img_topic_message.png](img/img_topic_message.png){:width="80%"}
   </br></br>
   
6. Paste in the "topic" of the publish text message block
7. Enter "hello" in "message"
   
   ![img_7.png](img/img_7.png){:width="90%"}
   </br></br>
8. Download the program to your micro:bit
   
   When finished, return to your project homepage on MakerCloud.
   After pressing A on your micro:bit, you should see the text messages sent from your micro:bit in the real-time data viewer.
   
   ![img_8.png](img/img_8.png){:width="70%"}

### Publishing a key-value pair message
#### Learning Focus
- Learn how to publish key-value pairs to a MakerCloud topic via KittenWiFi
- Learn to create a line graph on MakerCloud to display and record key-value pair messages

#### Exercise: publish random numbers
##### Goals
- When you press A on your micro:bit, the micro:bit will publish a key-value pair message (a random number value) on MakerCloud
- Create a line graph on MakerCloud to display and record key-value pairs

![img_10.png](img/img_10.png){:width="80%"}

**Preparation on MakerCloud:**

1. Create a project
2. Create a topic

**Programming on MakeCode:**

1. Create a project
2. Add the MakerCloud KittenWiFi extension:
   [https://github.com/maxwong-scale/pxt-makercloud-V2]()
3. On start:
   Update armourbit port, connect WiFi and MakerCloud MQTT
4. When button "A" is pressed:
   Publish a key-value pair
   
   ![img_11.png](img/img_11.png)
   </br></br>
   
Note: There are **publish key text pair** and **publish key-value pair** blocks available. Users can decdide which to use according to the type of data that they want to send.
5. Copy the topic name in MakerCloud
   
   ![img_topic_randNum.png](img/img_topic_randNum.png){:width="80%"}
   </br></br>
   
6. Paste in the "topic" of the publish text message building block
7. Enter "num" in "key" and add "random number 0-10" in 0
   
   ![img_13.png](img/img_13.png)
   </br></br>
   
8. Download the program to micro:bit
   
When finished, return to the project homepage of MakerCloud. 
After pressing A on your micro:bit, you should see the key-value or key-text messages from your micro:bit in the data viewer.

   ![img_14.png](img/img_14.png){:width="70%"}

Then refresh the project home page and go to the chart home page.

![img_tochartpage.png](img/img_tochartpage.png){:width="100%"}

MakerCloud will automatically record the name of the key and create a chart for the key-value pair messages.

![img_15.png](img/img_15.png){:width="60%"}