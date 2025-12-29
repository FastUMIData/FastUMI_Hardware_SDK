# FastUMI Hardware sdk

## 📁 Directory Structure

```
xv/				      # fast umi
├── doc/                             # Hardware Related Resources
├── scripts/                         # sdk installation script
├── install-ros1.sh                  # Installation of the sdk and ros1 Function Pack
    ├── install-ros2.sh              # Installation of the sdk and ros2 Function Pack
    ├── install-python.sh            # Installation of the SDK and Python Environment
    ├── multi-support.sh             # Expand USB bandwidth to support multi-device operating environments
├── sdk/			      # Hardware Installation Pack
    ├── XVSDK_focal_amd64_XXX.deb    # ROS1 Version
    ├── XVSDK_jammy_amd64_XXX.deb    # ROS2 Version
vive/				      # vive
├── doc/                             # vive usage profiles 
```

### 文件说明

| Files | Features | Use Cases |
|------|------|---------|

---

## 🚀 Quick Start

### Prerequisites

1. **ROS Environment Installation**
   ```bash
   #Recommend ROS1 neotic
   wget http://fishros.com/install -O fishros && . fishros
   ```
---

## 📖 Use Guides (Single/Double Device Universal)

1. **Installing the SDK**
   ```bash
   cd xv/scripts/
   #ros1 Version(recommended)
   sudo -E bash install-ros1.sh ../sdk/XXX/XVSDK_focal_amd64_XXX.deb
   ```
   
   ```bash
   cd xv/scripts/
   #ros2 Version
   sudo -E bash install-ros2.sh ../sdk/XXX/XVSDK_jammy_amd64_XXX.deb
   ```

2. **Connecting FastUMI**
   ```bash
   cd ~/catkin_ws/
   roslaunch xv_sdk xv_sdk.launch

   ```
   
3. **Extending USB bandwidth (optional, must be done first when multiple devices are used)**
   ```bash
   #The terminal automatically restarts after execution
   sudo -E bash multi-support.sh
   ```
   
3. **Checking FastUMI Status**
Sampling analysis of device collection data can be performed via [FastUMI Monitor Tool] (https://github.com/FastUMIRobotics/FastUMI_Monitor_Tool) to see if the device‘s operational status is normal.
---



## 🔍 Troubleshooting

### Problem: SDK roslaunch startup fails

**Check：**
Delete the related process and restart the SDK.


