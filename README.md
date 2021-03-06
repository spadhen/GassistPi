# Welcome to My Proficiency Technical Institute

# Google Assistant for Raspberry Pi Boards  

# Updated At 17-Sep-2018   Reference of Sid E Classroom


FIRST STEP- CLONE the PROJECT on to Pi

1. Open the terminal and execute the following


```
sudo apt-get install git  
git clone https://github.com/spadhen/GassistPi    
```

1. Update OS and Kernel    

```
sudo apt-get update  
sudo apt-get install raspberrypi-kernel  
```
2. Restart Pi

```
reboot
```

3. Audio configuration


  USB MIC AND AUDIO JACK users  
  ```  
  sudo chmod +x /home/pi/GassistPi/audio-drivers/USB-MIC-JACK/scripts/usb-mic-onboard-jack.sh  
  
  sudo /home/pi/GassistPi/audio-drivers/USB-MIC-JACK/scripts/usb-mic-onboard-jack.sh  
  
  speaker-test  
  ```
  
  USB MIC AND HDMI users  
  ```  
  sudo chmod +x ./GassistPi/audio-drivers/USB-MIC-HDMI/scripts/configure.sh  
  sudo ./GassistPi/audio-drivers/USB-MIC-HDMI/scripts/configure.sh  
  
  sudo reboot  
    
  
  sudo chmod +x ./GassistPi/audio-drivers/USB-MIC-HDMI/scripts/install-usb-mic-hdmi.sh  
  sudo ./GassistPi/audio-drivers/USB-MIC-HDMI/scripts/install-usb-mic-hdmi.sh  
  
  speaker-test  
  ```

4. Restart Pi

```
reboot
```

5. Check the speaker using the following command    

```
speaker-test -t wav  
```  

6. Make the installers Executable  

	```
	sudo chmod +x /home/pi/GassistPi/scripts/gassist-installer-pi3.sh
	
	```
	Or if you are using raspberry pi Zero
	```
	sudo chmod +x /home/pi/GassistPi/scripts/gassist-installer-pi-zero.sh

	```
7. Execute the installers (When Prompted, enter your Google Cloud console Project-Id, A name for your Assistant and the Full Name of your credentials file, including the json extension.)  
	```
	sudo  /home/pi/GassistPi/scripts/gassist-installer-pi3.sh  
	
	```
	Or if you are using raspberry pi Zero
	```
	sudo  /home/pi/GassistPi/scripts/gassist-installer-pi-zero.sh  

	```
*************************************************  
 **HEADLESS AUTOSTART**  
*************************************************  
1. Open the service files in the /home/pi/GassistPi/systemd/ directory and add your project and model ids in the indicated places and save the file.

2. Make the service installer executable  

```
sudo chmod +x /home/pi/GassistPi/scripts/service-installer.sh
```  

3. Run the service installer  

```
sudo /home/pi/GassistPi/scripts/service-installer.sh    
```  

4. Enable the services  
```
sudo systemctl enable gassistpi-ok-google.service  
sudo systemctl enable gassistpi-push-button.service
```  

5. Start the service  
```
sudo systemctl start gassistpi-ok-google.service  
sudo systemctl start gassistpi-push-button.service
```  

**RESTART and ENJOY**  

Tip: To Run any appliction on Auto start on boot of raspberry Pi 
Just Open file:
$ sudo nano /etc/profile
and at the end add you command line than save and exit and restart your pi
