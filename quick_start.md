# Linxdot LD1002 Operations Manual

![LD1002 BOX](/pictures/front.png)

## Table of Contents

- [Linxdot LD1002 Operations Manual](#linxdot-ld1002-operations-manual)
  - [Table of Contents](#table-of-contents)
  - [Introduction ](#introduction-)
  - [Getting Started ](#getting-started-)
  - [Product Components ](#product-components-)
  - [Installation ](#installation-)
  - [Operation Instructions ](#operation-instructions-)
  - [Accessing LD1002 via SSH and Editing global\_conf.json ](#accessing-ld1002-via-ssh-and-editing-global_confjson-)
  - [Hardware Information](#hardware-information)
  - [Troubleshooting ](#troubleshooting-)
  - [Maintenance ](#maintenance-)
  - [Safety Guidelines ](#safety-guidelines-)
  - [Contact Information ](#contact-information-)

## Introduction <a name="introduction"></a>

Welcome to the Linxdot LD1002 Operations Manual! This document is designed to provide you with all the necessary information to effectively and safely use the LD1002 Lorawan Gateway pre-installed with ChirpStack Server.

![LD1002 open view](/pictures/open.png)

LD1002 with those interface:
  - RJ45
  - USB
  - LORA ANTENNA

![LD1002 back view](/pictures/back.png)

## Getting Started <a name="getting-started"></a>

Before using the LD1002, please ensure that you have read through this manual thoroughly. Familiarize yourself with the product components and follow the installation instructions provided below.

## Product Components <a name="product-components"></a>

- Linxdot LD1002 Lorawan Gateway
- Power Adapter
- Antennas

![LD1002 contents view](/pictures/contents.png)

## Installation <a name="installation"></a>

1. Connect the LD1002 to power using the provided power adapter.
2. Connect the LD1002 to your network using the Ethernet cable.
3. Attach the antennas to the designated ports on the LD1002.

![LD1002 running view](/pictures/running.png)

## Operation Instructions <a name="operation-instructions"></a>

1. Connect one end of the Ethernet cable to your intranet using an RJ45 connector.
2. Connect the other end of the Ethernet cable to the LD1002.
3. The LD1002 will automatically connect to the network.
4. Once connected, the LD1002 will search for an IP address from the DHCP server.
5. After obtaining an IP address, open a web browser on your computer.
6. Enter the IP address of the LD1002 in the address bar of the web browser.
7. This will open the ChirpStack Server interface.
   
   ```bash
   ```

![LD1002 login view](/pictures/chripstack_login.png)

1. Log in to the ChirpStack Server interface using your credentials. Default username: "admin" , password: "admin"
2.  Once logged in, you can access the ChirpStack App Server services.

   ```bash
   ```

![LD1002 first view](/pictures/chirpstack_first.png)

10.  To add the LD1002 Lorawan Gateway as the 1st Lorawan Gateway, use the following Gateway ID: `8888880000000000`.

   ```bash
   ```

![LD1002 add gateway](/pictures/chirpstack_add_gateway1.png)

-- set the gateway(you could move the map point to set the gateway location in this stage)

   ```bash
   ```
![LD1002 set gateway](/pictures/chirpstack_add_gateway4.png)

11.  Follow the ChirpStack Server documentation for further configuration and management of devices.

## Accessing LD1002 via SSH and Editing global_conf.json <a name="accessing-ld1002-via-ssh"></a>

To configure the LD1002 Lorawan Gateway further, you can SSH into the device and edit the `global_conf.json` file. Follow these steps:

1. Open a terminal window on your computer.

2. Use the SSH command to connect to the LD1002:
   ```bash
   ssh root@<LD1002_IP_Address>
   ```
   Replace `<LD1002_IP_Address>` with the actual IP address of your LD1002. When prompted, enter the password `linxdot`.

3. Once logged in, navigate to the directory containing the `global_conf.json` file:
   ```bash
   cd /etc/lora/
   ```

4. Use the `vi` editor to open the `global_conf.json` file specific to your region and radio module. For example, for AS923_1 region and SX1250 radio module, use:
   ```bash
   vi global_conf.json.sx1250.AS923_1
   ```

![LD1002 change gateway id](/pictures/chirpstack_change_gateway_id.png)

5. Use the arrow keys to navigate through the file, and press `i` to enter insert mode.

6. Make the necessary modifications to the configuration parameters according to your requirements.

7. Once you have finished editing, press `Esc` to exit insert mode.

8. To save your changes and exit the vi editor, type `:wq` and press `Enter`.

9. Restart the Lorawan Gateway service to apply the changes:
   ```bash
   systemctl restart lorawan-gateway
   ```

Now, your LD1002 Lorawan Gateway is configured with the updated settings specified in the `global_conf.json` file.
These instructions provide a step-by-step guide for customers to SSH into the LD1002, edit the `global_conf.json` file using the vi editor, and restart the Lorawan Gateway service to apply the changes.

## Hardware Information

**Design**
- ABS plastic enclosure
- 190 x 190 x 50 mm
- 512 grams

**Connectivity**
- Bluetooth 5.0, BLE
- 802.11 b/g/n/ac WiFi
- 1Gbps Ethernet
- Semtech SX1302/SX1303 LoRa concentrator

**Antenna**
- 3dBi LoRa antenna included, higher dBi options available
- 27dBm Tx power
- RP-SMA female connector, allowing future upgrades and outdoor installations (outdoor enclosure available separately)

**SoC**
- Custom board design based on Rockchip RK3566
- Quad-Core CPU up to 1.8Ghz
- ATECC608 secure element

**RAM & Storage**
- 2GB

 RAM
- 32GB eMMC storage

**Power**
- Universal power supply (EU, UK, US, AU)
- Low power use – 5W at peak

## Troubleshooting <a name="troubleshooting"></a>

If you encounter any issues while using the LD1002, refer to the following troubleshooting guide:

1. Ensure that the LD1002 is powered on and connected to the network.
2. Check the network settings and connections.
3. Restart the LD1002 and/or ChirpStack Server if necessary.

## Maintenance <a name="maintenance"></a>

Regular maintenance is essential to ensure the longevity and performance of the LD1002. Follow these guidelines:

1. Check for firmware updates periodically and install them as needed.
2. Keep the LD1002 and antennas clean from dust and debris.

## Safety Guidelines <a name="safety-guidelines"></a>

Safety is our top priority. Please adhere to the following guidelines while using the LD1002:

1. Only use the provided power adapter and cables.
2. Do not attempt to disassemble or modify the LD1002.
3. Avoid exposing the LD1002 to extreme temperatures or moisture.

## Contact Information <a name="contact-information"></a>

If you have any questions, concerns, or require assistance, please contact Linxdot customer support:

- Phone: 02-77515339
- Email: support@guineatech.com
- Website: www.guineatech.com