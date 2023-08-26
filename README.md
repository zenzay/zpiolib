zpiolib
========

Using [the pigpio library](http://abyz.me.uk/rpi/pigpio/) to create some sensors and what-not.

This project grew out of a wish to switch from using the RPi.GPIO library to using the pigpio library.

It was also a way for me to learn a bit about class inheritance in Python and how importing packages work.

I created this in 2019, and cleaned it up a bit, before uploading it to Github in 2023.

I'm not bothering with documenting the different classes or adding comments in the source. This was just a project for me to learn new stuff - and the examples should suffice, if I should want to use the library for something in the future.

## Installing and enabling the pigpio library
```
sudo apt update
sudo apt install pigpio -y
sudo systemctl enable pigpiod.service
sudo systemctl start pigpiod.service
pip3 install pigpio
```

## Installing zpiolib
```
sudo apt install python3-venv
python3 -m pip install --upgrade pip
pip3 install build

git clone https://github.com/zenzay/zpiolib
cd zpiolib/src
python3 -m build
pip3 install --no-index ./dist/zpiolib-0.0.1-py3-none-any.whl
```
