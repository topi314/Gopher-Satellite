## Installing the Gopher firmware

### Flashing DFU software to Respeaker Lite

Your Respeaker Lite board comes pre-flashed with some software. However, most probably it's software, built to use the board as external microphone for computer over USB. There's also chance that the flashed firmware is intended for usage over I2S (which we need), but is using 16kHz sample rate (which we don't, as Gopher is using 48kHz sample rate for better sound playback).

To flash Respeaker board with correct software, you can take the software from the [official repo](https://github.com/respeaker/ReSpeaker_Lite/tree/master/xmos_firmwares) and [instructions from Seeed site](https://wiki.seeedstudio.com/xiao_respeaker/#flash-the-i2s-firmware).

#### _Please re-insert the board after flash and make sure that displayed version is correct one._

### Flashing ESPHome configuration to ESP32-S3 board

There's a configuration available: [dashboard](/config/gopher-dashboard.yaml). Also you will need to copy [base config YAML](/config/common/gopher-base.yaml) into `common` directory in your ESPHome root folder. Alternatively, you can copy everything from `gopher-base.yaml` to the chosen config and merge everything inside.

Build the firmware with ESPHome and flash it with your method of choice.

### Connecting to Home Assistant

- I'm sure you already know how to connect ESPHome devices to Home Assistant. If it's your first time, please check the [official documentation](https://www.home-assistant.io/integrations/esphome/).
- In case of Factory firmware you will need to connect the device to the WiFi first. Check [Improv docs](https://www.home-assistant.io/integrations/improv_ble/) for details.
  _**(When asked to authorize by pressing button on device, use small round button!)**_
- The voice satellite onboarding wizard will help you setup the pipeline and wake word.

### _Happy tinkering!_
