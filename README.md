Work in Progress



# 🔐 SDN-Based Dynamic Firewall (C++ + Ryu)

This project is a high-performance, software-defined dynamic firewall system using:
- **C++** for firewall logic (speed and memory efficiency)
- **Ryu** controller for SDN flow management
- **Mininet** for network emulation
- **Python scripts** for traffic generation and testing

---

## 📁 Project Structure

sdn-dynamic-firewall/
├── controller/ # Ryu/POX SDN controller logic

├── firewall_engine/ # C++ firewall logic with  communication handlers

├── topology/ # Mininet topology and setup scripts

├── test/ # Traffic generation and attack simulations

├── gui/ # (Optional) Flask dashboard for real-time monitoring

├── benchmarks/ # Performance tests (latency, memory)

├── logs/ # Log files (flows, blocked IPs)

├── docs/ # Report, diagrams, presentation

---

## 🚀 Features

- Dynamically block malicious flows (e.g., port scans, DoS)
- C++-based decision engine for low-latency flow handling
- Real-time visualization (optional Flask dashboard)
- Supports both TCP and UDP packet detection
- Scalable and extensible for future use (ML, anomaly detection)

---

## ⚙️ Setup Instructions

### 1. Install Python dependencies

```bash
pip install -r requirements.txt

2. Compile the C++ Firewall
    cd firewall_engine/
    mkdir build && cd build
    cmake ..
    make
3. Run Mininet topology
    sudo python3 topology/custom_topology.py
4. Start the Ryu Controller
    ryu-manager controller/ryu_firewall.py
5. Run the C++ firewall logic
    ./firewall_engine/build/firewall
6. (Optional) Launch Flask dashboard
    cd gui/
    python3 app.py
