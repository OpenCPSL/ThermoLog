# ThermoLog
Publishes data from DS18B20 1-wire sensors to MQTT.

The purpose of this programme is to read the values from 1-wire 
temperature sensors and publish the values to an MQTT broker.

It presently assumes use of DS18B20 temperature sensors, but may be
compatible with, or modified for use with, other similar sensors.

It has been tested using a Raspberry Pi.  Remember to enable the 1-wire
protocol using the Raspberry Pi OS configuration utility.


Several functions have been found on or were inspired by:
http://www.steves-internet-guide.com/into-mqtt-python-client/
