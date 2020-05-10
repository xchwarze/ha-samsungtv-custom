# How to use Alexa to control your Samsung TV

With the initial setup I was able to do only basic voice controls like TV Off or TV Mute with Alexa. Additionally, I had an external soundbar connected to my TV via HDMI and the Volume up / down voice commands only worked with the in-built TV speakers, while they did work when using the Home Assistant UI.
Since there is no clear guide as to how someone can properly integrate the Samsung TV Remote custom component to be used with Alexa, I decided to document my own steps to get it working. There might be an easier way to do this, but following this guide will give you the flexibility to control almost everything via convenient voice commands.

# Prerequisites:

* HomeAssistant installed
* Custom Component installed and able to control Samsung TV over web interface
* Linked Home Assistant to Alexa via HA Cloud (or own implementation)
* Able to execute basic voice controls via Alexa like TV Off, TV Mute
* Optional: add smart things API key to be able to use additional key commands

# How-To

### Step 1: Setup a Home Assistant script to do what you want

#### 1. Send single remote control keys or chain key presses

* In HomeAssistant UI go to Configuration -> Scripts
* Click the plus Icon in the lower right corner and enter a name for your script
* In "Action type" choose "Call service" and choose "media_player.play_media"
* As entitiy choose the Samsung TV Remote component, by default media_player.samsung_tv_remote (**NOT** the default Samsung TV)
* As service data use the following and edit the KEY to the one you want:
    ```
	media_content_id: KEY_CHDOWN
	media_content_type: send_key
    ```
* You can also use a key like KEY_HDMI to switch to HDMI input or KEY_TV / ST_TV (for me personally only the smart things key worked)
* Key chaining with "+" as described in the Readme is possible as well
* Save your script with the save icon

### 2. Start an app

* Get your app id from one of the lists linked in the readme
* If your app id is not in there you have to get it from your TV
	* To do this, go into your configuration.yaml and add the following
		```
		logger:
		  default: warning
		  logs:
		   custom_components.samsungtv_tizen.media_player: debug
		```
	* Restart Home Assistant and check your home-assistant.log - there should be a line where you can get your app ids from
* Again create a script exactly like above, but here choose the following service data (e.g. for Netflix, switch id for your app accordingly):
	```
	media_content_id: 11101200001
	media_content_type: app
    ```
	
## Step 2: Setup Alexa to execute your scripts

1. (Re-)Start Alexa App on your phone
2. Go to devices and discover devices
3. Your scripts will be added as scenes
4. Go to routines and create a new routine
    * choose name and voice command of your liking
    * choose scene (script) to be executed
5. With this method you can basically choose whatever command you want
    * e.g "Alexa, Netflix" to start the Netflix app
    * e.g "Alexa, Live TV" and so on
	
That's it. Enjoy your voice controlled TV.

Note: You can also add additional actions in scripts and for example start an app and then send one or multiple keys inside one script that will be executed by a single voice command.