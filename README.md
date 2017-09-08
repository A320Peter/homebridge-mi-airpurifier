# homebridge-mi-airpurifier
[![npm version](https://badge.fury.io/js/homebridge-mi-airpurifier.svg)](https://badge.fury.io/js/homebridge-mi-airpurifier)

XiaoMi air purifier plugins for HomeBridge.   
Thanks for [nfarina](https://github.com/nfarina)(the author of [homebridge](https://github.com/nfarina/homebridge)), [OpenMiHome](https://github.com/OpenMiHome/mihome-binary-protocol), [aholstenson](https://github.com/aholstenson)(the author of [miio](https://github.com/aholstenson/miio)), [licuhui](https://github.com/licuhui), all other developer and testers.   

**Note: I have only a part of these devices, so some devices don't have tested. If you find bugs, please submit them to [issues](https://github.com/YinHangCode/homebridge-mi-airpurifier/issues) or [QQ Group: 107927710](//shang.qq.com/wpa/qunwpa?idkey=8b9566598f40dd68412065ada24184ef72c6bddaa11525ca26c4e1536a8f2a3d).**   

![](https://raw.githubusercontent.com/YinHangCode/homebridge-mi-airpurifier/master/images/AirPurifier.jpg)
![](https://raw.githubusercontent.com/YinHangCode/homebridge-mi-airpurifier/master/images/AirPurifier2.jpg)
![](https://raw.githubusercontent.com/YinHangCode/homebridge-mi-airpurifier/master/images/AirPurifierPro.jpg)

## Supported Devices
1.AirPurifier(小米空气净化器)   
2.AirPurifier2(小米空气净化器2)   
3.AirPurifierPro(小米空气净化器Pro)   

## Pre-Requirements
1.Make sure your IOS version is ios11 or later.   

## Installation
1. Install HomeBridge, please follow it's [README](https://github.com/nfarina/homebridge/blob/master/README.md).   
If you are using Raspberry Pi, please read [Running-HomeBridge-on-a-Raspberry-Pi](https://github.com/nfarina/homebridge/wiki/Running-HomeBridge-on-a-Raspberry-Pi).   
2. Make sure you can see HomeBridge in your iOS devices, if not, please go back to step 1.   
3. Install packages.   
```
npm install -g miio homebridge-mi-airpurifier
```

## Configuration
```
"platforms": [{
    "platform": "MiAirPurifierPlatform",
    "deviceCfgs": [{
        "type": "AirPurifier",
        "ip": "192.168.88.xx",
        "token": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
        "airPurifierName": "AirPurifier",
        "airPurifierSilentModeName": "AirPurifier Silent Mode Switch",
        "temperatureDisable": false,
        "temperatureName": "Temperature",
        "humidityDisable": false,
        "humidityName": "Humidity",
        "buzzerSwitchDisable": true,
        "buzzerSwitchName": "AirPurifier Buzzer Switch",
        "ledBulbDisable": true,
        "ledBulbName": "AirPurifier LED Switch",
        "airQualityDisable": false,
        "airQualityName": "AirQuality"
    }, {
        "type": "AirPurifier2",
        "ip": "192.168.88.xx",
        "token": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
        "airPurifierName": "AirPurifier",
        "airPurifierSilentModeName": "AirPurifier Silent Mode Switch",
        "temperatureDisable": false,
        "temperatureName": "Temperature",
        "humidityDisable": false,
        "humidityName": "Humidity",
        "buzzerSwitchDisable": true,
        "buzzerSwitchName": "AirPurifier Buzzer Switch",
        "ledBulbDisable": true,
        "ledBulbName": "AirPurifier LED Switch",
        "airQualityDisable": false,
        "airQualityName": "AirQuality"
    }, {
        "type": "AirPurifierPro",
        "ip": "192.168.88.xx",
        "token": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
        "airPurifierName": "AirPurifier",
        "airPurifierSilentModeName": "AirPurifier Silent Mode Switch",
        "temperatureDisable": false,
        "temperatureName": "Temperature",
        "humidityDisable": false,
        "humidityName": "Humidity",
        "buzzerSwitchDisable": true,
        "buzzerSwitchName": "AirPurifier Buzzer Switch",
        "ledBulbDisable": true,
        "ledBulbName": "AirPurifier LED Switch",
        "airQualityDisable": false,
        "airQualityName": "AirQuality"
    }]
}]
```

## Get token
Open command prompt or terminal. Run following command:
```
miio --discover
```
Wait until you get output similar to this:
```
Device ID: xxxxxxxx   
Model info: Unknown   
Address: 192.168.88.xx   
Token: xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx via auto-token   
Support: Unknown   
```
"xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx" is token.   
If token is "???", then reset device and connect device created Wi-Fi hotspot.   
Run following command:   
```
miio --discover --sync
```
Wait until you get output.   
For more information about token, please refer to [OpenMiHome](https://github.com/OpenMiHome/mihome-binary-protocol) and [miio](https://github.com/aholstenson/miio).   

## Version Logs
### 0.0.1
1.support for XiaoMi AirPurifier.   
2.support for XiaoMi AirPurifier2.   
3.support for XiaoMi AirPurifierPro.   
