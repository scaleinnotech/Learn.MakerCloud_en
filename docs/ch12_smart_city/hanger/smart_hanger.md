# Instructions for the Smart Hanger

[TOC]

The smart hanger connects to the smart lamppost through MakerCloud and the use of MQTT and helps demonstrate the helpfulness of a smart city when used in connection with the smart lamppost.

The smart hanger is a model of a programmable clothing hanger that can open close on command. 

Here are instructions on how to construct the smart hanger

### Parts Needed

Here are all of the parts you need for the smart Hanger:
- the Powerbrick parts are:
- micro:bit and armourbit
- kittenwifi
- 1 4PIN cord
- 1 3PIN cord
- 1 battery pack
- 1 servo motor

![img_1.jpg](img/img_1.jpg)

Here is how the connections will work:

![img_2.jpg](img/img_2.jpg)

### Assembly

Here are some sequential steps on how to put the parts together:

![img_3.jpg](img/img_3.jpg)

![img_4.jpg](img/img_4.jpg)

![img_5.jpg](img/img_5.jpg)

![img_6.jpg](img/img_6.jpg)

![img_7.jpg](img/img_7.jpg)

![img_8.jpg](img/img_8.jpg)

Here is an example of what a completed smart hanger can look like:

![img_9.gif](img/img_9.gif)

### Connecting with Smart Lamppost

First make sure that you have constructed the smart lamppost. For instructions, click [here](ch12_smart_city/lamppost/smart_lamppost.md)

Then, program the connection between the smart lamppost and smart hanger using event trigger.



###### Programming for Smart Lamppost:
Program the lamppost to constantly publish rain data to MakerCloud

![img_9.png](img/img_9.png)

###### Programming for Smart Hanger:
Program the hanger to open and close based on messages it receives from MakerCloud

![img_10.png](img/img_10.png)

#### Programming the Applets on MakerCloud:

###### Program an "Opening" applet that:

- Triggers when it receives a key-value message on the "Rain" data type that your lamppost is publishing to.
- Uses logic to check if the rain level is above a threshold and:
    - Sends an "open" message to the hanger topic the rain level is under the threshold

![img_11.png](img/img_11.png)

###### Program a "Closing" applet that:

- Triggers when it receives a key-value message on the "Rain" data type that your lamppost is publishing to.
- Uses logic to check if the rain level is above a threshold and:
    - Sends a "close" message to the lamppost topic if the rain level is above the threshold

![img_12.png](img/img_12.png)

Note that there must be two topics, one for the hanger and one for the lamppost. They cannot operate on the same topic.

This should connect the smart lamppost and smart hanger; here is an example of what it should look like:

![img_13.gif](img/img_13.gif)

