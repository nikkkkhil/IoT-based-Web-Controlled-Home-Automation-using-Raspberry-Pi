# IoT-based-Web-Controlled-Home-Automation-using-Raspberry-Pi
To update the raspberry Pi below commands and then reboot the RPi;

sudo apt-get update
sudo apt-get upgrade
sudo reboot


Make sure you are in home directory using;

cd ~


Use wget to get the file from their sourceforge page;

wget http://sourceforge.net/projects/webiopi/files/WebIOPi-0.7.1.tar.gz


tar xvzf WebIOPi-0.7.1.tar.gz
cd WebIOPi-0.7.1/


Below commands are used to install patch while still in the WebIOPi directory, run;

wget https://raw.githubusercontent.com/doublebind/raspi/master/webiopi-pi2bplus.patch
patch -p1 -i webiopi-pi2bplus.patch


Then we can run the setup installation for the WebIOPi using;

sudo ./setup.sh
Keep saying yes if asked to install any dependencies during setup installation. When done, reboot your pi;

sudo reboot


Run the command;

sudo webiopi -d -c /etc/webiopi/config

After issuing the command above on the pi, point the web browser of your computer connected to the raspberry pi to http://raspberrypi.mshome.net:8000 or http;//thepi’sIPaddress:8000. The system will prompt you for username and password.

Username is webiopi
Password is raspberry


After the login, look around, and then click on the GPIO header link.





