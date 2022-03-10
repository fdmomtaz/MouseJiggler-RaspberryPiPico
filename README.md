# Mouse Jiggler : Raspberry Pi Pico

A mouse jiggler software written in c using the Raspberry Pi Pico software and the TinyUSB library.

The mouse jiggler moves your mouse in random patterns every half a second in order to keep your computer active.

## How To Build 
You can build the code using the `CMake` build system. 
The software requires the following libaraies in order jiggle your mouse:
- PicoSDK
- TinyUSB

You can follow the steps in the [Raspberry Pi Pico Starting Guide](https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf) to set up your development machine.

Following the following steps to build the code:
```
mkdir build
cd build

cmake ../src
make
```

Note: Don't forget to set the `PICO_SDK_PATH` in your environment variables.

## How To Deploy
Please follow the following steps to deploy the compiled binaries into your Rapsberry Pi Pico.
1) Buy a Raspberry Pi Pico
2) Download the [generated UF2 file](https://github.com/fdmomtaz/MouseJiggler-RaspberryPiPico/releases/download/v1.0/mouse-jiggler.uf2) from releases OR build it as described in section "How To Build"
3) Hold the "BootSel" button while connecting the Pico to the computer
4) Drag and drop the UF2 file to the device
5) Congrats your mouse will move around ;)

Here is a short video explaining the process:
[![How To Upload](https://img.youtube.com/vi/W4Bp1pWsgLo/maxresdefault.jpg)](https://youtu.be/W4Bp1pWsgLo)

## Credit
This software was modified from the [TinyUSB](https://docs.tinyusb.org/en/latest/) HIB example. The project and CMake was created using the [Pico Project Generator](https://github.com/raspberrypi/pico-project-generator).
