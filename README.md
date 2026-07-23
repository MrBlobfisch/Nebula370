# Nebula370
Config for my Nebula370 Mercury One Printer

Update klipper mcu:
cd ~/klipper
make menuconfig
[*] Enable extra low-level configuration options
    Micro-controller Architecture (STMicroelectronics STM32)  --->
    Processor model (STM32H723)  --->
    Bootloader offset (No bootloader) --->
    Clock Reference (25 MHz crystal)  --->
    Communication interface (USB (on PA11/PA12))  --->
    USB ids  --->
()  GPIO pins to set at micro-controller startup

make -j4
make flash -j4 FLASH_DEVICE=/dev/ttyACM0


check connection:  ~/klippy-env/bin/python ~/klipper/klippy/console.py /dev/serial/by-id/usb-Klipper_stm32h723xx_1F0014000851323235363233-if00