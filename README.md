# Welcome to My Proficiency Technical Institute

# Google Assistant for Raspberry Pi Boards  

# Updated At 17-Sep-2018


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


  3.4. USB MIC AND AUDIO JACK users,  
  ```  
  sudo chmod +x /home/pi/GassistPi/audio-drivers/USB-MIC-JACK/scripts/usb-mic-onboard-jack.sh  
  
  sudo /home/pi/GassistPi/audio-drivers/USB-MIC-JACK/scripts/usb-mic-onboard-jack.sh  
  
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
7. Execute the installers (When Prompted, enter your Google Cloud console Project-Id, A name for your Assistant and the Full Name of your credentials file, including the json extension.)  
	```
	sudo  /home/pi/GassistPi/scripts/gassist-installer-pi3.sh  
	
	```
*************************************************  
 **HEADLESS AUTOSTART on BOOT SERVICE SETUP**  
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
