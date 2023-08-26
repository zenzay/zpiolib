zpiolib
========

Using the pigpio library to create some sensors and what-not.

This project grew out of a wish to switch from using the RPi.GPIO library to using the pigpio library.

It was also a way for me to learn a bit about class inheritance in Python and how importing packages work.

I created this in 2019, and cleaned it up a bit, before uploading it to Github in 2023.


Installation
=============

python3 -m pip install --upgrade pip
pip3 install build

sudo apt update
sudo apt install pigpio python3-venv
sudo systemctl enable pigpiod.service
sudo systemctl start pigpiod.service

cd src
python3 -m build

This command should output a lot of text and once completed should generate two files in the dist directory:

dist/
├── example_package_YOUR_USERNAME_HERE-0.0.1-py3-none-any.whl
└── example_package_YOUR_USERNAME_HERE-0.0.1.tar.gz

The tar.gz file is a source distribution whereas the .whl file is a built distribution. Newer pip versions preferentially install built distributions, but will fall back to source distributions if needed.

cd dist

python3 -m pip install --no-deps zpiolib
