# Linxdot Freedom Revive: Restore Your Gateway

This guide explains how to restore your Linxdot Freedom gateway to its default firmware state using the **Linxdot Freedom Revive** method. Follow these steps carefully to ensure a successful reflash process.

---

## **Requirements**

1. **Hardware**:
   - Linxdot LD1002 gateway.
   - USB cable (preferably the one provided with the gateway).
   - Windows-based PC.

2. **Software**:
   - [Factory Tool Installer](https://linxdot-opensource.v7idea.com/sdk/Linxdot-Factory-tool-Installer.zip) (download and install on your PC).
   - [Latest Firmware Package](https://linxdot-opensource.v7idea.com/images/linxdot-opensource-image-2.0.0.05.tar.gz).

---

## **Step 1: Install the Factory Tool**
1. Download the **Factory Tool Installer** from [this link](https://linxdot-opensource.v7idea.com/sdk/Linxdot-Factory-tool-Installer.zip).
2. Extract the downloaded ZIP file and run the installer.
3. Follow the on-screen instructions to complete the installation.

---

## **Step 2: Download the Latest Firmware**
1. Visit the [firmware download page](https://linxdot-opensource.v7idea.com/images/linxdot-opensource-image-2.0.0.05.tar.gz).
2. Download the firmware package to your PC.
3. Keep the firmware file ready for the reflashing process.

---

## **Step 3: Prepare the Gateway**
1. Power off the Linxdot LD1002 gateway.
2. Locate the **BT Repair Key** at the back of the gateway.
3. Press and hold the **BT Repair Key** while powering on the device.
4. The gateway will enter **reflash mode**, indicated by the Factory Tool detecting the device as connected.

---

## **Step 4: Flash the Firmware**
1. Open the installed Factory Tool on your PC.
2. Confirm that the tool detects the gateway as connected.
3. Select the previously downloaded firmware file (`linxdot-opensource-image-2.0.0.05.tar.gz`).
4. Start the reflashing process by clicking the appropriate button in the Factory Tool.
5. Wait for the process to complete without interruptions.

---

## **Step 5: Restart the Gateway**
1. Once the firmware upload is successful, disconnect the USB cable.
2. Restart the Linxdot LD1002 gateway.
3. The device will boot up with a clean system running Linxdot Freedom firmware.

---

## **Next Steps**
After restoring the firmware:
- Install **ChirpStack** on your Linxdot LD1002 to enable LoRaWAN services.
- Refer to the ChirpStack installation guide for detailed instructions.

---

## **Troubleshooting**
- If the Factory Tool does not detect the device:
  - Ensure the gateway is in **reflash mode**.
  - Check the USB cable and port connection.
  - Reinstall the Factory Tool and drivers.

- If the reflashing process fails:
  - Retry the process.
  - Ensure the firmware file is not corrupted.

---

## **Final Notes**
Reflashing your Linxdot LD1002 resets it to factory settings. Make sure to back up any custom configurations before proceeding. For further assistance, refer to the Linxdot support team or official documentation.

---

**Disclaimer**: Proceeding with the firmware reflash may void your warranty if done incorrectly. Always use official tools and firmware packages.

---

# Linxdot Freedom Revive：恢復您的閘道設備

本指南將說明如何使用 **Linxdot Freedom Revive** 方法將 Linxdot Freedom 閘道恢復到默認韌體狀態。請仔細按照以下步驟操作，以確保重新燒錄過程成功。

---

## **需求條件**

1. **硬體**：
   - Linxdot LD1002 閘道設備。
   - USB 連接線。
   - 基於 Windows 的電腦。

2. **軟體**：
   - [Factory Tool Installer](https://linxdot-opensource.v7idea.com/sdk/Linxdot-Factory-tool-Installer.zip)（下載並安裝至您的電腦）。
   - [最新韌體包](https://linxdot-opensource.v7idea.com/images/linxdot-opensource-image-2.0.0.05.tar.gz)。

---

## **步驟 1：安裝 Factory Tool**
1. 從[此連結](https://linxdot-opensource.v7idea.com/sdk/Linxdot-Factory-tool-Installer.zip)下載 **Factory Tool Installer**。
2. 解壓縮下載的 ZIP 文件並運行安裝程式。
3. 按照螢幕上的指示完成安裝。

---

## **步驟 2：下載最新韌體**
1. 訪問[韌體下載頁面](https://linxdot-opensource.v7idea.com/images/linxdot-opensource-image-2.0.0.05.tar.gz)。
2. 將韌體包下載到您的電腦。
3. 將韌體文件準備好以供重新燒錄過程使用。

---

## **步驟 3：準備閘道設備**
1. 關閉 Linxdot LD1002 閘道設備電源。
2. 找到閘道背面的 **BT Repair Key**。
3. 按住 **BT Repair Key** 並打開電源。
4. 設備將進入 **重新燒錄模式**，此時 Factory Tool 會檢測到設備已連接。

---

## **步驟 4：燒錄韌體**
1. 在電腦上打開已安裝的 Factory Tool。
2. 確認工具已檢測到閘道設備已連接。
3. 選擇先前下載的韌體文件（`linxdot-opensource-image-2.0.0.05.tar.gz`）。
4. 點擊 Factory Tool 中的相應按鈕開始重新燒錄過程。
5. 在燒錄過程中保持穩定，避免中斷。

---

## **步驟 5：重新啟動閘道設備**
1. 韌體燒錄成功後，斷開 USB 連接線。
2. 重新啟動 Linxdot LD1002 閘道設備。
3. 設備將啟動並運行乾淨的 Linxdot Freedom 系統。

---

## **後續步驟**
恢復韌體後：
- 在您的 Linxdot LD1002 上安裝 **ChirpStack** 以啟用 LoRaWAN 服務。
- 詳細安裝說明請參閱 ChirpStack 安裝指南。

---

## **疑難排解**
- 如果 Factory Tool 無法檢測到設備：
  - 確保閘道設備處於 **重新燒錄模式**。
  - 檢查 USB 連接線和端口連接是否正常。
  - 重新安裝 Factory Tool 和驅動程式。

- 如果燒錄過程失敗：
  - 重試操作。
  - 確保韌體文件未損壞。

---

## **最終說明**
重新燒錄 Linxdot LD1002 將其重置為出廠設定。在操作前，請確保備份所有自訂配置。如需進一步協助，請聯繫 Linxdot 支援團隊或參考官方文檔。

---

**免責聲明**：如果操作不當，重新燒錄韌體可能會使您的保固失效。請始終使用官方工具和韌體包。
