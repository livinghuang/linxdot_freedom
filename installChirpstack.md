# Installing ChirpStack on Linxdot Freedom

This guide will explain what ChirpStack is and provide detailed steps to install it on the Linxdot Freedom gateway.

---
<img src="/pictures/chirpstack.png" alt="chirpstack" class="headline-image">

## **What is ChirpStack?**
ChirpStack is an open-source LoRaWAN Network Server stack. It provides essential components for LoRaWAN networks, including:

- **Network Server**: Handles the routing of messages between gateways and applications.
- **Application Server**: Provides APIs and tools for managing devices and applications.
- **Gateway Bridge**: Converts gateway communication protocols to LoRaWAN-compatible formats.

With ChirpStack, you can efficiently manage LoRaWAN devices, gateways, and applications, making it an ideal solution for private or public LoRaWAN networks.

---

## **Steps to Install ChirpStack on Linxdot Freedom**

### **Step 1: Install ChirpStack**

1. Open a terminal.
2. Navigate to the Linxdot open-source tools directory:
   ```bash
   cd /etc/linxdot-opensource/
   ```
   <img src="/pictures/installChirpstack0.png" alt="Install Chirpstack Step 0" class="operation-image">

3. Run the ChirpStack installation script:
   ```bash
   ./install-chirpstack.sh
   ```
   <img src="/pictures/installChirpstack1.png" alt="Install Chirpstack Step 1" class="operation-image">

4. After the installation completes, verify that the Docker containers are running:
   ```bash
   docker ps
   ```

---

### **Step 2: Log in to ChirpStack Admin**
1. Open a web browser and go to:
   ```
   http://{LinxdotIP}:8080
   ```
   Replace `{LinxdotIP}` with the IP address of your Linxdot Freedom gateway.
2. Log in with the default credentials:
   - **Username**: `admin`
   - **Password**: `admin`
3. Once logged in, add a new gateway in the ChirpStack admin interface. This will generate a `gateway_id`. Copy this ID for use in the next step.

---

### **Step 3: Configure LoRa Packet Forwarder**
1. Open a terminal.
2. Edit the LoRaWAN global configuration file:
   ```bash
   vi /etc/lora/global_conf.json.sx1250.AS923
   ```
3. Locate the line:
   ```json
   "gateway_ID": "8888880000000000"
   ```
   Replace `8888880000000000` with the `gateway_id` copied in Step 2.
4. Save and exit the file.
5. Run the LoRa Packet Forwarder installation script:
   ```bash
   cd /etc/linxdot-opensource/
   ./install-lora-pkd-fwd.sh
   ```
6. After the installation completes, check the ChirpStack admin interface to ensure the gateway is connected.

---

## **Final Notes**
After completing these steps, your Linxdot Freedom gateway will be fully set up with ChirpStack for LoRaWAN services. Ensure the gateway configuration matches your network requirements and verify device connectivity through the ChirpStack admin interface.

For further assistance, refer to the official Linxdot or ChirpStack documentation.

---

# 在 Linxdot Freedom 上安裝 ChirpStack

本指南將介紹什麼是 ChirpStack，並提供詳細步驟，指導您在 Linxdot Freedom 閘道設備上安裝它。

---

<img src="/pictures/chirpstack.png" alt="chirpstack" class="operation-image">

## **什麼是 ChirpStack？**
ChirpStack 是一個開源的 LoRaWAN 網路伺服器堆疊。它為 LoRaWAN 網路提供了以下重要組件：

- **Network Server（網路伺服器）**：處理閘道與應用程序之間的消息路由。
- **Application Server（應用伺服器）**：提供管理設備和應用程序的 API 和工具。
- **Gateway Bridge（閘道橋）**：將閘道通信協議轉換為 LoRaWAN 兼容格式。

透過 ChirpStack，您可以高效管理 LoRaWAN 設備、閘道和應用程序，是建構私人或公共 LoRaWAN 網路的理想解決方案。

---

## **在 Linxdot Freedom 上安裝 ChirpStack 的步驟**

### **步驟 1：安裝 ChirpStack**
1. 打開終端機。
2. 進入 Linxdot 開源工具目錄：
   ```bash
   cd /etc/linxdot-opensource/
   ```
   <img src="/pictures/installChirpstack0.png" alt="Install Chirpstack Step 0" class="operation-image">

3. 執行 ChirpStack 安裝腳本：
   ```bash
   ./install-chirpstack.sh
   ```
   <img src="/pictures/installChirpstack1.png" alt="Install Chirpstack Step 1" class="operation-image">

4. 安裝完成後，使用以下指令檢查 Docker 容器是否正在執行：
   ```bash
   docker ps
   ```

---

### **步驟 2：登入 ChirpStack 管理界面**
1. 打開瀏覽器，前往：
   ```
   http://{LinxdotIP}:8080
   ```
   將 `{LinxdotIP}` 替換為您的 Linxdot Freedom 閘道設備的 IP 位址。
2. 使用默認帳號和密碼登入：
   - **帳號**：`admin`
   - **密碼**：`admin`
3. 登入後，在 ChirpStack 管理界面中新增一個閘道，這將生成一組 `gateway_id`。複製此 ID 以便在下一步中使用。

---

### **步驟 3：配置 LoRa Packet Forwarder**
1. 打開終端機。
2. 編輯 LoRaWAN 全局配置文件：
   ```bash
   vi /etc/lora/global_conf.json.sx1250.AS923
   ```
3. 找到以下行：
   ```json
   "gateway_ID": "8888880000000000"
   ```
   將 `8888880000000000` 替換為步驟 2 中複製的 `gateway_id`。
4. 儲存並退出文件。
5. 執行 LoRa Packet Forwarder 安裝腳本：
   ```bash
   cd /etc/linxdot-opensource/
   ./install-lora-pkd-fwd.sh
   ```
6. 安裝完成後，進入 ChirpStack 管理界面檢查閘道是否已連線。

---

## **最後說明**
完成上述步驟後，您的 Linxdot Freedom 閘道設備將完整配置為支援 ChirpStack 的 LoRaWAN 服務。請確保閘道配置符合您的網路需求，並透過 ChirpStack 管理界面驗證設備連線情況。

如需進一步協助，請參考官方 Linxdot 或 ChirpStack 文檔。
