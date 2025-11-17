# IOT_AirQuality_Sensor

Overview

This project is an IoT-based Air Quality Monitoring System that measures:

1.Gas Concentration (MQ-135)

2.Dust Density (PM2.5/PM10) using DSM501A

3.Temperature & Humidity (DHT22)

4.Real-time display on a 16x4 LCD

5.Data transmission to Raspberry Pi over Serial

6.Monitoring through Prometheus + Grafana dashboards

The system continuously reads environmental parameters via Arduino sensors and forwards them to a Raspberry Pi, which exposes metrics for scraping by Prometheus. Grafana then visualizes these metrics through customizable dashboards.

Hardware Components

1.Arduino Uno / Mega

2.Raspberry Pi (any model with USB)

3.MQ-135 Gas Sensor

4.DSM501A Dust Sensor

5.DHT22 Temperature & Humidity Sensor

6.16×4 LCD Display + I2C module

8.Jumper wires, Breadboard

9.USB cable (Arduino ↔ Raspberry Pi)


System Architecture:
Sensors (MQ-135, DSM501A, DHT22, DSM501A)
             ↓
        Arduino (C++)
             ↓ Serial USB
       Raspberry Pi (Python)
             ↓
        Prometheus Exporter
             ↓
        Prometheus Server
             ↓
            Grafana (Dashboard)


Arduino Features

Reads gas, dust density, temperature, humidity

Prints values via Serial in a strict format:

Gas: 220 | Dust: 40.2 ug/m3 | Hum: 48.5 % | Temp: 26.9 C


Displays all values on a 16×4 LCD screen

Includes improved sensor calibration and delay timing  
















































































end point : https://prometheus-prod-43-prod-ap-south-1.grafana.net/api/prom

remote end point : https://prometheus-prod-43-prod-ap-south-1.grafana.net/api/prom/push

username : 2781875

API name : stack-1428820-hm-write

glc_eyJvIjoiMTU4MTQwNiIsIm4iOiJzdGFjay0xNDI4ODIwLWhtLXdyaXRlLWR1c3QiLCJrIjoiNjcyTzMyb0MyODdKRjF2SjNxWlhsbnFpIiwibSI6eyJyIjoicHJvZC1hcC1zb3V0aC0xIn19
