# HomeAssistant - SamsungTV Tizen Component

***Enable SmartThings***
---------------

**Warning: It is very important to follow this guide to the letter, many users do not follow it correctly and (for example) they try adding the "Device Network ID" instead of `device_id`, then say the component does not work. So follow this guide EXACTLY as it is written!**

Step 1: Make sure your TV is logged into your smart things account.

Step 2: Obtain an API key from https://account.smartthings.com/tokens

Step 3: Go [here](https://graph-eu01-euwest1.api.smartthings.com/device/list) for your device id for each device. Click on the name of your TV and the device id will be in the URL:

https://graph-eu01-euwest1.api.smartthings.com/device/show/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX

Step 4: In your `configuration.yaml` add:

```
media_player:
  - platform: samsungtv_tizen
    name: My TV name
    api_key: "YOUR API KEY"
    device_id: "YOUR DEVICE ID"
    ...
```
