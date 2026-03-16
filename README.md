# 🖥️ myrktop - Luckfox Aura (EV1126B) System Monitor

🔥 **myrktop** is a lightweight system monitor for **Luckfox Aura (EV1126B / RV1126B)**, providing real-time information about **CPU, NPU, VENC (video encoder), RAM, and system temperatures**.

## **📥 Installation Instructions**
### **1️⃣ Install Required Dependencies**
Before running the script, install dependencies to fetch readings:
```bash
sudo apt update && sudo apt install -y python3 python3-pip lm-sensors smartmontools && sudo sensors-detect --auto && pip3 install urwid
```

### **2️⃣ Download and Install myrktop**
Run the following command to download and install the script:
```bash
wget -O ~/myrktop.py https://raw.githubusercontent.com/Sermus/myrktop/refs/heads/luckfoxaura/myrktop.py
wget -O /usr/local/bin/myrktop https://raw.githubusercontent.com/Sermus/myrktop/refs/heads/luckfoxaura/myrktop
```
Then, make the script executable:
```bash
sudo chmod +x /usr/local/bin/myrktop
```

### **3️⃣ Run the Monitoring Script**
To run the script use:
```bash
myrktop
```

---

## **📊 Features**
- **Real-time CPU load & frequency monitoring (per core)**
- **NPU usage & frequency** (via devfreq at `22000000.npu`)
- **VENC (video encoder) usage & frequency** (via devfreq at `21f40000.rkvenc`)
- **RAM & Swap usage**
- **System temperature readings**
- **Network interfaces: Down/Up readings**
- **Storage Usage (/etc/fstab)**
- **NVMe & ATA Storage Info**

> **Note:** This board does not have a discrete GPU or RGA debug interface. GPU and RGA sections are automatically hidden.

---

## **📌 Example Output**
```bash
──────────────────────────────────────────────────
🔥 System Monitor
──────────────────────────────────────────────────
Device: rockchip,rv1126b-evb1-v11rockchip,rv1126b
System Uptime: up 2 hours, 15 minutes
──────────────────────────────────────────────────
📊 CPU Usage & Frequency:
Core 0:   5%  800 MHz   Core 1:   3%  800 MHz
──────────────────────────────────────────────────
🧠 NPU Load: 0%    800 MHz
──────────────────────────────────────────────────
🎬 VENC Load: 0%    550 MHz
──────────────────────────────────────────────────
🖥️  RAM & Swap Usage:
RAM Used: 128Mi / 256Mi
Swap Used: 0B / 0B
──────────────────────────────────────────────────
🌡️  Temperatures:
soc_thermal-virtual-0          35°C
──────────────────────────────────────────────────
🌐 Network Traffic:
eth0: Down 0.10 Mbps | Up 0.05 Mbps
──────────────────────────────────────────────────
💾 Storage Usage (/etc/fstab):
Mount Point             Total     Used     Free
/                        7.2G     1.1G     5.7G
──────────────────────────────────────────────────
No ATA devices detected.
──────────────────────────────────────────────────
Press 'q' to exit. Use arrows or mouse to scroll.
```

---

## **🔧 How to Contribute**
If you find a bug or want to improve **myrktop**, feel free to fork the repository and submit a pull request.

📂 **GitHub Repository:** [https://github.com/Sermus/myrktop](https://github.com/Sermus/myrktop)

---

## **❓ Support**
If you have any issues, open an issue on GitHub, or contact me!

---

### **🔗 License**
This project is **open-source** and available under the **MIT License**.
