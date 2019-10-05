# Random lighting for home made desk lamp with wroom-esp32

    sudo apt-get install -y build-essential tk-dev libncurses5-dev libncursesw5-dev \
    libreadline6-dev libdb5.3-dev libgdbm-dev libsqlite3-dev libssl-dev libbz2-dev \
    libexpat1-dev liblzma-dev zlib1g-dev libffi-dev

     wget https://www.python.org/ftp/python/3.7.0/Python-3.7.0.tgz

    sudo tar zxf Python-3.7.0.tgz
    cd Python-3.7.0
    sudo ./configure
    sudo make -j 4
    sudo make altinstall


    sudo apt install python3-pip
    sudo pip3 install esptool

    dmesg | grep ttyUSB

    esptool.py --port /dev/ttyUSB0 erase_flash

    wget https://micropython.org/resources/firmware/esp32-20190907-v1.11-291-gc69f58e6b.bin

    esptool.py --port /dev/ttyUSB0 write_flash 0x1000 <path to firmware file>

    sudo pip3 install rshell

    rshell --buffer-size=30 -p /dev/ttyUSB0 
    repl
