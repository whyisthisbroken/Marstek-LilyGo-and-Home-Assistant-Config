
# 🚀 ESPHome Installation & Flashing Guide  
### For LilyGO T-Display RS485 (T-CAN485) & Marstek Battery Integration

This guide explains how to install ESPHome on **Windows or Linux** and flash it onto a **LilyGO T-Display RS485** (also known as T-CAN485) to communicate with **Marstek RS485 batteries** using a custom ESPHome configuration.

---

## 🛠️ Requirements

- Python 3.8 or higher (on Windows or Linux)
- USB-C cable
- LilyGO T-CAN485 development board
- ESPHome YAML configuration file (e.g. `marstekbattery.yaml`)
- Internet connection (for dependency installation)

---

## 💻 Installation

### ✅ Windows

Open a terminal (CMD or PowerShell):

```bash
# Step 1: Upgrade pip
python -m pip install --upgrade pip

# Step 2: Install or update ESPHome
pip3 install esphome --upgrade

# (Optional) Step 3: Upgrade PlatformIO (used by ESPHome)
python -m pip install -U platformio
```

---

### 🐧 Linux (Ubuntu/Debian-based)

Open a terminal:

```bash
# Step 1: Install Python and pip
sudo apt update
sudo apt install -y python3 python3-pip

# Step 2: Upgrade pip
python3 -m pip install --upgrade pip

# Step 3: Install or update ESPHome
pip3 install --user esphome --upgrade

# (Optional) Step 4: Upgrade PlatformIO
python3 -m pip install -U platformio
```

> 💡 **Note:** If `esphome` is not found after installation, add `~/.local/bin` to your `PATH`.

---

## ⚙️ ESPHome Commands

Below are useful commands for managing and flashing your ESPHome project.

```bash
# Show installed ESPHome version
esphome version

# Clean previous build files
esphome clean marstekbattery.yaml

# Compile only (no flashing)
esphome compile marstekbattery.yaml

# Compile and flash via USB
esphome run marstekbattery.yaml
```

> 💡 **Note:** The first flash must be done via USB. Subsequent uploads can be done over-the-air (OTA).

---

## 🔌 Flashing Tips

### USB Flashing (First-Time)

1. Connect the LilyGO board to your PC using a USB-C cable.
2. If the board is not detected:
   - Hold the **BOOT** button while plugging in the board.
   - Release BOOT once connected.
3. Run:
   ```bash
   esphome run marstekbattery.yaml
   ```

### Specify Port Manually (if needed)

```bash
# Example for Windows:
esphome run marstekbattery.yaml --device COM3

# Example for Linux:
esphome run marstekbattery.yaml --device /dev/ttyUSB0
```

---

## 📡 After Flashing

Once the initial USB flash is successful:

- The device will connect to Wi-Fi (as configured in your YAML).
- It will be available for **OTA updates**.
- You can now manage it from the **ESPHome Dashboard** or via command line:
  ```bash
  esphome dashboard
  ```

---

## 📚 Useful Resources

- 🔗 [ESPHome Documentation](https://esphome.io)
- 🔗 [Mushroom UI Cards (Lovelace)](https://github.com/piitaya/lovelace-mushroom)
- 🔗 [LilyGO T-CAN485 GitHub Repository](https://github.com/Xinyuan-LilyGO/T-Display-S3)
- 🔗 [Marstek RS485 Battery Integration](https://github.com) *(insert your repo link here)*

---

## 🧪 Troubleshooting

- **Permission error on Linux**  
  Add your user to the `dialout` group and reconnect the device:
  ```bash
  sudo usermod -aG dialout $USER
  ```

- **Device not found?**  
  Use `esphome run marstekbattery.yaml --device /dev/ttyUSBx` or `COMx` to specify manually.

- **OTA upload failing?**  
  Reboot the device manually, verify Wi-Fi config, or reflash via USB.

---

## 📄 License

MIT – Free to use, share, and modify.

---
