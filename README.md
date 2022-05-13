# IMP006A Zj-58
IMP006A Zj-58 POS Bluetooth Printer Linux Driver

If you only want use this printer with usb cable just open a terminal and install driver using:
~~~
sudo chmod +x install58
~~~
And next:
~~~
sudo ./install58
~~~
## This is how to configure IMP006A or Zj-58 Bluetooth printer on linux by Bluetooth connection.
### 1
Install driver with:
~~~
sudo chmod +x install58
~~~
and  next:
~~~
sudo ./install58
~~~
### 2 
  Install cups with:
~~~
sudo apt install cups
~~~
### 3 
  Install bluez-cups with:
~~~
sudo apt install bluez-cups
~~~
(This allow cups to use bluetooth protocol)
### 4 
  Sync the bluetooth printer with your computer, use password 1234 or 0000. Or use the default passwords according to your manufacturer.
### 5
  Take a note on bluetooth adress of printer e.g: 0f:08:09:07:0b:08
### 6
  Open http://localhost:631/admin and go to 'add printer'
### 7
  Put your root credentials
### 8
  Select LPD/LPR Host or Printer
### 9
  In URI put bluetooth://0f0809070b08 where "0f0809070b08" is your bluetooth printer adress
### 10
  Select POS58.ppd File if necessary and click 'ADD Printer'
### 11
  Go to the file you want to print or open the system where the printout will be made...
### 12
  Check the paper preset and send it to the print queue.
#### Cups link:
  https://github.com/apple/cups/releases

#### Bluez-cups links:
  https://packages.debian.org/sid/admin/bluez-cups
  
  https://www.archlinux.org/packages/extra/x86_64/bluez-cups/
