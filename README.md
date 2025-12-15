# PanaProxy

Controller for Panasonic Aquarea heat pumps, integrating seamlessly with Home Assistant.

<p align="center">
    <!-- Add device images if available -->
    <!-- <img src="IMAGE_URL_1" alt="PanaProxy" width="30%" /> -->
    <!-- <img src="IMAGE_URL_2" alt="PanaProxy" width="30%" /> -->
</p>

---

## ℹ️ What is PanaProxy?

PanaProxy is a physical device that runs `panasonic_aquarea` from IoTLabs Components. It gives you full control and monitoring of Panasonic Aquarea heat pumps through:
- 📱 Web interface (on the device)
- 🏠 Home Assistant integration (automatic discovery)

Your device comes **pre-loaded and ready to use** – no code or flashing needed. Plus, firmware updates happen automatically – you never need to worry about keeping it current.

---

## � Quick Start

### 1. Connect to Heat Pump

Connect the device to your Panasonic Aquarea heat pump using the provided CN-CNT cable: the device powers automatically from the heat pump

### 2. Connect to Wi-Fi

1. Look for Wi-Fi network: **`IoTLabs PanaProxy`** (no password)
2. Open [`http://192.168.4.1`](http://192.168.4.1) in your browser
3. Select your home Wi-Fi and enter the password
4. Click **Save**

> **Alternative:** Use [Web Tools](https://iotlabs.pl/en/tools) with Improv BLE or Serial

### 3. Open Web Interface

Once connected, find the device's IP address and open `http://<device_ip>` in your browser.

You'll see:
- Current temperature
- Power consumption
- Operation status
- All heat pump controls

### 4. Add to Home Assistant (Optional)

1. Go to **Settings** → **Devices & Services**
2. Accept PanaProxy discovery
3. Heat pump controls now appear in Home Assistant

**Done!** Your device is ready to monitor and control your heat pump.

---

## ❓ FAQ

<details>
<summary>
<h3 style="display:inline-block">Device not showing heat pump data?</h3>
</summary>

1. Verify UART cable is properly connected to both device and heat pump
2. Check device logs in web interface (`http://<device_ip>`) for errors
3. Restart the device
4. If problem persists, check the UART communication using serial debugging

</details>

<details>
<summary>
<h3 style="display:inline-block">Can't connect to Wi-Fi?</h3>
</summary>

1. Restart the device
2. Verify the Wi-Fi password is correct
3. Try connecting from closer to your router
4. Try using Improv Serial via USB instead of the access point

</details>

<details>
<summary>
<h3 style="display:inline-block">Home Assistant not discovering the device?</h3>
</summary>

1. Ensure Home Assistant's **ESPHome integration** is enabled
2. Go to **Settings** → **Devices & Services** → check Discovered devices
3. Restart Home Assistant if needed
4. Verify device and Home Assistant are on the same network

</details>

---

## ⚙️ Advanced Users: Customizing the Firmware

If you want to modify the firmware (add sensors, automations, change behavior, etc.), use **Adopt** in ESPHome Dashboard.

### How to Adopt & Customize

1. **Open ESPHome Dashboard**
2. **Click "Take Control"** on the device
3. **Edit your device config** - add/modify settings as needed
4. **Save & Upload**
