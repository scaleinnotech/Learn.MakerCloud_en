# Using M5Stack to connect to MakerCloud

[TOC]

## MakerCloud UiFlow Custom
UiFlow has pre-loaded the MQTT function, but the steps to connect to MakerCloud are more complicated.
In order to facilitate the connection of M5Stack and MakerCloud, users can download and use Custom:

[MakerCloud UiFlow Custom](https://cutt.ly/makercloud)

## Connect MakerCloud

#### Join MakerCloud UiFlow Custom
1. Click on the Custom(Beta) column and select "Open *.m5b* file".
2. Open the downloaded "MakerCloud1.m5b".

![img_3.gif](img/img_3.gif)
</br></br>

3. After opening the file, you can find blocks that work with MakerCloud in Custom.

![img_4.png](img/img_4.png)

#### Connect MakerCloud
1. Click on the "Advanced" column, then click on the "MQTT" column.
2. Under Setup, add the building blocks for setting up MQTT.
3. Click the "MakerCloud" column and add the "MakerCloud server" block to the "server" of the MQTT block setting.

![img_8.gif](img/img_8.gif) 
</br></br>
4.Add "mqtt start" to the setup building block.

![img_9.png](img/img_9.png){:width="80%"}
5. When using MQTT blocks, programming must be downloaded to M5Stack. Click the option in the upper right corner and then click "download".

![img_7.png](img/img_7.png){:width="70%"}

After the download is successful, M5Stack will be connected to MakerCloud.