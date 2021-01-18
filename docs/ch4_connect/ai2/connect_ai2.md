# Using App Inventor 2 to Connect to MakerCloud

[TOC]

## MakerCloud AI2 extension
Since App Inventor 2 does not have the MQTT function, it is necessary to download the extension before connecting to MQTT.
In order to facilitate using AI2, we have made a special extension for MakerCloud connecting to AI2:

[MakerCloud AI2 extension](extension/scale.MakerCloud.aix) (right click to save as new file）

## Connecting to MakerCloud

#### Join AI2 extension
In the extension column, click "import extension".
![img_1.png](img/img_1.png){:width="40%"}

Click "choose file".
![img_2.png](img/img_2.png){:width="60%"}

Select the downloaded "scale.MakerCloud.aix", then click "import".
![img_3.png](img/img_3.png){:width="60%"}

#### Join MakerCloud Components
Drag the MakerCloud component to the screen.
![img_4.png](img/img_4.png){:width="100%"}

#### Modifing your Username
MakerCloud will record the user's name, so you need to make a username that belongs to you in the component properties.
![img_5.png](img/img_5.png){:width="40%"}

#### Join the Connected MakerCloud Building Block
After joining MakerCloud AI2 extension, go to the programming page.
When the screen is initialized, execute "Call MakerCloud MQTT".
![img_6.png](img/img_6.png){:width="100%"}

This will successfully connect it to MakerCloud through MQTT