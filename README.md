<img src="branding/midea.png" width="200px">, <img src="branding/homebridge.png" width="150px">

# Homebridge-Midea-Air

[![Downloads](https://img.shields.io/npm/dt/homebridge-midea-air.svg?color=critical)](https://www.npmjs.com/package/homebridge-midea-air)
[![Version](https://img.shields.io/npm/v/homebridge-midea-air)](https://www.npmjs.com/package/homebridge-midea-air)<br>
<a target="blank" href="https://www.paypal.me/hillaliy"><img src="https://img.shields.io/badge/PayPal-Donate-blue.svg?logo=paypal"/></a><br>

[Homebridge](https://github.com/nfarina/homebridge) plugin to control Midea AC units. Still in early development.

<img src="branding/product.jpeg" width="200px">

### Requirements

<img src="https://img.shields.io/badge/node-%3E%3D10.17-brightgreen"> &nbsp;
<img src="https://img.shields.io/badge/homebridge-%3E%3D0.4.4-brightgreen"> &nbsp;
<img src="https://img.shields.io/badge/iOS-%3E%3D11.0.0-brightgreen">

## Configuration

Add this to the platforms array in your config.json:

    {
        "user": "MIDEA_ACCOUNT_EMAIL",
        "password": "MIDEA_PASSWORD",
        "interval": 1,
        "debug": true,
        "devices": [
        	{
        		"deviceId": "DEVICE_ID",
        		"supportedSwingMode": "Both"
        	}
        ],
        "platform": "midea-air"
    }

## Optional per-device Configuration Values

To set specific per-device values, be sure to first look into the Home app to find your deviceId and use it as the key in the devices object

### Supported Swing Mode

"None", "Vertical", "Horizontal", "Both"
You have to select which type your device supports

### Temperature Display Units

Temperature display units can set in the homekit device when you swipe up to device settings.
Display Units values are: FAHRENHEIT, CELSIUS

## Usage

Rotation Speed/Swing mode can set in the homekit device when you swipe up to device settings.
Rotation Speed values are:
0 : device off
-25%: Low
-50%: Middle
-75%: High
-100%: Auto

## Notes

This version of `homebridge-midea-air` is a platform and should be able to access all device in the user's account. However, many devices may not be supported or function incorrectly. This is due to the lack of documentation of the raw MSmart API. If you encounter any problems, please open a new issue and specify your device model.
