## Installing the Gopher firmware

### Flashing DFU software to Respeaker Lite

To flash Respeaker board with correct software, you can use [included sowtware](/respeaker_lite_i2s_dfu_firmware_48k_v1.1.0.bin) (or take one with version >= 1.1.0 and 48kHz sample rate from [official repo](https://github.com/respeaker/ReSpeaker_Lite/tree/master/xmos_firmwares)) with [instructions from Seeed site](https://wiki.seeedstudio.com/xiao_respeaker/#flash-the-i2s-firmware).

#### _Please re-insert the board after flash and make sure that displayed version is correct one._

### DFU software auto-update
Since version 2025.2.2, the Koala firmware includes corresponding DFU firmware for Respeaker Lite board. On first start after update, new firmware will be installed to Respeaker automatically. You will see Respeaker LED flashing yellow, while installing, and green on successful install.
So now there's no need to update DFU firmware. Woohoo!

### Flashing ESPHome configuration to ESP32-S3 board

There's a configuration available: [dashboard](/config/gopher-dashboard.yaml). Also you will need to copy [base config YAML](/config/common/gopher-base.yaml) into `common` directory in your ESPHome root folder. Alternatively, you can copy everything from `gopher-base.yaml` to the chosen config and merge everything inside.

Build the firmware with ESPHome and flash it with your method of choice.

### Connecting to Home Assistant

- I'm sure you already know how to connect ESPHome devices to Home Assistant. If it's your first time, please check the [official documentation](https://www.home-assistant.io/integrations/esphome/).
- In case of Factory firmware you will need to connect the device to the WiFi first. Check [Improv docs](https://www.home-assistant.io/integrations/improv_ble/) for details.
  _**(When asked to authorize by pressing button on device, use small round button!)**_
- The voice satellite onboarding wizard will help you setup the pipeline and wake word.

### Using the alarm functionality.
Since 2025.4.1, the device has built-in alarm, that you can setup and use in your smart home. Check [this short tutorial](https://github.com/formatBCE/Respeaker-Lite-ESPHome-integration/blob/ae414e06fea8334e726837d5dbe72a55645b3445/readme/alarms.md) on how to set it up!

### _Happy tinkering!_
