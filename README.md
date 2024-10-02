# STM32BluePill-Bootloader //Đang không đc không biết bị sao
    https://www.youtube.com/watch?v=ReSaV4y2XSA
# STM32BluePill-CanBoot
![image](https://github.com/user-attachments/assets/c2a43043-669e-4a44-9f1f-2c35110a200a)

![image](https://github.com/user-attachments/assets/4bca120e-6616-4192-866f-397e68faf9f2)

Kết nối vào Can tranceiver (dung 5V cho Vcc - 3.3 V không thử)
     ~/klippy-env/bin/python ~/klipper/scripts/canbus_query.py can0

![image](https://github.com/user-attachments/assets/637a0ae4-cedf-46a0-9114-c1885833f68e)

# Configure Klipper firmware
Open the config interface of the Klipper firmware with following commands:

    cd ~/klipper

    make menuconfig

and set the following settings:

Enable extra low-level configuration options: check

Micro-controller Architecture: STMicroelectronics STM32

Processor model: STM32G0B1

Bootloader offset: No bootloader (without CanBoot)

Bootloader offset: 8KiB bootloader (with CanBoot)

Clock Reference: 8 MHz crystal

Communication interface: CAN bus (on PB0/PB1)

CAN bus speed: 500000

The result should look like this:

![image](https://github.com/user-attachments/assets/7dd5ef49-a9c3-417b-bec3-4d8cd22ec745)


