# Using Python to subscribe to topics on MakerCloud
Before programming and subscribing to MakerCloud, users must first connect Python to MakerCloud MQTT. For instructions, refer to the following link:
[Using Python to connect to MakerCloud](../../ch4_connect/python/connect_python.md)

[TOC]

## Subscription functions
In the MakerCloud extension on python, there are different types of subscription functions.

#### MakerCloudMQTT.subscribe()
This block subscribes to topics on MakerCloud
```python
MakerCloudMQTT.subscribe(topic)
```
**Topic -**
the topic name created on "MakerCloud"

#### MakerCloudMQTT.message_handler
When a text message is received, this function will runs.
**
Define it by itself** first, then assign it to MakerCloudMQTT.
```python
def message_handler(topic, message):
     print('Topic: '+ topic +' Message: '+ message)

MakerCloudMQTT.message_handler = message_handler
```

**Topic -**
the name of the topic you are subscribed to

**Message -**
the received text message

#### MakerCloudMQTT.key_message_handler
When a key text message is received, this function will run.
**Define it by itself** first, then assign it to MakerCloudMQTT.
```python
def key_message_handler(topic, key, message):
     print('Topic: '+ topic +'Key:' + key + 'Message:' + message)

MakerCloudMQTT.key_message_handler = key_message_handler
```

**Topic -**
the topic you are subscribed to

**Key -**
the key of the received text message

**Message -**
the text of the received message

#### MakerCloudMQTT.key_value_handler
When a key-value pair message is received, this function will run.
**Define it by itself** first, then assign it to MakerCloudMQTT.
```python
def key_value_handler(topic, key, value):
     print('Topic: '+ topic +'Key:' + key + 'Value:' ,value)

MakerCloudMQTT.key_value_handler = key_value_handler
```

**Topic -**
the topic that you are subscribed to

**Key -**
the key of the received message

**Value -**
the received value

#### MakerCloudMQTT.coordinate_handler
When a latitude-longitude message is received, this function will run.
**Define it by itself** first, then assign it to MakerCloudMQTT.
```python
def coordinate_handler(topic, latitude, longitude):
     print('Topic: '+ topic +'Latitude:',latitude +' longitude:' ,Longitude)

MakerCloudMQTT.coordinate_handler = coordinate_handler
```

**Topic -**
The name of the topic you are subscribed to

**Latitude -**
The received latitude value

**Longitude -**
The received longitude value

## Receiving text messages
#### Learning Focus:
- Learn how to receive text messages from subscribed topics through Python

#### Goals:
- Subscribe to topics
- Receive text messages from MakerCloud

**Before programming on Python, we need to prepare on MakerCloud:**

1. Create a project
2. Create a topic
3. Copy the topic name in MakerCloud

   ![img_topic_message.png](img/img_topic_message.png){:width="70%"}
   
   **Then you can program in Python:**
```python
import MakerCloudMQTT

MakerCloudMQTT.username ='Max'
# Paste the topic name
topic ='QQP4LRB0'

# Define message_handler
def message_handler(topic, message):
     print('Topic: '+ topic +' Message: '+ message)

# Assign message_handler to MakerCloudMQTT.message_handler
MakerCloudMQTT.message_handler = message_handler
# Subscribe to topics
MakerCloudMQTT.subscribe(topic)
```

After finishing and running the program, return to your project's IOT homepage in MakerCloud.
Press the "Details" button in the topic to enter the topic homepage.
In the "Send Message to Subject" box, enter "hello" and click "Send".

![img_publishhello.gif](img/img_publishhello.gif)

In the Python program, you will receive a text message:
```
Topic: QQP4LRB0 Message: hello
```