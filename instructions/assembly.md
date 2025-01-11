## Gopher assembly process.

### First, check out and order required [parts and tools](parts_and_tools.md).

You don't have to use exactly the parts i used - but make sure that your parts will fit to the casing.
For example, threaded inserts holes are 4mm, count on that.
The rotary encoder is pretty specific, but it's widely accessible.
Same goes to ESP32-S3 board. Make sure it has sticking antenna - the casing made for it. You'll find over9000 clones on Amazon, and mostly (!) they will be decent. Just make sure the board works before proceeding.

### Prepare guts

- Bridge buttons on Respeaker Lite to corresponding pins (`USR` to `D2`, `Mute` to `D3`).
- Bridge `IN-OUT` and `RGB` with solder on ESP board.
- Solder the male Jst 2.0 Ph 2-Pin Connector to the speaker. Keep the cable short, ~3cm.
- Solder the female Jst 2.0 Ph 2-Pin Connector to the Respeaker Lite. You will find corresponding pads on Respeaker board near the soldered JST connector (marked + and -). Check the cables polarity. Make the cable long, so it sticks from the bottom of main casing, when Respeaker is on top (~12cm).
- Cut 43 LED long piece of WS2812 strip. Make sure it will fit LED diffuser slot nicely. Start from round hole, and move clockwise when placing the strip into diffuser.
- Solder cables of 3-wire connector male part to the LED strip. Keep these cables ~5cm long. Check the wiring. I prefer to color-code (5v -> red, GND -> black, data -> other colour).
- Solder cables of 3-wire LED connector female part to the ESP board. Make these cables ~7cm long.
  - power -> `5V`
  - ground -> `GND`
  - data -> `GPIO13`
- Solder the rotary encoder to ESP board. Make sure cables length is enough for mounting, but not too long.
  - `+` -> `5V`
  - `GND` -> `GND`
  - `SW` -> `GPIO20`
  - `CLK` -> `GPIO47`
  - `DT` -> `GPIO21`
- Solder all Respeaker Lite pins to the ESP board. This will take some time.
  - Check pinout on [this image](images/respeaker-esp-pinout.jpg).

#### At this stage, you can [install the firmware](software.md), connect the peripherals and check that everything works.
