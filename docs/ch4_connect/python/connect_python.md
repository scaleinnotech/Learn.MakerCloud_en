# Using Python to connect to MakerCloud
Python has a wide range of uses, and many control boards support the use of Python. Additionally, Raspberry Pi can coordinate with Python to use MQTT.
Overall, as long as the device can support python and connect to the internet, it can connect to MQTT.

[TOC]

## MQTT with MakerCloud using Python
Although Python has a library that supports MQTT, there may be issues when you use it. In order to better facilitate the connection to MakerCloud, we have written MakerCloudMQTT Library.
First, download the MakerCloud Python Library:  
[MakerCloudMQTT Library](library/MakerCloudMQTT.zip)

#### Installation
You must **install** these pieces of software before using MakerCloudMQTT:

1. Python
2. Paho MQTT

##### Installing Python
Users can download the installer from the official Python website: [Download Python](https://www.python.org/downloads/)
After downloading, open the installer and follow the instructions to install Python.

##### Installing Paho MQTT
MakerCloudMQTT uses Paho MQTT, so you need to install Paho MQTT first.
Press the system to open the Terminal or DOS program, and then enter:
```
pip install paho-mqtt
```
## Connecting MakerCloud
1. Create a python project called "main.py"
2. Unzip"MakerCloudMQTT.zip"
3. Copy "MakerCloudMQTT.py" and paste it in the same directory of "main.py"
4. Import MakerCloudMQTT.py
5. Set the Username to Max

#### What the code looks like:
```python
import MakerCloudMQTT

MakerCloudMQTT.username = 'Max' 
```
