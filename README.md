# STM32BluePill-Bootloader 
    https://www.youtube.com/watch?v=ReSaV4y2XSA

# Canbus phải dùng PB8 (vào TRX của bo TTLToCan)+PB9(vào CTX); PA11+PA12 ko chạy
<img width="697" height="297" alt="image" src="https://github.com/user-attachments/assets/3d562779-ef62-4401-a81d-cdff5405640d" />

Dùng STLink để nạp

<img width="823" height="611" alt="image" src="https://github.com/user-attachments/assets/9e1df737-13a6-48dd-ac13-6fc8393e4d98" />

Lệnh tìm can id

    ~/klippy-env/bin/python ~/klipper/scripts/canbus_query.py can0

Nếu ko chạy thì restart lại Canbus

    sudo ip link set can0 down

    sudo ip link set can0 type can restart

    sudo ip link set can0 type can bitrate 500000 

    sudo ip link set can0 up

# Máy BTT-PAD7 sau khi cài canboot ko phải khởi động lại Canbus nữa.
    cd ~

    git clone https://github.com/Arksine/CanBoot
