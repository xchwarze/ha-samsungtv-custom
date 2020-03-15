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


***Benefits of Enabling SmartThings***
---------------

- Better states for running apps (read [app_list guide](https://github.com/jaruba/ha-samsungtv-tizen/blob/master/App_list.md) for more information)
- New keys available (read more below about [SmartThings Keys](https://github.com/jaruba/ha-samsungtv-tizen/blob/master/Smartthings.md#smartthings-keys))
- Shows TV channel names
- Shows accurate states for HDMI or TV input sources


***SmartThings Keys***
---------------

*Input Keys*
____________
Key|Description
---|-----------
ST_TV|TV
ST_HDMI1|HDMI1
ST_HDMI2|HDMI2
ST_HDMI3|HDMI3
ST_HDMI4|HDMI4
...

*Channel Keys*
______________
Key|Description
---|-----------
ST_CHUP|ChannelUp
ST_CHDOWN|ChannelDown
ST_CH1|Channel1
ST_CH2|Channel2
ST_CH3|Channel3
...
