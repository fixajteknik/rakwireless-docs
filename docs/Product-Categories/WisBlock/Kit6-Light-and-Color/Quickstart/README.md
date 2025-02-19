---
rak_img: /assets/images/wisblock/kits/6_lightcolor_kit_1.png
rak_desc: Contains extensive instructions and tutorials for installing and deploying your LoRaWAN project with the WisBlock IoT Education Kit - Light & Color.
rak_grp: [wisblock,wiskit]
rak_model: Light & Color
prev: ../Overview/
next: ../Datasheet/
tags:
    - IoT Education Kit
    - WisBlock IoT Education Kit - Light & Color
    - WisBlock Kit
    - WisBlock
---

# WisBlock IoT Education Kit - Light & Color Quick Start Guide

## Prerequisite

### What Do You Need?

The **WisBlock IoT Education Kit - Light & Color** comes with **RAK19007** and **RAK19001** **WisBlock Base boards**, two **RAK4631** **WisBlock Core modules**, and set of sensor modules to explore with. Before going through each and every step on using the **WisBlock IoT Education Kit - Light & Color**, make sure to prepare the necessary items listed below:

#### Hardware

- [RAK4631 WisBlock Core](https://store.rakwireless.com/products/nordic-nrf52840-ble-core-module-for-lorawan-with-lora-sx1262-rak4631-rak4631-c?variant=42576992436422)
- [RAK19007 WisBlock Base Board](https://store.rakwireless.com/products/rak19007-wisblock-base-board-2nd-gen)
- [RAK19001 WisBlock Base Board](https://store.rakwireless.com/products/rak19001-wisblock-dual-io-base-board)
- [RAK12019 UV Sensor](https://store.rakwireless.com/products/rak12019-wisblock-uv-sensor)
- [RAK12010 Ambient Light Sensor](https://store.rakwireless.com/products/wisblock-ambient-light-sensor-rak12010)
- [RAK12021 RGB Light Sensor](https://store.rakwireless.com/products/rak12021-wisblock-rgb-sensor)
- [RAK14001 RGB LED Module](https://store.rakwireless.com/products/rgb-led-module-rak14001)
- [RAK14003 LED Bar Module](https://store.rakwireless.com/products/wisblock-led-bar-module-rak14003)
- USB C Cable
- [RAK19005 Sensor Extension Cable (optional)](https://store.rakwireless.com/products/fpc-extension-cable-for-slot-a-to-d-rak19005)
- [RAK19008 IO Extension Cable (optional)](https://store.rakwireless.com/products/wisblock-io-extension-cable-rak19008)
- [Li-Ion/LiPo battery (optional)](https://store.rakwireless.com/collections/wisblock-accessory/products/battery-connector-cable?utm_source=BatteryConnector&utm_medium=Document&utm_campaign=BuyFromStore)
- [Solar charger (optional)](https://store.rakwireless.com/collections/wisblock-accessory/products/solar-panel-connector-cable?utm_source=SolarPanelConnector&utm_medium=Document&utm_campaign=BuyFromStore)

#### Software

##### Arduino

- Download and install the [ArduinoIDE](https://www.arduino.cc/en/Main/Software).
- To add the RAKwireless Core boards on your Arduino Boards Manager, install the [RAKwireless Arduino BSP](https://github.com/RAKWireless/RAKwireless-Arduino-BSP-Index).

## Product Configuration

### Hardware Setup & Sample Applications

**WisBlock IoT Education Kit - Light & Color** comprises of UV and light sensors, and RGB LED modules that can be used with **RAK19007** and **RAK19001** **WisBlock Base boards** which you can choose from. This kit will help you learn how to measure light and colors and how to create different light sources. You can choose from these devices for your desired applications.

- **UV Index & UV Intensity Meter - RAK4631 + RAK12019 + RAK12010 + RAK14003**

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/uv_index.png"
  width="65%"
  caption="RAK4631 + RAK12019 + RAK12010 + RAK14003"
/>

- **RGB LED Color Changer - RAK4631 + RAK12021 + RAK14001**

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/rgb.png"
  width="60%"
  caption="RAK4631 + RAK12021 + RAK14001"
/>

#### Assembly and Functionality Tests of WisBlock Light and Color Modules

The following WisBlock Light and Color modules listed below are used in this kit. To check for their asssemblies and functionalities, please refer to the links below for further information:

- [RAK12019 UV Sensor](https://docs.rakwireless.com/Product-Categories/WisBlock/RAK12019/Quickstart/#prerequisite)
- [RAK12010 Ambient Light Sensor](https://docs.rakwireless.com/Product-Categories/WisBlock/RAK12010/Quickstart/#prerequisite)
- [RAK12021 RGB Light Sensor](https://docs.rakwireless.com/Product-Categories/WisBlock/RAK12021/Quickstart/#prerequisite)
- [RAK14001 RGB LED Module](https://docs.rakwireless.com/Product-Categories/WisBlock/RAK14001/Quickstart/#software-configuration-and-example)
- [RAK14003 LED Bar Module](https://docs.rakwireless.com/Product-Categories/WisBlock/RAK14003/Quickstart/#software-configuration-and-example)

### Software Configuration and Examples

#### LoRaWAN Applications for WisBlock IoT Education Kit - Light & Color using TTN and Qubitro

- [UV Index & UV Intensity Monitoring LoRaWAN Application](#uv-index-uv-intensity-monitoring-lorawan-application)
- [Light Color Recognizer LoRaWAN Application](#light-color-recognizer-lorawan-application)

##### UV Index & UV Intensity Monitoring LoRaWAN Application

The **UV Index & UV Intensity Monitoring LoRaWAN Application** is used to monitor the UV index, UV intensity and light intensity from the sun exposure. It uses **RAK12019** which is an ambient light sensor and a ultraviolet sensor which is based on **LTR-390UV-01** from Lite-On. Also, it uses **RAK12010** which is an ambient light sensor which is based from **VEML7700** chip from Vishay Semiconductors. And finally the **RAK14003** LED bar module which visualizes the UV Index level measured from the **RAK12019** module.

**UV Index** is the measure of the level of UV radiation from the sun exposure. It ranges from zero upward. The higher the UV Index level, the greater potential for damage to the skin and eye. The **UV Index & UV Intensity Monitoring** device will help alert people about the need to use sun protection when going outside. Below is the **UV Index Scale** which can help users monitor the level of the UV Index during daytime. For further details about UV index levels and their impacts, you can refer from this [link](https://www.epa.gov/sunsafety/uv-index-scale-0).

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_UV_Index.png"
  width="60%"
  caption="UV Index Scale"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_UV.png"
  width="50%"
  caption="UV Index & UV Intensity Monitoring device"
/>

###### UV Index & UV Intensity Monitoring - TTN Registration Section and Device Registration

1. If you already have an existing TTN account, you may proceed to the next steps. If you haven't created any TTN account, please refer to this [link](#ttn-account-creation) to create one.

2. Once done with the TTN account creation, you may now proceed with the device registration. Please refer to this [guide](#device-registration) for your reference. After creating the application and adding the device in TTN, you can proceed on the LoRaWAN Code uploading steps.

###### LoRaWAN Code for UV Index & UV Intensity Monitoring

1. If you already have **Arduino IDE** installed to your laptop or PC and added **RAK4631 board** into it, you may proceed to the next step. If you haven't yet installed the **Arduino IDE**, please refer to this [link](#arduino-ide-installation-rak4631) for the steps.

2. After the installation, you can now proceed programming your **UV Index & UV Intensity Monitoring** device. Just copy the code below for **UV Index & UV Intensity Monitoring LoRaWAN Application** and paste it into the **Arduino IDE**.

::: tip 📝 NOTE

The example code uses [SX126x-Arduino](https://github.com/beegee-tokyo/SX126x-Arduino) library which needs to be added to successfully compile the LoRaWAN code.

:::

::: details Click Here to View Example Code
```c
#include <Arduino.h>
#include <LoRaWan-RAK4630.h>  //http://librarymanager/All#SX126x
#include <SPI.h>
#include <Wire.h>

#include "UVlight_LTR390.h"                // http://librarymanager/All#RAK12019_LTR390
UVlight_LTR390 ltr = UVlight_LTR390();

#include "Light_VEML7700.h"                // http://librarymanager/All#Light_veml7700
Light_VEML7700 VMEL = Light_VEML7700();

uint16_t uvi;
uint32_t uvs;
uint32_t lux;
uint32_t white;
uint32_t raw_als;

#include <Adafruit_MCP23X17.h>  //http://librarymanager/All#Adafruit_MCP23017
Adafruit_MCP23X17 mcp;

// Added definitions for the functionality of RAK14003
const uint8_t LED_0 = 0;      // PA0 (17) of MCP23017
const uint8_t LED_1 = 1;      // PA1 (18) of MCP23017
const uint8_t LED_2 = 2;      // PA2 (19) of MCP23017
const uint8_t LED_3 = 3;      // PA3 (20) of MCP23017
const uint8_t LED_4 = 4;      // PA4 (21) of MCP23017
const uint8_t LED_5 = 5;      // PA5 (22) of MCP23017
const uint8_t LED_6 = 6;      // PA6 (23) of MCP23017
const uint8_t LED_7 = 7;      // PA7 (24) of MCP23017
const uint8_t LED_8 = 8;      // PB0 (25) of MCP23017
const uint8_t LED_9 = 9;      // PB1 (26) of MCP23017

#ifdef RAK4630
#define BOARD "RAK4631 "
#define RAK4631_BOARD true
#else
#define RAK4631_BOARD false
#endif

bool doOTAA = true;                                               // OTAA is used by default.
#define SCHED_MAX_EVENT_DATA_SIZE APP_TIMER_SCHED_EVENT_DATA_SIZE /**< Maximum size of scheduler events. */
#define SCHED_QUEUE_SIZE 60                                       /**< Maximum number of events in the scheduler queue. */
#define LORAWAN_DATERATE DR_0                                     /*LoRaMac datarates definition, from DR_0 to DR_5*/
#define LORAWAN_TX_POWER TX_POWER_5                               /*LoRaMac tx power definition, from TX_POWER_0 to TX_POWER_15*/
#define JOINREQ_NBTRIALS 3                                        /**< Number of trials for the join request. */
DeviceClass_t g_CurrentClass = CLASS_A;                           /* class definition*/
LoRaMacRegion_t g_CurrentRegion = LORAMAC_REGION_US915;           /* Region:EU868*/
lmh_confirm g_CurrentConfirm = LMH_CONFIRMED_MSG;                 /* confirm/unconfirm packet definition*/
uint8_t gAppPort = LORAWAN_APP_PORT;                              /* data port*/

/**@brief Structure containing LoRaWan parameters, needed for lmh_init()
*/
static lmh_param_t g_lora_param_init = { LORAWAN_ADR_ON, LORAWAN_DATERATE, LORAWAN_PUBLIC_NETWORK, JOINREQ_NBTRIALS, LORAWAN_TX_POWER, LORAWAN_DUTYCYCLE_OFF };

// Forward declaration
static void lorawan_has_joined_handler(void);
static void lorawan_join_failed_handler(void);
static void lorawan_rx_handler(lmh_app_data_t *app_data);
static void lorawan_confirm_class_handler(DeviceClass_t Class);
static void send_lora_frame(void);

/**@brief Structure containing LoRaWan callback functions, needed for lmh_init()
*/
static lmh_callback_t g_lora_callbacks = { BoardGetBatteryLevel, BoardGetUniqueId, BoardGetRandomSeed,
                                           lorawan_rx_handler, lorawan_has_joined_handler, lorawan_confirm_class_handler, lorawan_join_failed_handler };
//OTAA keys !!!! KEYS ARE MSB !!!!
uint8_t nodeDeviceEUI[8] = { 0xAC, 0x1F, 0x09, 0xFF, 0xFE, 0x06, 0xD3, 0xE9 };
uint8_t nodeAppEUI[8] = { 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00 };
uint8_t nodeAppKey[16] = { 0xE9, 0x0D, 0x28, 0x1D, 0x92, 0x3D, 0xE4, 0x9F, 0xD9, 0xF7, 0xE0, 0x5F, 0x39, 0x10, 0x55, 0x71 };

// ABP keys
uint32_t nodeDevAddr = 0x260116F8;
uint8_t nodeNwsKey[16] = { 0x7E, 0xAC, 0xE2, 0x55, 0xB8, 0xA5, 0xE2, 0x69, 0x91, 0x51, 0x96, 0x06, 0x47, 0x56, 0x9D, 0x23 };
uint8_t nodeAppsKey[16] = { 0xFB, 0xAC, 0xB6, 0x47, 0xF3, 0x58, 0x45, 0xC7, 0x50, 0x7D, 0xBF, 0x16, 0x8B, 0xA8, 0xC1, 0x7C };

// Private definition
#define LORAWAN_APP_DATA_BUFF_SIZE 64                                            /**< buffer size of the data to be transmitted. */
static uint8_t m_lora_app_data_buffer[LORAWAN_APP_DATA_BUFF_SIZE];               //< Lora user application data buffer.
static lmh_app_data_t m_lora_app_data = { m_lora_app_data_buffer, 0, 0, 0, 0 };  //< Lora user application data structure.

static uint32_t count = 0;
static uint32_t count_fail = 0;

void setup() {

  // Initialize Serial for debug output
	pinMode(LED_BLUE, OUTPUT);
	digitalWrite(LED_BLUE, HIGH);

  // Sensor Power Switch
  pinMode(WB_IO2, OUTPUT);
  digitalWrite(WB_IO2, HIGH);

  // Reset RAK14003 module
  pinMode(WB_IO4, OUTPUT);
  digitalWrite(WB_IO4, HIGH);
  delay(10);
  digitalWrite(WB_IO4, LOW);
  delay(10);
  digitalWrite(WB_IO4, HIGH);
  delay(10);

  // Initialize LoRa chip.
  lora_rak4630_init();

  // Initialize Serial for debug output
  time_t timeout = millis();
  Serial.begin(115200);
  while (!Serial) {
    if ((millis() - timeout) < 5000) {
      delay(100);
    } else {
      break;
    }
  }
  Serial.println("=====================================");
  Serial.println("Welcome to RAK4630 LoRaWan!!!");
  if (doOTAA) {
    Serial.println("Type: OTAA");
  } else {
    Serial.println("Type: ABP");
  }

  switch (g_CurrentRegion) {
    case LORAMAC_REGION_AS923:
      Serial.println("Region: AS923");
      break;
    case LORAMAC_REGION_AU915:
      Serial.println("Region: AU915");
      break;
    case LORAMAC_REGION_CN470:
      Serial.println("Region: CN470");
      break;
    case LORAMAC_REGION_EU433:
      Serial.println("Region: EU433");
      break;
    case LORAMAC_REGION_IN865:
      Serial.println("Region: IN865");
      break;
    case LORAMAC_REGION_EU868:
      Serial.println("Region: EU868");
      break;
    case LORAMAC_REGION_KR920:
      Serial.println("Region: KR920");
      break;
    case LORAMAC_REGION_US915:
      Serial.println("Region: US915");
      break;
  }
  Serial.println("=====================================");

  // Setup the EUIs and Keys
  if (doOTAA) {
    lmh_setDevEui(nodeDeviceEUI);
    lmh_setAppEui(nodeAppEUI);
    lmh_setAppKey(nodeAppKey);
  } else {
    lmh_setNwkSKey(nodeNwsKey);
    lmh_setAppSKey(nodeAppsKey);
    lmh_setDevAddr(nodeDevAddr);
  }

  uint32_t err_code;
  // Initialize LoRaWan
  err_code = lmh_init(&g_lora_callbacks, g_lora_param_init, doOTAA, g_CurrentClass, g_CurrentRegion);
  if (err_code != 0) {
    Serial.printf("lmh_init failed - %d\n", err_code);
    return;
  }

  // Start Join procedure
  lmh_join();

  Serial.println("================================");
  Serial.println("RAK12019 + RAK12010 LoRaWAN Code");
  Serial.println("================================");

  if (!VMEL.begin())
  {
    Serial.println("Sensor not found");
    while (1);
  }

  VMEL.setGain(VEML7700_GAIN_1);
  VMEL.setIntegrationTime(VEML7700_IT_800MS);

  Serial.print(F("Gain: "));
  switch (VMEL.getGain())
  {
    case VEML7700_GAIN_1: Serial.println("1"); break;
    case VEML7700_GAIN_2: Serial.println("2"); break;
    case VEML7700_GAIN_1_4: Serial.println("1/4"); break;
    case VEML7700_GAIN_1_8: Serial.println("1/8"); break;
  }

  Serial.print(F("Integration Time (ms): "));
  switch (VMEL.getIntegrationTime())
  {
    case VEML7700_IT_25MS: Serial.println("25"); break;
    case VEML7700_IT_50MS: Serial.println("50"); break;
    case VEML7700_IT_100MS: Serial.println("100"); break;
    case VEML7700_IT_200MS: Serial.println("200"); break;
    case VEML7700_IT_400MS: Serial.println("400"); break;
    case VEML7700_IT_800MS: Serial.println("800"); break;
  }

	Serial.println("RAK12019 test");
	Wire.begin();
	if (!ltr.init())
	{
		Serial.println("Couldn't find LTR sensor!");
		while (1)
			delay(10);
	}
	Serial.println("Found LTR390 sensor!");

	//set to LTR390_MODE_UVS,get ultraviolet light data.
  ltr.setMode(LTR390_MODE_UVS);  // UVS Mode

	Serial.println("In UVS mode");

	ltr.setGain(LTR390_GAIN_3);
	Serial.print("Gain : ");
	switch (ltr.getGain())
	{
	case LTR390_GAIN_1:
		Serial.println(1);
		break;
	case LTR390_GAIN_3:
		Serial.println(3);
		break;
	case LTR390_GAIN_6:
		Serial.println(6);
		break;
	case LTR390_GAIN_9:
		Serial.println(9);
		break;
	case LTR390_GAIN_18:
		Serial.println(18);
		break;
	default:
		Serial.println("Failed to set gain");
		break;
	}
	ltr.setResolution(LTR390_RESOLUTION_16BIT);
	Serial.print("Integration Time (ms): ");
	switch (ltr.getResolution())
	{
	case LTR390_RESOLUTION_13BIT:
		Serial.println(13);
		break;
	case LTR390_RESOLUTION_16BIT:
		Serial.println(16);
		break;
	case LTR390_RESOLUTION_17BIT:
		Serial.println(17);
		break;
	case LTR390_RESOLUTION_18BIT:
		Serial.println(18);
		break;
	case LTR390_RESOLUTION_19BIT:
		Serial.println(19);
		break;
	case LTR390_RESOLUTION_20BIT:
		Serial.println(20);
		break;
	default:
		Serial.println("Failed to set Integration Time");
		break;
	}

	ltr.setThresholds(100, 1000); //Set the interrupt output threshold range for lower and upper.

  ltr.configInterrupt(true, LTR390_MODE_UVS);

  // For RAK14003
  mcp.begin_I2C(0x24);

  // Added for the functionality of RAK14003

  Wire.begin();    // initialize I2C serial bus

  // Configuration of MCP23017 I/O ports
  mcp.pinMode(LED_0, OUTPUT);     // Red LED; Top most
  mcp.pinMode(LED_1, OUTPUT);     // Red LED
  mcp.pinMode(LED_2, OUTPUT);     // Orange LED
  mcp.pinMode(LED_3, OUTPUT);     // Orange LED
  mcp.pinMode(LED_4, OUTPUT);     // Orange LED
  mcp.pinMode(LED_5, OUTPUT);     // Green LED
  mcp.pinMode(LED_6, OUTPUT);     // Green LED
  mcp.pinMode(LED_7, OUTPUT);     // Green LED
  mcp.pinMode(LED_8, OUTPUT);     // Green LED
  mcp.pinMode(LED_9, OUTPUT);     // Green LED; Bottom

  // Initially Turn OFF all LEDs
  mcp.digitalWrite(LED_0, HIGH);
  mcp.digitalWrite(LED_1, HIGH);
  mcp.digitalWrite(LED_2, HIGH);
  mcp.digitalWrite(LED_3, HIGH);
  mcp.digitalWrite(LED_4, HIGH);
  mcp.digitalWrite(LED_5, HIGH);
  mcp.digitalWrite(LED_6, HIGH);
  mcp.digitalWrite(LED_7, HIGH);
  mcp.digitalWrite(LED_8, HIGH);
  mcp.digitalWrite(LED_9, HIGH);

}

void loop() {
  // Put your application tasks here, like reading of sensors,
  // Controlling actuators and/or other functions.

  // Trial # 1
  // Data from RAK12019
  if (ltr.newDataAvailable())
  {
    uvi = ltr.getUVI();
    uvs = ltr.readUVS();
  }

  // Data from RAK12010
  lux = VMEL.readLux();
  white = VMEL.readWhite();
  raw_als = VMEL.readALS();

  Serial.println("Sending frame now...");
  send_lora_frame();

  // Showing only UV Index (uvi), UV Intensity (uvs) and Lux (lx)

  // From RAK12019 module
  Serial.print("UVI: ");
  Serial.println(uvi);          // Uvi data from RAK12019
  Serial.print("UVS: ");
  Serial.println(uvs);            // Uvs data from RAK12019

  // From RAK12010
  Serial.print("Lux: ");
  Serial.print(lux);
  Serial.println(" lx ");
  Serial.print("White: ");
  Serial.println(white);
  Serial.print("Raw ALS: ");
  Serial.println(raw_als);

  // Result of uvi to be displayed via RAK14003 module
  if (uvi <= 0.4)
  {
    mcp.digitalWrite(LED_0, HIGH);
    mcp.digitalWrite(LED_1, HIGH);
    mcp.digitalWrite(LED_2, HIGH);
    mcp.digitalWrite(LED_3, HIGH);
    mcp.digitalWrite(LED_4, HIGH);
    mcp.digitalWrite(LED_5, HIGH);
    mcp.digitalWrite(LED_6, HIGH);
    mcp.digitalWrite(LED_7, HIGH);
    mcp.digitalWrite(LED_8, HIGH);
    mcp.digitalWrite(LED_9, HIGH);
  }

  else if (uvi > 0.5 && uvi <= 1)
  {
    mcp.digitalWrite(LED_0, HIGH);
    mcp.digitalWrite(LED_1, HIGH);
    mcp.digitalWrite(LED_2, HIGH);
    mcp.digitalWrite(LED_3, HIGH);
    mcp.digitalWrite(LED_4, HIGH);
    mcp.digitalWrite(LED_5, HIGH);
    mcp.digitalWrite(LED_6, HIGH);
    mcp.digitalWrite(LED_7, HIGH);
    mcp.digitalWrite(LED_8, HIGH);
    mcp.digitalWrite(LED_9, LOW);
  }

  else if (uvi > 1.5 && uvi <= 2)
  {
    mcp.digitalWrite(LED_0, HIGH);
    mcp.digitalWrite(LED_1, HIGH);
    mcp.digitalWrite(LED_2, HIGH);
    mcp.digitalWrite(LED_3, HIGH);
    mcp.digitalWrite(LED_4, HIGH);
    mcp.digitalWrite(LED_5, HIGH);
    mcp.digitalWrite(LED_6, HIGH);
    mcp.digitalWrite(LED_7, HIGH);
    mcp.digitalWrite(LED_8, LOW);
    mcp.digitalWrite(LED_9, LOW);
  }

  else if (uvi > 2.5 && uvi <= 3)
  {
    mcp.digitalWrite(LED_0, HIGH);
    mcp.digitalWrite(LED_1, HIGH);
    mcp.digitalWrite(LED_2, HIGH);
    mcp.digitalWrite(LED_3, HIGH);
    mcp.digitalWrite(LED_4, HIGH);
    mcp.digitalWrite(LED_5, HIGH);
    mcp.digitalWrite(LED_6, HIGH);
    mcp.digitalWrite(LED_7, LOW);
    mcp.digitalWrite(LED_8, LOW);
    mcp.digitalWrite(LED_9, LOW);
  }

  else if (uvi > 3.5 && uvi <= 4)
  {
    mcp.digitalWrite(LED_0, HIGH);
    mcp.digitalWrite(LED_1, HIGH);
    mcp.digitalWrite(LED_2, HIGH);
    mcp.digitalWrite(LED_3, HIGH);
    mcp.digitalWrite(LED_4, HIGH);
    mcp.digitalWrite(LED_5, HIGH);
    mcp.digitalWrite(LED_6, LOW);
    mcp.digitalWrite(LED_7, LOW);
    mcp.digitalWrite(LED_8, LOW);
    mcp.digitalWrite(LED_9, LOW);
  }

  else if (uvi > 4.5 && uvi <= 5)
  {
    mcp.digitalWrite(LED_0, HIGH);
    mcp.digitalWrite(LED_1, HIGH);
    mcp.digitalWrite(LED_2, HIGH);
    mcp.digitalWrite(LED_3, HIGH);
    mcp.digitalWrite(LED_4, HIGH);
    mcp.digitalWrite(LED_5, LOW);
    mcp.digitalWrite(LED_6, LOW);
    mcp.digitalWrite(LED_7, LOW);
    mcp.digitalWrite(LED_8, LOW);
    mcp.digitalWrite(LED_9, LOW);
  }

  else if (uvi > 5.5 && uvi <= 6)
  {
    mcp.digitalWrite(LED_0, HIGH);
    mcp.digitalWrite(LED_1, HIGH);
    mcp.digitalWrite(LED_2, HIGH);
    mcp.digitalWrite(LED_3, HIGH);
    mcp.digitalWrite(LED_4, LOW);
    mcp.digitalWrite(LED_5, LOW);
    mcp.digitalWrite(LED_6, LOW);
    mcp.digitalWrite(LED_7, LOW);
    mcp.digitalWrite(LED_8, LOW);
    mcp.digitalWrite(LED_9, LOW);
  }

  else if (uvi > 6.5 && uvi <= 7)
  {
    mcp.digitalWrite(LED_0, HIGH);
    mcp.digitalWrite(LED_1, HIGH);
    mcp.digitalWrite(LED_2, HIGH);
    mcp.digitalWrite(LED_3, LOW);
    mcp.digitalWrite(LED_4, LOW);
    mcp.digitalWrite(LED_5, LOW);
    mcp.digitalWrite(LED_6, LOW);
    mcp.digitalWrite(LED_7, LOW);
    mcp.digitalWrite(LED_8, LOW);
    mcp.digitalWrite(LED_9, LOW);
  }

  else if (uvi > 7.5 && uvi <= 8)
  {
    mcp.digitalWrite(LED_0, HIGH);
    mcp.digitalWrite(LED_1, HIGH);
    mcp.digitalWrite(LED_2, LOW);
    mcp.digitalWrite(LED_3, LOW);
    mcp.digitalWrite(LED_4, LOW);
    mcp.digitalWrite(LED_5, LOW);
    mcp.digitalWrite(LED_6, LOW);
    mcp.digitalWrite(LED_7, LOW);
    mcp.digitalWrite(LED_8, LOW);
    mcp.digitalWrite(LED_9, LOW);
  }

  else if (uvi > 8.5 && uvi <= 9.5)
  {
    mcp.digitalWrite(LED_0, HIGH);
    mcp.digitalWrite(LED_1, LOW);
    mcp.digitalWrite(LED_2, LOW);
    mcp.digitalWrite(LED_3, LOW);
    mcp.digitalWrite(LED_4, LOW);
    mcp.digitalWrite(LED_5, LOW);
    mcp.digitalWrite(LED_6, LOW);
    mcp.digitalWrite(LED_7, LOW);
    mcp.digitalWrite(LED_8, LOW);
    mcp.digitalWrite(LED_9, LOW);
  }

  else if (uvi >= 10)
  {
    mcp.digitalWrite(LED_0, LOW);
    mcp.digitalWrite(LED_1, LOW);
    mcp.digitalWrite(LED_2, LOW);
    mcp.digitalWrite(LED_3, LOW);
    mcp.digitalWrite(LED_4, LOW);
    mcp.digitalWrite(LED_5, LOW);
    mcp.digitalWrite(LED_6, LOW);
    mcp.digitalWrite(LED_7, LOW);
    mcp.digitalWrite(LED_8, LOW);
    mcp.digitalWrite(LED_9, LOW);
  }

  delay(10000);
}

/**@brief LoRa function for handling HasJoined event.
 */
void lorawan_has_joined_handler(void) {
  Serial.println("OTAA Mode, Network Joined!");
}

/**@brief LoRa function for handling OTAA join failed
*/
static void lorawan_join_failed_handler(void) {
  Serial.println("OTAA join failed!");
  Serial.println("Check your EUI's and Keys's!");
  Serial.println("Check if a Gateway is in range!");
}
/**@brief Function for handling LoRaWan received data from Gateway
 *
 * @param[in] app_data  Pointer to rx data
 */
void lorawan_rx_handler(lmh_app_data_t *app_data) {
  Serial.printf("LoRa Packet received on port %d, size:%d, rssi:%d, snr:%d, data:%s\n",
                app_data->port, app_data->buffsize, app_data->rssi, app_data->snr, app_data->buffer);
}

void lorawan_confirm_class_handler(DeviceClass_t Class) {
  Serial.printf("switch to class %c done\n", "ABC"[Class]);
  // Informs the server that switch has occurred ASAP
  m_lora_app_data.buffsize = 0;
  m_lora_app_data.port = gAppPort;
  lmh_send(&m_lora_app_data, g_CurrentConfirm);
}

String data = "";

void send_lora_frame(void) {
  if (lmh_join_status_get() != LMH_SET) {
    //Not joined, try again later
    return;
  }

  Serial.print("result: ");
  uint32_t i = 0;
  memset(m_lora_app_data.buffer, 0, LORAWAN_APP_DATA_BUFF_SIZE);
  m_lora_app_data.port = gAppPort;

  // Showing only UV Index (uvi), UV Intensity (uvs) and Lux (lx)
  data = " Uvi Data: " + String(uvi) + " Uvs Data: " + String(uvs) + " Lux Data: " + String(lux) + " lx " ;

  Serial.println(data);

  // Showing only UV Index (uvi), UV Intensity (uvs) and Lux (lx)
  uint16_t uvi_data = uvi;            // Uvi data from RAK12019
  uint32_t uvs_data = uvs;            // Uvs data from RAK12019
  uint32_t lux_data = lux;            // Lux data from RAK12010

  m_lora_app_data.buffer[i++] = 0x01;  // byte[0]

  // Showing only UV Index (uvi), UV Intensity (uvs) and Lux (lx)
  // Data from RAK12019 module
  m_lora_app_data.buffer[i++] = (uint8_t)((uvi_data & 0x0000FF00) >> 8);     // byte[1]
  m_lora_app_data.buffer[i++] = (uint8_t)(uvi_data & 0x000000FF);            // byte[2]

  // Data from RAK12019 module
  m_lora_app_data.buffer[i++] = (uint8_t)((uvs_data & 0xFF000000) >> 24);    // byte[3]
  m_lora_app_data.buffer[i++] = (uint8_t)((uvs_data & 0x00FF0000) >> 16);    // byte[4]
  m_lora_app_data.buffer[i++] = (uint8_t)((uvs_data & 0x0000FF00) >> 8);     // byte[5]
  m_lora_app_data.buffer[i++] = (uint8_t)(uvs_data & 0x000000FF);            // byte[6]

  // Data from RAK12010 module
  m_lora_app_data.buffer[i++] = (uint8_t)((lux_data & 0xFF000000) >> 24);    // byte[7]
  m_lora_app_data.buffer[i++] = (uint8_t)((lux_data & 0x00FF0000) >> 16);    // byte[8]
  m_lora_app_data.buffer[i++] = (uint8_t)((lux_data & 0x0000FF00) >> 8);     // byte[9]
  m_lora_app_data.buffer[i++] = (uint8_t)(lux_data & 0x000000FF);            // byte[10]

  m_lora_app_data.buffsize = i;

  lmh_error_status error = lmh_send(&m_lora_app_data, g_CurrentConfirm);
  if (error == LMH_SUCCESS) {
    count++;
    Serial.printf("lmh_send ok count %d\n", count);
  } else {
    count_fail++;
    Serial.printf("lmh_send fail count %d\n", count_fail);
  }
}
```
:::

Before uploading the Arduino Code, there are configurations that you need to set up to ensure that the device can join a LoRaWAN Network server. The steps below will explain the default settings and how to configure them.

- Set up the LoRaWAN region. The **LORAMAC_REGION** can be any of your desired region to work with. You can change this to a region that is applicable to you like `LORAMAC_REGION_US915`, `LORAMAC_REGION_AU915`, etc. Below is the table of LoRaWAN regions and their respective countries where they are used in:

|     LoRaWAN Region      |                               Usage                                  |
| ----------------------- | -------------------------------------------------------------------- |
| LORAMAC_REGION_AS923-1  | Australia, Singapore, Solomon Islands, Sri-Lanka, Taiwan             |
| LORAMAC_REGION_AS923-2  | Vietnam                                                              |
| LORAMAC_REGION_AS923-3  | Philippines, Albania, Algeria, Denmark, Greenland, Jordan            |
| LORAMAC_REGION_AS923-4  | Israel                                                               |
| LORAMAC_REGION_AU915    | Australia, Anguilla, Argentina, and many parts of South America      |
| LORAMAC_REGION_CN470    | China                                                                |
| LORAMAC_REGION_EU433    | EU, UK, Brazil, Costa Rica, Cuba, and many parts of Africa           |
| LORAMAC_REGION_IN865    | India, Cook Islands, Egypt, Hong Kong, Jordan, New Zealand, Niger    |
| LORAMAC_REGION_EU868    | EU, UK and many parts of Africa                                      |
| LORAMAC_REGION_KR920    | Republic of Korea                                                    |
| LORAMAC_REGION_US915    | USA                                                                  |
| LORAMAC_REGION_RU864    | Russia                                                               |

```c
LoRaMacRegion_t g_CurrentRegion = LORAMAC_REGION_US915;    /* Region:US915*/
```
- Set up the LoRaWAN activation method. In this case, we will be using the **OTAA** configuration which is also the default from the given code.

```c
bool doOTAA = true;   // OTAA is used by default.
```

- Set up the message type if confirmed or not. **Confirmed message** is the default for this one. You can change to an **unconfirmed message** by changing the value to `LMH_UNCONFIRMED_MSG`.

```c
lmh_confirm g_CurrentConfirm = LMH_CONFIRMED_MSG;         /* confirm/unconfirm packet definition*/
```

- Set the device to **Class A**.

```c
DeviceClass_t g_CurrentClass = CLASS_A;         /* class definition*/
```

- Setup the EUIs and KEY. The **DeviceEUI**, **AppEUI** and **AppKey** are the credentials of your device registered to TTN that will be used for the OTAA keys in the code. You need to replace the ones in the code with the credentials registered in TTN.

```c

//OTAA keys !!!! KEYS ARE MSB !!!!
uint8_t nodeDeviceEUI[8] = { 0xAC, 0x1F, 0x09, 0xFF, 0xFE, 0x06, 0xD3, 0xE9 };
uint8_t nodeAppEUI[8] = { 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00 };
uint8_t nodeAppKey[16] = { 0xE9, 0x0D, 0x28, 0x1D, 0x92, 0x3D, 0xE4, 0x9F, 0xD9, 0xF7, 0xE0, 0x5F, 0x39, 0x10, 0x55, 0x71 };

```

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_21.png"
  width="90%"
  caption="OTAA device successfully registered to TTN"
/>

3. Once done with the code, you can now proceed uploading it into your device. You need to select first your RAK4631 board from desktop or laptop. To do this, go to **Tools** > **Board:XXXXX** > **RAKwireless nRF Boards** > **WisBlock RAK4631**. After you selected your board, you need to select the specific port of your board. To do this, go to **Tools** > **Port** > then the specific port of your board.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12019_1.png"
  width="90%"
  caption="Selecting the RAK4631 board"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12019_2.png"
  width="90%"
  caption="Selecting the port of RAK4631 board"
/>

4. Once done, you can now upload your code. Simply click the right arrow sign at the upper left portion of your Arduino IDE. Once done, you will see the **Device programmed** notification at the bottom part of your Arduino IDE.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12019_3.png"
  width="90%"
  caption="Uploading your code into your RAK4631 board"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12019_4.png"
  width="90%"
  caption="Arduino code is successfully uploaded into your RAK4631 board"
/>

###### UV Index & UV Intensity Monitoring via TTN

1. To monitor the data of your **UV Index & UV Intensity Monitoring** device via **TTN**, you need to go back to your TTN account where you created your application and registered your device.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12019_5.png"
  width="90%"
  caption="Your UV Index & UV Intensity Monitoring device in TTN"
/>

2. Then go to **Payload formatters**. Under **Formatter type**, select **Custom Javascript formatter**. Then under the **Formatter code**, you need to replace the default code with the one below. This will decode the data from your device going to **TTN**. Once done, simply click **Save changes**.

```c
// LoRaWAN code for RAK12019 + RAK12010 Application

function Decoder(bytes, port)
{

  var decoded = {};

  if (port === 2)
  {
    if( bytes[0] == 1) // check if the header byte is 1.
    {
      uvi_data = (bytes[1] << 8) | (bytes[2]);
      uvs_data = (bytes[3] << 24) | (bytes[4] << 16) | (bytes[5] << 8) | (bytes[6]);
      lux_data = (bytes[7] << 24) | (bytes[8] << 16) | (bytes[9] << 8) | (bytes[10]);

      decoded.uvi = uvi_data;
      decoded.uvs = uvs_data;
      decoded.lux = lux_data;

      return decoded;
    }
  }
}
```

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12019_6.png"
  width="90%"
  caption="Payload Formatter"
/>

3. Then go back to **Live data** of your device in TTN and compare it with the live data from the **Serial Monitor** of your device. You should now seeing identical results between them.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12019_7.png"
  width="90%"
  caption="Live data from your device in TTN"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12019_8.png"
  width="90%"
  caption="Live data from your device in its Serial Monitor"
/>

###### UV Index & UV Intensity Monitoring via Qubitro

This section will guide you on how to integrate your application using Qubitro.

1. Go to [Qubitro Portal](https://portal.qubitro.com/login) and create your account.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_1.png"
  width="80%"
  caption="Creating Qubitro Account"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_2.png"
  width="80%"
  caption="Creating Qubitro Account"
/>

2. Once done with the account creation, login into your **Qubitro Account**. Then click **New Project**, then fill out your desired **Name**, as well as the **Description** based on your battery monitoring application, then click **Create**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_3.png"
  width="80%"
  caption="Creating New Project"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_4.png"
  width="80%"
  caption="Creating New Project"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_5.png"
  width="80%"
  caption="Created New Project"
/>

3. Then click into your newly-created project then click **New source**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_6.png"
  width="80%"
  caption="Adding New source"
/>

4. Among the data sources, choose **The Things Stack**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_7.png"
  width="80%"
  caption="Choosing The Things Stack"
/>

5. For the **integration type**, choose **Import from network**, then copy and paste the **PROJECT ID** and **WEBHOOK SIGNING KEY** temporarily to notepad. These credentials will be used on the later part, then click **Go to project**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_8.png"
  width="80%"
  caption="Copying the credentials"
/>

6. Then head back to your **TTN Application** where you created your battery monitoring application to add webhook from it. To do this, just click your device then go to **Integrations** > **Webhooks** > **+ Add webhook**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_9.png"
  width="80%"
  caption="Going to your TTN application for your UV Monitoring Application"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_10.png"
  width="80%"
  caption="Adding Webhook"
/>

7. Then choose **Qubitro** as your webhook template.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_11.png"
  width="80%"
  caption="Qubitro"
/>

8. Then fill in the needed details:
   - **Webhook ID** - For this example, you can use **uv-monitoring-application**.
   - **Project ID** - Paste the credential you copied from **Step 5**.
   - **Webhook Signing Key** - Paste the credential you copied from **Step 5**.

   Then click **Create Qubitro webhook**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_12.png"
  width="80%"
  caption="Creating Qubitro webhook"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_13.png"
  width="80%"
  caption="Added a Qubitro webhook"
/>

9. After you created your webhook, go back to your **Qubitro** platform to check the changes made. Refresh **Qubitro** by clicking the **Refresh** button on the upper right side of your screen. You will notice that a newly-added device is included in the platform.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_14.png"
  width="80%"
  caption="Device successfully included in Qubitro"
/>

10. To add the decoder, simply go to **Functions** > **Create Function**. Then under **Decoder Function**, click **Get started**. You will be now routed to **Function Configuration**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_15.png"
  width="80%"
  caption="Creating Function"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_16.png"
  width="80%"
  caption="Decoder Function"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_17.png"
  width="80%"
  caption="Function Configuration"
/>

11. Under the **Formatter type**, choose **Custom Javascript formatter**. Then under the **Formatter code**, you need to replace its default entry with the code below:

```c
// LoRaWAN code for RAK12019 + RAK12010 Application

function Decoder(bytes, port)
{

  var decoded = {};

  if (port === 2)
  {
    if (bytes[0] == 1) // check if the header byte is 1.
    {
      uvi_data = (bytes[1] << 8) | (bytes[2]);
      uvs_data = (bytes[3] << 24) | (bytes[4] << 16) | (bytes[5] << 8) | (bytes[6]);
      lux_data = (bytes[7] << 24) | (bytes[8] << 16) | (bytes[9] << 8) | (bytes[10]);

      decoded.uvi = uvi_data;
      decoded.uvs = uvs_data;
      decoded.lux = lux_data;

      return decoded;
    }
  }
}
```

Once done, simply click **Save and complete**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_18.png"
  width="80%"
  caption="Function Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_19.png"
  width="80%"
  caption="Created Decoder Function"
/>

12. Then go to your device and click on the **Data** tab to check for the incoming data coming from your device. You should now be seeing live data from your device. To gather the most recent data, simply click **Refresh**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_20.png"
  width="80%"
  caption="Data Tab"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_21.png"
  width="80%"
  caption="Historical Data"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_22.png"
  width="80%"
  caption="Refreshing data to get newer ones"
/>

13. To add a monitoring dashboard for the data from the UV monitoring device, you need to go to **Home** which is located at the left top most part of your screen. Then click **Dashboards** > **New dashboard** > **Create new**. Then fill out the **Create New Dashboard** portion using the details of your device. For the **Tags**, just simply input **Test** then click **Create**. Once done, click on to your newly-created dashboard.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_23.png"
  width="80%"
  caption="Creating dashboard for your UV Monitoring device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_24.png"
  width="80%"
  caption="Creating dashboard for your UV Monitoring device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_25.png"
  width="80%"
  caption="Creating dashboard for your UV Monitoring device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_26.png"
  width="80%"
  caption="Creating dashboard for your UV Monitoring device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_27.png"
  width="80%"
  caption="Newly-created dashboard for your UV Monitoring device"
/>

14. Click **Edit** > **New widget** to add a widget for a specific parameter need to be monitored.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_28.png"
  width="80%"
  caption="Adding a widget"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_29.png"
  width="80%"
  caption="Adding a widget"
/>

15. Once done, you're now at the **Widget Configuration**. At the **WIDGET TYPE**, choose **Chart**. Then provide the name of the parameter under **SHOW WIDGET NAME**. Once done, proceed to **Add point +**. Choose your **existing project**, **application** and the **specific parameter** you need to monitor in your dashboard. Once done, just click **Save**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_30.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_31.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_32.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_33.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_34.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_35.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_36.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_37.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_38.png"
  width="100%"
  caption="Connect Data Point"
/>

16. Now you have an existing preview of your data from your device. Under **CHART TYPE** at the left side of your screen, choose **Line**. Once done, go to **STANDARD OPTIONS** to choose the appropriate unit for your parameter to be monitored in the dashboard. Once done, click **Save widget**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_39.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_40.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_41.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_42.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_43.png"
  width="100%"
  caption="Saving the changes made in your Widget Configuration"
/>

17. Then click **Save changes** to include the data of parameter. Then you have now the newly-made widget for your specific parameter.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_44.png"
  width="100%"
  caption="Save changes"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_45.png"
  width="100%"
  caption="Newly-made widget"
/>

18. In able for you to include additional widgets for other parameters, you need to click **Edit** > **New widget** then repeat **Step 15** to **Step 17**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_46.png"
  width="100%"
  caption="Adding widgets into your dashboard"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_47.png"
  width="100%"
  caption="Adding widgets into your dashboard"
/>

19. Then there you have it a real-time monitoring dashboard for your UV monitoring device.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Qub_48.png"
  width="100%"
  caption="Monitoring dashboard for your UV monitoring device"
/>

[Back](#lorawan-applications-for-wisblock-iot-education-kit-light-color-using-ttn-and-qubitro)

##### Light Color Recognizer LoRaWAN Application

The **Light Color Recognizer LoRaWAN Application** is used to evaluate the color of the light being monitored using an RGB sensor. It uses **RAK12021** which is an RGB sensor which is based on **TCS37725FN** from AMS. It also uses **RAK14001** RGB LED module which will visualize the color being monitored by **RAK12021** module.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Light.png"
  width="85%"
  caption="Light Color Recognizer device"
/>

###### Light Color Recognizer - TTN Registration Section and Device Registration

1. If you already have an existing TTN account, you may proceed to the next steps. If you haven't created any TTN account, please refer to this [link](#ttn-account-creation) to create one.

2. Once done with the TTN account creation, you may now proceed with the device registration. Please refer to this [guide](#device-registration) for your reference. After creating the application and adding the device in TTN, you can proceed on the LoRaWAN Code uploading steps.

###### LoRaWAN Code for Light Color Recognizer

1. If you already have **Arduino IDE** installed to your laptop or PC and added **RAK4631 board** into it, you may proceed to the next step. If you haven't yet installed the **Arduino IDE**, please refer to this [link](#arduino-ide-installation-rak4631) for the steps.

2. After the installation, you can now proceed programming your **Light Color Recognizer** device. Just copy the code below for **Light Color Recognizer LoRaWAN Application** and paste it into the **Arduino IDE**.

::: tip 📝 NOTE

The example code uses [SX126x-Arduino](https://github.com/beegee-tokyo/SX126x-Arduino) library which needs to be added to successfully compile the LoRaWAN code.

:::

::: details Click Here to View Example Code
```c
#include <Arduino.h>
#include <LoRaWan-RAK4630.h>  //http://librarymanager/All#SX126x
#include <Wire.h>
#include <NCP5623.h>	//http://librarymanager/All#NCP5623 By:RAKWireless
#include "TCS3772.h"  // Click here to get the library: http://librarymanager/All#TCS37725
// It use WB_IO2 to power up and is conflicting with INT1, so better use in SlotA/SlotC/SlotD.

NCP5623 rgb;
TCS3772 tcs3772;
TCS3772_DataScaled tcs3772_data = {0};

uint16_t scale_factor;

uint16_t redColor;
uint16_t greenColor;
uint16_t blueColor;

#ifdef RAK4630
#define BOARD "RAK4631 "
#define RAK4631_BOARD true
#else
#define RAK4631_BOARD false
#endif

bool doOTAA = true;                                               // OTAA is used by default.
#define SCHED_MAX_EVENT_DATA_SIZE APP_TIMER_SCHED_EVENT_DATA_SIZE /**< Maximum size of scheduler events. */
#define SCHED_QUEUE_SIZE 60                                       /**< Maximum number of events in the scheduler queue. */
#define LORAWAN_DATERATE DR_0                                     /*LoRaMac datarates definition, from DR_0 to DR_5*/
#define LORAWAN_TX_POWER TX_POWER_5                               /*LoRaMac tx power definition, from TX_POWER_0 to TX_POWER_15*/
#define JOINREQ_NBTRIALS 3                                        /**< Number of trials for the join request. */
DeviceClass_t g_CurrentClass = CLASS_A;                           /* class definition*/
LoRaMacRegion_t g_CurrentRegion = LORAMAC_REGION_US915;           /* Region:EU868*/
lmh_confirm g_CurrentConfirm = LMH_CONFIRMED_MSG;                 /* confirm/unconfirm packet definition*/
uint8_t gAppPort = LORAWAN_APP_PORT;                              /* data port*/

/**@brief Structure containing LoRaWan parameters, needed for lmh_init()
*/
static lmh_param_t g_lora_param_init = { LORAWAN_ADR_ON, LORAWAN_DATERATE, LORAWAN_PUBLIC_NETWORK, JOINREQ_NBTRIALS, LORAWAN_TX_POWER, LORAWAN_DUTYCYCLE_OFF };

// Forward declaration
static void lorawan_has_joined_handler(void);
static void lorawan_join_failed_handler(void);
static void lorawan_rx_handler(lmh_app_data_t *app_data);
static void lorawan_confirm_class_handler(DeviceClass_t Class);
static void send_lora_frame(void);

/**@brief Structure containing LoRaWan callback functions, needed for lmh_init()
*/
static lmh_callback_t g_lora_callbacks = { BoardGetBatteryLevel, BoardGetUniqueId, BoardGetRandomSeed,
                                           lorawan_rx_handler, lorawan_has_joined_handler, lorawan_confirm_class_handler, lorawan_join_failed_handler };
//OTAA keys !!!! KEYS ARE MSB !!!!
uint8_t nodeDeviceEUI[8] = { 0xAC, 0x1F, 0x09, 0xFF, 0xFE, 0x05, 0x3E, 0x3E };
uint8_t nodeAppEUI[8] = { 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00 };
uint8_t nodeAppKey[16] = { 0x96, 0xBD, 0xC5, 0x98, 0x17, 0x69, 0x8D, 0xFA, 0x1F, 0x64, 0xFE, 0x1C, 0xF9, 0x26, 0x7F, 0x8D };

// ABP keys
uint32_t nodeDevAddr = 0x260116F8;
uint8_t nodeNwsKey[16] = { 0x7E, 0xAC, 0xE2, 0x55, 0xB8, 0xA5, 0xE2, 0x69, 0x91, 0x51, 0x96, 0x06, 0x47, 0x56, 0x9D, 0x23 };
uint8_t nodeAppsKey[16] = { 0xFB, 0xAC, 0xB6, 0x47, 0xF3, 0x58, 0x45, 0xC7, 0x50, 0x7D, 0xBF, 0x16, 0x8B, 0xA8, 0xC1, 0x7C };

// Private definition
#define LORAWAN_APP_DATA_BUFF_SIZE 64                                            /**< buffer size of the data to be transmitted. */
static uint8_t m_lora_app_data_buffer[LORAWAN_APP_DATA_BUFF_SIZE];               //< Lora user application data buffer.
static lmh_app_data_t m_lora_app_data = { m_lora_app_data_buffer, 0, 0, 0, 0 };  //< Lora user application data structure.

static uint32_t count = 0;
static uint32_t count_fail = 0;

void setup() {

  // Initialize Serial for debug output
	pinMode(LED_BLUE, OUTPUT);
	digitalWrite(LED_BLUE, HIGH);

  // Sensor Power Switch
  pinMode(WB_IO2, OUTPUT);
  digitalWrite(WB_IO2, HIGH);

  // enable RAK14001
  pinMode(WB_IO6, OUTPUT);
  digitalWrite(WB_IO6, HIGH);

  // Initialize LoRa chip.
  lora_rak4630_init();

  // Initialize Serial for debug output
  time_t timeout = millis();
  Serial.begin(115200);
  while (!Serial) {
    if ((millis() - timeout) < 5000) {
      delay(100);
    } else {
      break;
    }
  }
  Serial.println("=====================================");
  Serial.println("Welcome to RAK4630 LoRaWan!!!");
  if (doOTAA) {
    Serial.println("Type: OTAA");
  } else {
    Serial.println("Type: ABP");
  }

  switch (g_CurrentRegion) {
    case LORAMAC_REGION_AS923:
      Serial.println("Region: AS923");
      break;
    case LORAMAC_REGION_AU915:
      Serial.println("Region: AU915");
      break;
    case LORAMAC_REGION_CN470:
      Serial.println("Region: CN470");
      break;
    case LORAMAC_REGION_EU433:
      Serial.println("Region: EU433");
      break;
    case LORAMAC_REGION_IN865:
      Serial.println("Region: IN865");
      break;
    case LORAMAC_REGION_EU868:
      Serial.println("Region: EU868");
      break;
    case LORAMAC_REGION_KR920:
      Serial.println("Region: KR920");
      break;
    case LORAMAC_REGION_US915:
      Serial.println("Region: US915");
      break;
  }
  Serial.println("=====================================");

  // Setup the EUIs and Keys
  if (doOTAA) {
    lmh_setDevEui(nodeDeviceEUI);
    lmh_setAppEui(nodeAppEUI);
    lmh_setAppKey(nodeAppKey);
  } else {
    lmh_setNwkSKey(nodeNwsKey);
    lmh_setAppSKey(nodeAppsKey);
    lmh_setDevAddr(nodeDevAddr);
  }

  uint32_t err_code;
  // Initialize LoRaWan
  err_code = lmh_init(&g_lora_callbacks, g_lora_param_init, doOTAA, g_CurrentClass, g_CurrentRegion);
  if (err_code != 0) {
    Serial.printf("lmh_init failed - %d\n", err_code);
    return;
  }

  // Start Join procedure
  lmh_join();

  Serial.println("================================");
  Serial.println("RAK12021 + RAK14001 LoRaWAN Code");
  Serial.println("================================");

  // If using Native I2C
  Wire.begin();
  Wire.setClock(100000);

  // Serial.println("RAK14001 + RAK12021");

  if (!rgb.begin())
  {
    Serial.println("RAK14001 not found on the I2C line");
    while (1);
  }
  else
  {
    Serial.println("RAK14001 Found. Begining execution");
  }

  // set the current output level max, the range is 1 to 31
  rgb.setCurrent(25);

  if(tcs3772.begin() == true)
  {
    Serial.println("Found sensor.");
  }
  else
  {
    Serial.println("TCS37725 not found ... check your connections.");
    while(1)
    {
      delay(10);
    }
  }
  delay(1000);
}

void loop() {
  // Put your application tasks here, like reading of sensors,
  // Controlling actuators and/or other functions.

  tcs3772_data = tcs3772.getMeasurement();

  scale_factor = tcs3772.autoGain(tcs3772_data.clear);

  redColor = tcs3772_data.red;
  greenColor = tcs3772_data.green;
  blueColor = tcs3772_data.blue;

  rgb.setColor(0,0,0);     // Initially OFF

  Serial.println("Sending frame now...");
  send_lora_frame();

  Serial.print("  R: ");
  Serial.println(redColor);
  Serial.print("  G: ");
  Serial.println(greenColor);
  Serial.print("  B: ");
  Serial.println(blueColor);

  // The values of redColor, greenColor and blueColor can be varied during the sensing calibration of RAK12021 module

  if (((redColor >= 9000) && (redColor <= 65535)) && ((greenColor >= 10000) && (greenColor <= 65535)) && ((blueColor >= 12000) && (blueColor <= 65535)))
  {
    rgb.setColor(255,255,255); // WHITE
  }

  else if (((redColor >= 4000) && (redColor <= 18000)) && ((greenColor >= 1300) && (greenColor <= 5000)) && ((blueColor >= 950) && (blueColor <= 2000)))
  {
    rgb.setColor(255,255,0);  // YELLOW
  }

  else if (((redColor >= 600) && (redColor <= 2000)) && ((greenColor >= 1700) && (greenColor <= 10000)) && ((blueColor >= 6800) && (blueColor <= 27000)))
  {
    rgb.setColor(0,0,255);    // BLUE
  }

  else if (((redColor >= 1400) && (redColor <= 4000)) && ((greenColor >= 1300) && (greenColor <= 10000)) && ((blueColor >= 950) && (blueColor <= 2700)))
  {
    rgb.setColor(0,255,0);    // GREEN
  }

  else if (((redColor >= 3000) && (redColor <= 20000)) && ((greenColor >= 700) && (greenColor <= 2400)) && ((blueColor >= 950) && (blueColor <= 3000)))
  {
    rgb.setColor(255,0,0);    // RED
  }

  else if ((redColor < 1500) && (greenColor < 1400) && (blueColor < 900))
  {
    rgb.setColor(0,0,0);  // OFF
  }

  delay(5000);
}

/**@brief LoRa function for handling HasJoined event.
 */
void lorawan_has_joined_handler(void) {
  Serial.println("OTAA Mode, Network Joined!");
}

/**@brief LoRa function for handling OTAA join failed
*/
static void lorawan_join_failed_handler(void) {
  Serial.println("OTAA join failed!");
  Serial.println("Check your EUI's and Keys's!");
  Serial.println("Check if a Gateway is in range!");
}
/**@brief Function for handling LoRaWan received data from Gateway
 *
 * @param[in] app_data  Pointer to rx data
 */
void lorawan_rx_handler(lmh_app_data_t *app_data) {
  Serial.printf("LoRa Packet received on port %d, size:%d, rssi:%d, snr:%d, data:%s\n",
                app_data->port, app_data->buffsize, app_data->rssi, app_data->snr, app_data->buffer);
}

void lorawan_confirm_class_handler(DeviceClass_t Class) {
  Serial.printf("switch to class %c done\n", "ABC"[Class]);
  // Informs the server that switch has occurred ASAP
  m_lora_app_data.buffsize = 0;
  m_lora_app_data.port = gAppPort;
  lmh_send(&m_lora_app_data, g_CurrentConfirm);
}

String data = "";

void send_lora_frame(void) {
  if (lmh_join_status_get() != LMH_SET) {
    //Not joined, try again later
    return;
  }

  Serial.print("result: ");
  uint32_t i = 0;
  memset(m_lora_app_data.buffer, 0, LORAWAN_APP_DATA_BUFF_SIZE);
  m_lora_app_data.port = gAppPort;

  // Showing the values of red, green and blue colors from RAK12021
  data = " Red: " + String(redColor) + " Green: " + String(greenColor) + " Blue: " + String(blueColor);

  Serial.println(data);

  uint16_t red_data = redColor;
  uint16_t green_data = greenColor;
  uint16_t blue_data = blueColor;

  m_lora_app_data.buffer[i++] = 0x01;  // byte[0]

  // Red data
  m_lora_app_data.buffer[i++] = (uint8_t)((red_data & 0x0000FF00) >> 8);     // byte[1]
  m_lora_app_data.buffer[i++] = (uint8_t)(red_data & 0x000000FF);            // byte[2]

  // Green data
  m_lora_app_data.buffer[i++] = (uint8_t)((green_data & 0x0000FF00) >> 8);   // byte[3]
  m_lora_app_data.buffer[i++] = (uint8_t)(green_data & 0x000000FF);          // byte[4]

  // Blue data
  m_lora_app_data.buffer[i++] = (uint8_t)((blue_data & 0x0000FF00) >> 8);    // byte[5]
  m_lora_app_data.buffer[i++] = (uint8_t)(blue_data & 0x000000FF);           // byte[6]

  m_lora_app_data.buffsize = i;

  lmh_error_status error = lmh_send(&m_lora_app_data, g_CurrentConfirm);
  if (error == LMH_SUCCESS) {
    count++;
    Serial.printf("lmh_send ok count %d\n", count);
  } else {
    count_fail++;
    Serial.printf("lmh_send fail count %d\n", count_fail);
  }
}

```
:::

Before uploading the Arduino Code, there are configurations that you need to set up to ensure that the device can join a LoRaWAN Network server. The steps below will explain the default settings and how to configure them.

- Set up the LoRaWAN region. The **LORAMAC_REGION** can be any of your desired region to work with. You can change this to a region that is applicable to you like `LORAMAC_REGION_US915`, `LORAMAC_REGION_AU915`, etc. Below is the table of LoRaWAN regions and their respective countries where they are used in:

|     LoRaWAN Region      |                               Usage                                  |
| ----------------------- | -------------------------------------------------------------------- |
| LORAMAC_REGION_AS923-1  | Australia, Singapore, Solomon Islands, Sri-Lanka, Taiwan             |
| LORAMAC_REGION_AS923-2  | Vietnam                                                              |
| LORAMAC_REGION_AS923-3  | Philippines, Albania, Algeria, Denmark, Greenland, Jordan            |
| LORAMAC_REGION_AS923-4  | Israel                                                               |
| LORAMAC_REGION_AU915    | Australia, Anguilla, Argentina, and many parts of South America      |
| LORAMAC_REGION_CN470    | China                                                                |
| LORAMAC_REGION_EU433    | EU, UK, Brazil, Costa Rica, Cuba, and many parts of Africa           |
| LORAMAC_REGION_IN865    | India, Cook Islands, Egypt, Hong Kong, Jordan, New Zealand, Niger    |
| LORAMAC_REGION_EU868    | EU, UK and many parts of Africa                                      |
| LORAMAC_REGION_KR920    | Republic of Korea                                                    |
| LORAMAC_REGION_US915    | USA                                                                  |
| LORAMAC_REGION_RU864    | Russia                                                               |

```c
LoRaMacRegion_t g_CurrentRegion = LORAMAC_REGION_US915;    /* Region:US915*/
```
- Set up the LoRaWAN activation method. In this case, we will be using the **OTAA** configuration which is also the default from the given code.

```c
bool doOTAA = true;   // OTAA is used by default.
```

- Set up the message type if confirmed or not. **Confirmed message** is the default for this one. You can change to an **unconfirmed message** by changing the value to `LMH_UNCONFIRMED_MSG`.

```c
lmh_confirm g_CurrentConfirm = LMH_CONFIRMED_MSG;         /* confirm/unconfirm packet definition*/
```

- Set the device to **Class A**.

```c
DeviceClass_t g_CurrentClass = CLASS_A;         /* class definition*/
```

- Setup the EUIs and KEY. The **DeviceEUI**, **AppEUI** and **AppKey** are the credentials of your device registered to TTN that will be used for the OTAA keys in the code. You need to replace the ones in the code with the credentials registered in TTN.

```c
//OTAA keys !!!! KEYS ARE MSB !!!!
uint8_t nodeDeviceEUI[8] = { 0xAC, 0x1F, 0x09, 0xFF, 0xFE, 0x05, 0x3E, 0x3E };
uint8_t nodeAppEUI[8] = { 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00 };
uint8_t nodeAppKey[16] = { 0x96, 0xBD, 0xC5, 0x98, 0x17, 0x69, 0x8D, 0xFA, 0x1F, 0x64, 0xFE, 0x1C, 0xF9, 0x26, 0x7F, 0x8D };
```

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12021_1.png"
  width="90%"
  caption="OTAA device successfully registered to TTN"
/>

3. Once done with the code, you can now proceed uploading it into your device. You need to select first your RAK4631 board from desktop or laptop. To do this, go to **Tools** > **Board:XXXXX** > **RAKwireless nRF Boards** > **WisBlock RAK4631**. After you selected your board, you need to select the specific port of your board. To do this, go to **Tools** > **Port** > then the specific port of your board.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12021_3.png"
  width="90%"
  caption="Selecting the RAK4631 board"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12021_4.png"
  width="90%"
  caption="Selecting the port of RAK4631 board"
/>

4. Once done, you can now upload your code. Simply click the right arrow sign at the upper left portion of your Arduino IDE. Once done, you will see the **Device programmed** notification at the bottom part of your Arduino IDE.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12021_5.png"
  width="90%"
  caption="Uploading your code into your RAK4631 board"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12021_6.png"
  width="90%"
  caption="Arduino code is successfully uploaded into your RAK4631 board"
/>

###### Light Color Recognizer via TTN

1. To monitor the data of your **Light Color Recognizer** device via **TTN**, you need to go back to your TTN account where you created your application and registered your device.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12021_2.png"
  width="90%"
  caption="Your Light Color Recognizer device in TTN"
/>

2. Then go to **Payload formatters**. Under **Formatter type**, select **Custom Javascript formatter**. Then under the **Formatter code**, you need to replace the default code with the one below. This will decode the data from your device going to **TTN**. Once done, simply click **Save changes**.

```c
// LoRaWAN code for RAK12021 + RAK14001 Application

function Decoder(bytes, port)
{

  var decoded = {};

  if (port === 2)
  {
    if( bytes[0] == 1) // check if the header byte is 1.
    {
      red_data = (bytes[1] << 8) | (bytes[2]);
      green_data = (bytes[3] << 8) | (bytes[4]);
      blue_data = (bytes[5] << 8) | (bytes[6]);

      decoded.red = red_data;
      decoded.green = green_data;
      decoded.blue = blue_data;

      return decoded;
    }
  }
}
```

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12021_7.png"
  width="90%"
  caption="Payload Formatter"
/>

3. Then go back to **Live data** of your device in TTN and compare it with the live data from the **Serial Monitor** of your device. You should now seeing identical results between them.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12021_8.png"
  width="90%"
  caption="Live data from your device in TTN"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_RAK12021_9.png"
  width="90%"
  caption="Live data from your device in its Serial Monitor"
/>

###### Light Color Recognizer via Qubitro

This section will guide you on how to integrate your application using Qubitro.

1. Go to [Qubitro Portal](https://portal.qubitro.com/login) and create your account.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_1.png"
  width="80%"
  caption="Creating Qubitro Account"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_2.png"
  width="80%"
  caption="Creating Qubitro Account"
/>

2. Once done with the account creation, login into your **Qubitro Account**. Then click **New Project**, then fill out your desired **Name**, as well as the **Description** based on your light color recognizer application, then click **Create**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_3.png"
  width="80%"
  caption="Creating New Project"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_4.png"
  width="80%"
  caption="Creating New Project"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_5.png"
  width="80%"
  caption="Created New Project"
/>

3. Then click into your newly-created project then click **New source**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_6.png"
  width="80%"
  caption="Adding New source"
/>

4. Among the data sources, choose **The Things Stack**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_7.png"
  width="80%"
  caption="Choosing The Things Stack"
/>

5. For the **integration type**, choose **Import from network**, then copy and paste the **PROJECT ID** and **WEBHOOK SIGNING KEY** temporarily to notepad. These credentials will be used on the later part, then click **Go to project**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_8.png"
  width="80%"
  caption="Copying the credentials"
/>

6. Then head back to your **TTN Application** where you created your light color recognizer application to add webhook from it. To do this, just click your device then go to **Integrations** > **Webhooks** > **+ Add webhook**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_9.png"
  width="80%"
  caption="Going to your TTN application for your Light Color Recognizer Application"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_10.png"
  width="80%"
  caption="Adding Webhook"
/>

7. Then choose **Qubitro** as your webhook template.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_11.png"
  width="80%"
  caption="Qubitro"
/>

8. Then fill in the needed details:
   - **Webhook ID** - For this example, you can use **light-color-recognizer-application**.
   - **Project ID** - Paste the credential you copied from **Step 5**.
   - **Webhook Signing Key** - Paste the credential you copied from **Step 5**.

   Then click **Create Qubitro webhook**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_12.png"
  width="90%"
  caption="Creating Qubitro webhook"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_13.png"
  width="100%"
  caption="Added a Qubitro webhook"
/>

9. After you created your webhook, go back to your **Qubitro** platform to check the changes made. Refresh **Qubitro** by clicking the **Refresh** button on the upper right side of your screen. You will notice that a newly-added device is included in the platform.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_14.png"
  width="80%"
  caption="Device successfully included in Qubitro"
/>

10. To add the decoder, simply go to **Functions** > **Create Function**. Then under **Decoder Function**, click **Get started**. You will be now routed to **Function Configuration**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_15.png"
  width="80%"
  caption="Creating Function"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_16.png"
  width="80%"
  caption="Decoder Function"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_17.png"
  width="80%"
  caption="Function Configuration"
/>

11. Under the **Formatter type**, choose **Custom Javascript formatter**. Then under the **Formatter code**, you need to replace its default entry with the code below:

```c
// LoRaWAN code for RAK12021 + RAK14001 Application

function Decoder(bytes, port)
{

  var decoded = {};

  if (port === 2)
  {
    if( bytes[0] == 1) // check if the header byte is 1.
    {
      red_data = (bytes[1] << 8) | (bytes[2]);
      green_data = (bytes[3] << 8) | (bytes[4]);
      blue_data = (bytes[5] << 8) | (bytes[6]);

      decoded.red = red_data;
      decoded.green = green_data;
      decoded.blue = blue_data;

      return decoded;
    }
  }
}
```

Once done, simply click **Save and complete**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_18.png"
  width="80%"
  caption="Function Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_19.png"
  width="80%"
  caption="Created Decoder Function"
/>

12. Then go to your device and click on the **Data** tab to check for the incoming data coming from your device. You should now be seeing live data from your device. To gather the most recent data, simply click **Refresh**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_20.png"
  width="80%"
  caption="Data Tab"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_21.png"
  width="80%"
  caption="Historical Data"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_22.png"
  width="80%"
  caption="Refreshing data to get newer ones"
/>

13. To add a monitoring dashboard for the data from the light color recognizer device, you need to go to **Home** which is located at the left top most part of your screen. Then click **Dashboards** > **New dashboard** > **Create new**. Then fill out the **Create New Dashboard** portion using the details of your device. For the **Tags**, just simply input **Test** then click **Create**. Once done, click on to your newly-created dashboard.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_23.png"
  width="90%"
  caption="Creating dashboard for your Light Color Recognizer device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_24.png"
  width="90%"
  caption="Creating dashboard for your Light Color Recognizer device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_25.png"
  width="90%"
  caption="Creating dashboard for your Light Color Recognizer device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_26.png"
  width="90%"
  caption="Creating dashboard for your Light Color Recognizer device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_27.png"
  width="90%"
  caption="Newly-created dashboard for your Light Color Recognizer device"
/>

14. Click **Edit** > **New widget** to add a widget for a specific parameter need to be monitored.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_28.png"
  width="80%"
  caption="Adding a widget"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_29.png"
  width="80%"
  caption="Adding a widget"
/>

15. Once done, you're now at the **Widget Configuration**. At the **WIDGET TYPE**, choose **Chart**. Then provide the name of the parameter under **SHOW WIDGET NAME**. Once done, proceed to **Add point +**. Choose your **existing project**, **application** and the **specific parameter** you need to monitor in your dashboard. Once done, just click **Save**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_30.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_31.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_32.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_33.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_34.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_35.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_36.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_37.png"
  width="100%"
  caption="Connect Data Point"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_38.png"
  width="100%"
  caption="Connect Data Point"
/>

16. Now you have an existing preview of your data from your device. Under **CHART TYPE** at the left side of your screen, choose **Bar**. Also, you can modify the color of your bar graph at the **STYLE** section. Once done, go to **STANDARD OPTIONS** to choose the appropriate unit for your parameter to be monitored in the dashboard. Once done, click **Save widget**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_39.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_40.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_41.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_42.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_43.png"
  width="100%"
  caption="Widget Configuration"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_44.png"
  width="100%"
  caption="Saving the changes made in your Widget Configuration"
/>

17. Then click **Save changes** to include the data of parameter. Then you have now the newly-made widget for your specific parameter.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_45.png"
  width="100%"
  caption="Save changes"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_46.png"
  width="100%"
  caption="Newly-made widget"
/>

18. In able for you to include additional widgets for other parameters, you need to click **Edit** > **New widget** then repeat **Step 15** to **Step 17**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_47.png"
  width="100%"
  caption="Adding widgets into your dashboard"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_48.png"
  width="100%"
  caption="Adding widgets into your dashboard"
/>

19. Then there you have it a real-time monitoring dashboard for your light color recognizer device.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/Light_Qub_49.png"
  width="90%"
  caption="Monitoring dashboard for your light color recognizer device"
/>

[Back](#lorawan-applications-for-wisblock-iot-education-kit-light-color-using-ttn-and-qubitro)

## Miscellaneous

### TTN Account Creation

1. The first step is to go to [The Things Network](https://www.thethingsnetwork.org/) and sign up an account shown in the figure below. Then select a cluster as shown in the figure below.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_1.png"
  width="90%"
  caption="Signing up an account in TTN"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_2.png"
  width="90%"
  caption="Signing up an account in TTN"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_3.png"
  width="90%"
  caption="Selecting Cluster in TTN"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_4.png"
  width="90%"
  caption="Signing up through the Things ID"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_5.png"
  width="90%"
  caption="Creation of an account through the Things ID"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_6.png"
  width="90%"
  caption="Creation of an account through the Things ID"
/>

You can use the same login credentials on the TTN V2 if you have one. If you have no account yet, you need to create one.

2. Now that you are logged in to the platform, the next step is to create an application. Click **Create an application**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_7.png"
  width="90%"
  caption="The Things Stack Platform"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_8.png"
  width="90%"
  caption="Creating TTN Application of your LoRaWAN devices"
/>

3. To have an application registered, input first the specific details and necessary information about your application then click **Create application**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_9.png"
  width="70%"
  caption="Details of the TTN application"
/>

::: tip 📝 NOTE

The details and information are dependent to what device you are using (e.g. **RAK12019**, etc.).

:::

4. If you have no error on the previous step, you should now be on the application console page.

::: tip 📝 NOTE

Above procedures are applicable to all applications you will be using.

- For **UV Index & UV Intensity Monitoring**, go to this [link](#uv-index-uv-intensity-monitoring-ttn-registration-section-and-device-registration) once done with the TTN account creation.
- For **Light Color Recognizer**, go to this [link](#light-color-recognizer-ttn-registration-section-and-device-registration) once done with the TTN account creation.

:::

### Device Registration

1. Go to your application console to register a device. To start adding an OTAA end-device, click **+ Register end device**, as shown below.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_11.png"
  width="90%"
  caption="Register End Device"
/>

2. To register the board, click the **Enter end device specifics manually**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_12.png"
  width="60%"
  caption="Enter end device specifics manually"
/>

3. Next step is to set up **Frequency plan**, compatible **LoRaWAN version**, and **Regional Parameters version** supported. Then provide the **JoinEUI** credentials by entering zeroes into it.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_13.png"
  width="70%"
  caption="Setting up your device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_14.png"
  width="60%"
  caption="Setting up your device"
/>

4. Then click **Show advanced activation, LoRaWAN class and cluster settings**. Configure the activation mode by selecting **Over the air activation (OTAA)** and Additional LoRaWAN class capabilities to **class A only**. Then click **Confirm**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_15.png"
  width="60%"
  caption="Setting up your device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_16.png"
  width="50%"
  caption="Setting up your device"
/>

5. Once done, provide the DevEUI credentials of your device into the **DevEUI** portion. This will automatically generate the specific End
device ID of your board. Then click **Generate** under **AppKey** under Provisioning information section. Once done, you need to change the **End device ID** since it is automatically prefilled using the **DevEUI** of your device. Then click **Register end device**.

:::tip 📝 NOTE:

- The **AppEUI**, **DevEUI**, and **AppKey** are hidden in this section as these are unique from a specific device. The **DevEUI** credential is unique to every **RAK4631** device. Also, you should generate your own **AppEUI** and **AppKey** credentials for your specific device and application.

- The **AppEUI** is the same as **JoinEUI**.

- The details under **End device ID** are dependent to what device you are using (e.g. **uv-intensity-meter**, etc.).

:::

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_17.png"
  width="50%"
  caption="Setting up your device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_18.png"
  width="50%"
  caption="Setting up your device"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_19.png"
  width="50%"
  caption="Changing the End device ID"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_20.png"
  width="50%"
  caption="Register End Device"
/>

6. You should now be able to see the device on the TTN console after you fully register your device, as shown below.

:::tip 📝 NOTE:

- The **AppEUI**, **DevEUI**, and **AppKey** are the parameters that you will need to activate your LoRaWAN end-device via OTAA. The **AppKey** is hidden by default for security reasons, but you can easily show it by clicking the show button. You can also copy the parameters quickly using the copy button.

- These parameters are always accessible on the device console page, as highlighted in the figure below.
:::

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_21.png"
  width="90%"
  caption="OTAA device successfully registered to TTN"
/>

::: tip 📝 NOTE

Above procedures are applicable to all applications you will be using.

- For **UV Index & UV Intensity Monitoring**, go to this [link](#lorawan-code-for-uv-index-uv-intensity-monitoring) once done with the device registration.
- For **Light Color Recognizer**, go to this [link](#lorawan-code-for-light-color-recognizer) once done with the device registration.

:::

### Arduino IDE Installation + RAK4631

1. Download the [Arduino IDE](https://www.arduino.cc/en/software) and install it on your PC or laptop. You must choose the appropriate **Arduino IDE** depending on your operating system.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_22.png"
  width="80%"
  caption="Download Options for the Arduino IDE"
/>

2. Open the **Arduino IDE** then install the [RAKwireless Arduino BSP](https://github.com/RAKWireless/RAKwireless-Arduino-BSP-Index) for WisBlock by using the `package_rakwireless_index.json` board installation package. The WisBlock Core should now be available on the Arduino IDE. Click on **File** > **Preference**. In the **Preference** window, look for **Additional Boards Manager URLs** then click the icon on the right side. Paste the link into it then click **OK** > **OK**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_23.png"
  width="80%"
  caption="Preference Set-Up"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_24.png"
  width="80%"
  caption="Preference Window"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_25.png"
  width="80%"
  caption="RAKwireless Arduino BSP"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_26.png"
  width="80%"
  caption="Completing the setup of the RAKwireless BSP support for the Arduino Board Manager"
/>

3. Then to your **Arduino IDE**, go to **Tools** > **Board:XXXXX** > **Boards Manager**. Then look for **RAKwireless Boards by RAKwireless** since we will be working on with the **RAK4631 WisBlock Core**. Choose the latest version then install it. Once done, close the **Board Manager**.

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_27.png"
  width="80%"
  caption="Opening the Boards Manager"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_28.png"
  width="80%"
  caption="Installing the RAKwireless nRF Boards"
/>

<rk-img
  src="/assets/images/wisblock/kits/kit6_quickstart/TTN_Kit_Light_29.png"
  width="80%"
  caption="Successfully installed the RAKwireless nRF Boards"
/>

::: tip 📝 NOTE

Above procedures are applicable to all applications you will be using.

- For **UV Index & UV Intensity Monitoring**, go to this [link](#lorawan-code-for-uv-index-uv-intensity-monitoring) once done with the device registration.
- For **Light Color Recognizer**, go to this [link](#lorawan-code-for-light-color-recognizer) once done with the device registration.

:::




