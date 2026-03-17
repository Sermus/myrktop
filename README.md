# 🖥️ myrktop - BananaPi M5 Pro (RK3576) System Monitor

🔥 **myrktop** is a lightweight system monitor for **BananaPi M5 Pro (RK3576)**, providing real-time information about **CPU, GPU, NPU, RAM, RGA, and system temperatures**.

> This is a fork adapted for **BananaPi M5 Pro (RK3576)**. The original project targets Orange Pi 5 (RK3588): [mhl221135/myrktop](https://github.com/mhl221135/myrktop).

## **📥 Installation Instructions**
### **1️⃣ Install Required Dependencies**
Before running the script, install dependencies to fetch readings:
```bash
sudo apt update && sudo apt install -y python3 python3-pip lm-sensors smartmontools nvme-cli && sudo sensors-detect --auto && pip3 install urwid
```

### **2️⃣ Download and Install myrktop**
Run the following command to download and install the script:
```bash
wget -O ~/myrktop.py https://raw.githubusercontent.com/Sermus/myrktop/refs/heads/bananapim5pro/myrktop.py
wget -O /usr/local/bin/myrktop https://raw.githubusercontent.com/Sermus/myrktop/refs/heads/bananapim5pro/myrktop
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
- **Live GPU usage & frequency**
- **NPU & RGA usage**
- **RAM & Swap usage**
- **System temperature readings**
- **Network interfaces: Down/Up readings**
- **Storage Usage (/etc/fstab)**
- **NVMe & ATA Storage Info**

---

## **📌 Example Output**
```
──────────────────────────────────────────────────
🔥 System Monitor
──────────────────────────────────────────────────
Device: armsom,sige5rockchip,rk3576
NPU Version: RKNPU driver: v0.9.6
System Uptime: up 2 days, 2 hours, 46 minutes
──────────────────────────────────────────────────
📊 CPU Usage & Frequency:
Core 0:   0% 2208 MHz   Core 1:   0% 2208 MHz
Core 2:   0% 2208 MHz   Core 3:   0% 2208 MHz
Core 4:   0% 2304 MHz   Core 5:   0% 2304 MHz
Core 6:   0% 2304 MHz   Core 7:   0% 2304 MHz
──────────────────────────────────────────────────
🧠 NPU Load: 0% 0%   1000 MHz
──────────────────────────────────────────────────
🖼️  RGA Load: 0% 0%
──────────────────────────────────────────────────
🖥️  RAM & Swap Usage:
RAM Used: 544Mi / 7.7Gi
Swap Used: 9.8Mi / 4.0Gi
──────────────────────────────────────────────────
🌡️  Temperatures:
npu_thermal-virtual-0          49°C
little_core_thermal-virtual-0  50°C
soc_thermal-virtual-0          49°C
gpu_thermal-virtual-0          50°C
ddr_thermal-virtual-0          49°C
bigcore_thermal-virtual-0      49°C
──────────────────────────────────────────────────
🌐 Network Traffic:
wlan1: Down 0.00 Mbps | Up 0.00 Mbps
end0: Down 0.00 Mbps | Up 0.00 Mbps
wlan0: Down 0.00 Mbps | Up 0.00 Mbps
end1: Down 0.00 Mbps | Up 0.00 Mbps
──────────────────────────────────────────────────
💾 Storage Usage (/etc/fstab):
Mount Point             Total     Used     Free
/oem                     123M      12M     108M
/userdata                 44G      40G     4.5G
──────────────────────────────────────────────────
No ATA devices detected.
──────────────────────────────────────────────────
Press 'q' to exit. Use arrows or mouse to scroll.
```

---

## **🔧 How to Contribute**
If you find a bug or want to improve **myrktop**, feel free to fork the repository and submit a pull request.

📂 **GitHub Repository:** [https://github.com/Sermus/myrktop](https://github.com/Sermus/myrktop/tree/bananapim5pro)

---

## **❓ Support**
If you have any issues, open an issue on GitHub, or contact me!

---

### **🔗 License**
This project is **open-source** and available under the **MIT License**.

