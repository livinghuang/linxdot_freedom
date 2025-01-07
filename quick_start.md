# Linxdot LD1002 Operations Manual

![LD1002 BOX](/pictures/front.png)

## Table of Contents
- [Linxdot LD1002 Operations Manual](#linxdot-ld1002-operations-manual)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Getting Started](#getting-started)
  - [Product Components](#product-components)
  - [Installation](#installation)
  - [Operation Instructions](#operation-instructions)
  - [Accessing LD1002 via SSH and Editing global_conf.json](#accessing-ld1002-via-ssh-and-editing-global_confjson)
  - [Troubleshooting](#troubleshooting)
  - [Maintenance](#maintenance)
  - [Safety Guidelines](#safety-guidelines)
  - [Contact Information](#contact-information)

---

## Introduction

Welcome to the Linxdot LD1002 Operations Manual! This document is designed to provide you with all the necessary information to effectively and safely use the LD1002 LoRaWAN Gateway pre-installed with ChirpStack Server.

![LD1002 open view](/pictures/open.png)

LD1002 interfaces include:
- RJ45  
- USB  
- LORA ANTENNA  

![LD1002 back view](/pictures/back.png)

---

## Getting Started

Before using the LD1002, please ensure that you have read through this manual thoroughly. Familiarize yourself with the product components and follow the installation instructions provided below.

---

## Product Components

- Linxdot LD1002 LoRaWAN Gateway  
- Power Adapter  
- Antennas  

![LD1002 contents view](/pictures/contents.png)

---

## Installation

1. Connect the LD1002 to power using the provided power adapter.  
2. Connect the LD1002 to your network using the Ethernet cable.  
3. Attach the antennas to the designated ports on the LD1002.  

![LD1002 running view](/pictures/running.png)

---

## Operation Instructions

1. Connect one end of the Ethernet cable to your intranet using an RJ45 connector.  
2. Connect the other end of the Ethernet cable to the LD1002.  
3. The LD1002 will automatically connect to the network.  
4. Once connected, the LD1002 will obtain an IP address from your DHCP server.  
5. Open a web browser on your computer and enter the LD1002’s IP address in the address bar.  
6. This will open the ChirpStack Server interface.

   ![LD1002 login view](/pictures/chripstack_login.png)

7. Log in using your credentials. (Default username: `admin` , password: `admin`)  
8. Once logged in, you can access ChirpStack’s App Server services.

   ![LD1002 first view](/pictures/chirpstack_first.png)

9. To add the LD1002 LoRaWAN Gateway for the first time, use the Gateway ID: `8888880000000000`.

   ![LD1002 add gateway](/pictures/chirpstack_add_gateway1.png)

   *(You can move the map pin to set the gateway location during this step.)*

   ![LD1002 set gateway](/pictures/chirpstack_add_gateway4.png)

10. Follow the ChirpStack Server documentation for further configuration and management of devices.

---

## Accessing LD1002 via SSH and Editing global_conf.json

To configure the LD1002 LoRaWAN Gateway further, you can SSH into the device and edit the `global_conf.json` file. Follow these steps:

1. Open a terminal on your computer.  
2. Use the SSH command to connect to the LD1002:
   ```bash
   ssh root@<LD1002_IP_Address>
   ```
   Replace `<LD1002_IP_Address>` with the actual IP address of your LD1002. When prompted, enter the password: `linxdot`.

3. Once logged in, navigate to the directory containing the `global_conf.json` file:
   ```bash
   cd /etc/lora/
   ```

4. Use the `vi` editor to open the file that corresponds to your region and radio module. For example:
   ```bash
   vi global_conf.json.sx1250.AS923_1
   ```

   ![LD1002 change gateway id](/pictures/chirpstack_change_gateway_id.png)

5. Press `i` to enter **insert** mode and make necessary modifications.  
6. Press `Esc` to exit insert mode when finished editing.  
7. Type `:wq` and press Enter to save changes and exit the editor.  
8. Restart the LoRaWAN Gateway service to apply the changes:
   ```bash
   systemctl restart lorawan-gateway
   ```

---

## Troubleshooting

If you encounter any issues while using the LD1002, refer to the following steps:

1. Ensure that the LD1002 is powered on and properly connected to the network.  
2. Check your network settings and connections.  
3. Restart the LD1002 and/or ChirpStack Server if necessary.

---

## Maintenance

Regular maintenance helps ensure the longevity and performance of the LD1002. Follow these guidelines:

1. Check for firmware updates periodically and install them as needed.  
2. Keep the LD1002 and antennas clean and free from dust or debris.

---

## Safety Guidelines

Safety is a top priority. Please adhere to the following guidelines while using the LD1002:

1. Only use the provided power adapter and cables.  
2. Do not attempt to disassemble or modify the LD1002.  
3. Avoid exposing the LD1002 to extreme temperatures or moisture.

---

## Contact Information

If you have any questions, concerns, or require assistance, please contact Linxdot customer support:

- **Phone**: 02-77515339  
- **Email**: [support@guineatech.com](mailto:support@guineatech.com)  
- **Website**: [www.guineatech.com](http://www.guineatech.com)  

---
# Linxdot LD1002 操作手冊

![LD1002 BOX](/pictures/front.png)

## 目錄
- [Linxdot LD1002 操作手冊](#linxdot-ld1002-操作手冊)
  - [目錄](#目錄)
  - [簡介](#簡介)
  - [快速上手](#快速上手)
  - [產品組件](#產品組件)
  - [安裝教學](#安裝教學)
  - [操作說明](#操作說明)
  - [透過 SSH 連線至 LD1002 並編輯 global_conf.json](#透過-ssh-連線至-ld1002-並編輯-global_confjson)
  - [故障排除](#故障排除)
  - [維護與保養](#維護與保養)
  - [安全指南](#安全指南)
  - [聯絡資訊](#聯絡資訊)

---

## 簡介

歡迎使用 **Linxdot LD1002** 操作手冊！本手冊將為您提供完整資訊，協助您有效且安全地使用內建 **ChirpStack Server** 的 **LD1002 LoRaWAN Gateway**。

![LD1002 open view](/pictures/open.png)

**LD1002 具備以下介面：**
- RJ45  
- USB  
- LORA 天線  

![LD1002 back view](/pictures/back.png)

---

## 快速上手

在使用 LD1002 前，請先詳細閱讀本手冊，並確實瞭解產品組件；接著依照下列安裝說明進行設定。

---

## 產品組件

- Linxdot LD1002 LoRaWAN Gateway  
- 電源供應器  
- 天線  

![LD1002 contents view](/pictures/contents.png)

---

## 安裝教學

1. 使用隨附的電源供應器為 LD1002 供電。  
2. 使用乙太網路線（Ethernet cable）將 LD1002 連接至網路。  
3. 將天線旋入 LD1002 專用的天線連接埠。

![LD1002 running view](/pictures/running.png)

---

## 操作說明

1. 將乙太網路線的一端透過 RJ45 連接器，插入內部網路。  
2. 將乙太網路線的另一端連接至 LD1002。  
3. LD1002 通電後會自動連線至網路。  
4. 取得 DHCP 伺服器分配的 IP 位址後，在電腦上的瀏覽器輸入該 IP 位址。  
5. 將開啟 **ChirpStack Server** 介面。

   ![LD1002 login view](/pictures/chripstack_login.png)

6. 使用您的帳號密碼登入。預設帳號為：`admin`，密碼為：`admin`。  
7. 登入後，即可進入 **ChirpStack** 的應用伺服器（App Server）功能頁面。

   ![LD1002 first view](/pictures/chirpstack_first.png)

8. 第一次新增 LD1002 LoRaWAN Gateway 時，請使用 Gateway ID：`8888880000000000`。

   ![LD1002 add gateway](/pictures/chirpstack_add_gateway1.png)

   *（在此步驟中，您可以拖曳地圖上的定位點來設定閘道器所在位置）*

   ![LD1002 set gateway](/pictures/chirpstack_add_gateway4.png)

9. 接下來請依 **ChirpStack Server** 官方文件進行更多裝置的設定與管理。

---

## 透過 SSH 連線至 LD1002 並編輯 global_conf.json

若需要進一步配置 **LD1002 LoRaWAN Gateway**，可使用 SSH 登入裝置並修改 `global_conf.json`。請依下列步驟操作：

1. 在電腦上開啟終端機（Terminal）。  
2. 使用 SSH 指令連線至 LD1002：
   ```bash
   ssh root@<LD1002_IP_Address>
   ```
   請將 `<LD1002_IP_Address>` 替換為實際的 LD1002 IP 位址。系統提示後，輸入密碼：`linxdot`。

3. 登入後，進入存放 `global_conf.json` 的資料夾：
   ```bash
   cd /etc/lora/
   ```

4. 使用 `vi` 編輯與您所處頻段及無線電模組相對應的設定檔。例如：
   ```bash
   vi global_conf.json.sx1250.AS923_1
   ```

   ![LD1002 change gateway id](/pictures/chirpstack_change_gateway_id.png)

5. 按下 `i` 進入**插入模式（insert mode）**，進行所需的參數修改。  
6. 修改完畢後，按 `Esc` 退出插入模式。  
7. 輸入 `:wq` 並按下 Enter 儲存並退出編輯器。  
8. 重啟 LoRaWAN Gateway 服務，使變更生效：
   ```bash
   systemctl restart lorawan-gateway
   ```

---

## 故障排除

若使用 LD1002 期間遇到問題，可參考下列方式進行排除：

1. 確認 LD1002 是否已正確開機並連線至網路。  
2. 檢查網路設定與連線品質。  
3. 必要時，重啟 LD1002 或 ChirpStack Server。

---

## 維護與保養

定期維護有助於延長 LD1002 的使用壽命與維持其效能，建議您：

1. 不定期檢查並安裝可用的韌體更新。  
2. 保持 LD1002 與天線的清潔，避免灰塵與雜物積累。

---

## 安全指南

我們非常重視使用者的安全。請確實遵守下列注意事項：

1. 請僅使用隨附的電源供應器與線材。  
2. 請勿自行拆解或改裝 LD1002。  
3. 避免將 LD1002 暴露於極端溫度或潮濕環境中。

---

## 聯絡資訊

若您有任何疑問、需求或其他協助，歡迎與我們聯繫：

- **電話**: 02-77515339  
- **電子郵件**: [support@guineatech.com](mailto:support@guineatech.com)  
- **官網**: [www.guineatech.com](http://www.guineatech.com)