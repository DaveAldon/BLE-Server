# BLE-Server

Turn a prototype device into a discoverable BLE GATT server

### Requirements

- Raspberry Pi 3B+ / 4B / Zero W
- iOS/Android running nRF Toolkit app
- BlueZ 5.50+ (latest Raspberry Pi OS Full 32-bit) comes with this version
- Git

### Instructions

1. Install this repo via Git

```
git clone https://github.com/DaveAldon/BLE-Server.git && cd BLE-Server/
```

2. Run the main python script

```
python3 uart.py
```

3. You should get something similar to this output, which means the device is now discoverable

```
$ python3 uart.py
Skip adapter: /org/bluez
GATT application registered
GetAll
returning props
Advertisement registered
```

4. Open the nRF Toolbox app on your phone and tap on “UART”
5. Tap “CONNECT” and the app will start scanning for nearby BLE devices
6. Select your device from the detected device list. It triggers the connection between your device and the app

### Troubleshooting

Restart bluetooth service

```
sudo systemctl restart bluetooth.service
```

### Credit

Files and original instructions adapted from https://web.archive.org/web/20200724062734/https://scribles.net/creating-ble-gatt-server-uart-service-on-raspberry-pi/
