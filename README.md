# Nebula370
Config for my Nebula370 Mercury One Printer
 Update Klipper Ebb36: 
 cd ~/klipper
 make menuconfig
    [*] Enable extra low-level configuration options
        Micro-controller Architecture (STMicroelectronics STM32)  --->
        Processor model (STM32G0B1)  --->
        Bootloader offset (8KiB bootloader)  --->
        Clock Reference (8 MHz crystal)  --->
        Communication interface (CAN bus (on PB0/PB1))  --->
    (1000000) CAN bus speed
    ()  GPIO pins to set at micro-controller startup

make -j4
~/klippy-env/bin/python3 ~/katapult/scripts/flash_can.py -i can0 -f ~/klipper/out/klipper.bin -u af1be5c02d14