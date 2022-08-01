# ThermoLog
Publishes data from DS18B20 1-wire sensors to MQTT.

## Overview

The purpose of this programme is to read the values from 1-wire 
temperature sensors and publish the values to an MQTT broker.

It presently assumes use of DS18B20 temperature sensors, but may be
compatible with, or modified for use with, other similar sensors.

It has been tested using a Raspberry Pi.  Remember to enable the 1-wire
protocol using the Raspberry Pi OS configuration utility.


Several functions have been found on or were inspired by:
http://www.steves-internet-guide.com/into-mqtt-python-client/

## Configuration

Configuration is stored in two files:

- `config.json`
- `sensors.json`

### config.json

| Setting | Details |
|---|---|
|"broker": "127.0.0.1",|                        IP Address of MQTT Broker.|
|"port": 1883,|                                 Port of MQTT Broker.|
|"sensorTempTopic": "zigbee2mqtt/ThermoLog",|   MQTT Topic to Publish values to.|
|"deltaT": 1.0,|                                Minimum temperature difference before publishing to MQTT Broker.|
|"logToFile": true |                            Optionally, log data to file.|

### sensors.json

Each sensor is given a name, and the associated sensor ID for that sensor.

For example, a sensor named `TempA` is associated with its sensor ID as follows:

`"TempA":"28-xxxxxxxxxxxx"`

Where `28-xxxxxxxxxxxx` is replaced with the specific sensor ID for the 1-wire sensor in use.

