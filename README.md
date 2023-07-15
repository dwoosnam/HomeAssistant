# Home Assistant
I currently am using [Home Assistant](https://www.home-assistant.io/) ([OS](https://www.home-assistant.io/installation/alternative)) inside of an [ESXi](https://www.vmware.com/uk/products/esxi-and-esx.html) virtual machine that's running on [Lenovo ThinkStation P340](https://www.lenovo.com/gb/en/p/workstations/thinkstationp/thinkstation-p340-tiny/33ts3tp340t) (i7 10th) tiny PC.

I'm sharing a handful of my configuration items here.

## TTS Package
Providing you have the [Alexa Media Player Custom Component](https://github.com/custom-components/alexa_media_player) installed from [HACS](https://hacs.xyz/) in your Home Assistant install, you should be able to place the `tts_package.yaml` into your packages folder and get the same setup as me.
This package includes:

 - Custom Sensor entities to allow for randomised TTS (seasonal) greeting, inturruption and alert messages.
 - Custom Input Select entities to allow for easier selection of Alexa TTS voices (English speaking only).
 - Custom script to make calling the `notify.alexa_media` player service easier from within your automations.
 - Automation to allow the manual sending of TTS notifications from the Lovelace dashboard.

***You will need to edit the yaml configuration manually to compensate for media_player entities.***

## TTS Manual Lovelace Card
The `tts_manual_lovelace.yaml` file should give you the lovelace dashboard to allow for manual input of TTS requests.
You will require:

 - [Mushroom Cards](https://github.com/piitaya/lovelace-mushroom)
 - [Lovelace Card Mod](https://github.com/thomasloven/lovelace-card-mod)
