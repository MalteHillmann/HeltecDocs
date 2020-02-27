# Connect "STM32 + LoRa" to LoRaWAN Server

In this document, all operations and tests must be performed with a standard [LoRaWAN Gateway](https://heltec.org/proudct_center/lora/lora-gateway/), and at least have 8 channels!

Before this operation, please read this document carefully: **[“STM32 + LoRa” Node Preparation & Config Parameters]() .**

&nbsp;

## Preparation

- Install [STM32CubeIDE](https://www.st.com/zh/development-tools/stm32cubeide.html#get-software) and [STM32CubeProgrammer](https://www.st.com/zh/development-tools/stm32cubeprog.html) correctly.
- A standard LoRaWAN gateway with at least 8 channels (based on SX1301/8 base band chip will be OK), and make sure your gateway had already connected to a LoRa server.
  - [How to connect HT-M01 to a LoRa server]().
  - [How to connect HT-M02 to a LoRa server]().

- A STM32 LoRa node( [LoRa Node 151](https://heltec.org/project/lora-node-151/) , [LoRa Kit 151](https://heltec.org/project/lora-kit-151/) , [Turtle Board](https://heltec.org/project/turtle-board/)), a high quality USB cable and an ST-LINK.

## Connect to TTN

Before that, make sure there is a LoRa Gateway active in your TTN's account.

### Register a device

Register a new device in TTN's "Applications" page. The `Device ID`, `Device EUI`, `App Key` can be generated automatically. users need make sure the relevant parameter in STM32 LoRa node is the same with TTN.

![](img/connect_to_gateway/02.png)

Correctly config LoRaWAN parameters for STM32 LoRa node, please refer to [this document](). If all goes well, we will be able to see Device is alive in "DEVICE OVERVIEW".

![](img/connect_to_gateway/03.png)

&nbsp;

## Connect to ChirpStack

Coming soon.

&nbsp;

## Important Hints

Please double check the following two things:

1. The LoRaWAN parameters is the same as server!
2. The listening frequency of your LoRa Gateway is the same as ESP32 LoRa node's sending frequency. We strictly follow [LoRaWAN 1.1 Regional Parameters](https://lora-alliance.org/sites/default/files/2018-04/lorawantm_regional_parameters_v1.1rb_-_final.pdf);
