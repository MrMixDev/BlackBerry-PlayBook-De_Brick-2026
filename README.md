RIM Blackberry Playbook De-Brick.
If you reset your blackberry playbook tablet then it will get bricked at the agreement where no country's show up so if you have a working playbook DO NOT RESET IT OR ELESE IT WILL BE BRICKED!!! 

but if you did reset it or if it was never set up or you forgot the password on it 
then here's how to fix it 

Note: only tested on the 16gb Blackberry Playbook WI-FI AND ALSO NOTE THAT I WILL NOT BE HELD RESPONSABLE IF YOU BRICK YOUR PLAYBOOK BECAUSE IF YOU FOLOW THIS GUIDE AND FAIL THEN THATS YOUR PROBROM AND NOT MINE SO DONT COME TO ME WITH PICHFORKS AND TOURCHES IF YOU SCREW UP AND ARE FLOWOING THIS GUIDE!!! Also note that you should watch this vid that i did not make and DONT FOLLOW THE STEPS JUST WATCH IT AND OBSERVE SO THAT YOU CAN SEE HOW ITS DONE "https://www.youtube.com/watch?v=adFwuF9Wv6k".

The autoloaders I have found for this guide that have the setup bypassed where from this guide "https://www.reddit.com/r/PlayBook/comments/1phmro3/downgrade_and_root_your_blackberry_playbook_in/"  

Step 1
Install Blackberry Desktop Software from "https://archive.org/details/black-berry-desktop-software-7.1_202605", THIS IS NESSACEREY AS NOT DOING THIS STEP WILL RESALT IN ALL OF THE OTHER STEPS FAILING!!!

Step 2

Plug in The Playbook. IF YOU DONT DO THIS THEN THIS WILL NOT WORK AND MAKE SHURE YOU ARE USEING A GOOD HIGH QUALTY MICROUSB DATA CABLE!!!

Step 3 


To de-brick and keep it on the latest version 2.1.0.1917 Download and Run "PlayBook_2.1.0.1917.modded.exe" From "https://archive.org/download/playbook-root-downgrade-1.0/2.1.0.1917/".  DO NOT AND I MEAN DO NOT UNDER ANY CURCANSTANCE UNPLUG THE PLAYBOOK UNTILL THE WINDOW CLOSES AND THE PLAYBOOK BOOTS TO THE HOME SCREEN. IF YOU DO THEN YOUR SCREWED AND YOU SHOUD HATE YOURSELF FOREVER!!!

Step 4 

To Install apps you need an old version of chromium that is in this repo and the browser extension to go with it

Download and extract "win_764946_chrome-win.zip from https://archive.org/download/win-764946-chrome-win"
go to the chrome-win Folder
run chrome.exe
ignore any api key errors
install the extension by going to "chrome://extensions/" and enable developer mode and drag & drop "PBManager-(DO_NOT_EXTRACT).zip" DO NOT EXTRACT THIS ZIP FILE BECAUSE IT WILL NOT WORK AND ITS NOT NECESSARY!

Step 5 

If it does not open a window automatically then click on pb manager in chrome.

Step 6 

On the PlayBook go to "Settings>>Security>>Development Mode>>Use Development Mode>>Enter a passcode of your choice (I Used 1234)"

Step 7 

Under "Device Hostnames/IPs: (BB10: Settings » About » Network » Wi-Fi or USB » IPv4)" Enter The PlayBook IP. You can find the Ip under "Settings » About » Network » Wi-Fi or USB » IPv4"

Step 8

Click on "YOUR _PLAYBOOK_IP_ADDRESS" Under "Manage your device:"

Step 9 

Ignore Security Error

Step 10

Enter the password you set in step 6 for your PlayBook and hit "Log in"

Step 11

Click On Install APPS and select the ".bar or .BAR" file you want to install 

step 12 

Wait

Step 13

If you made it here then congratulations you have de-bricked your PlayBook and now you can use it again like its 2013. But If You Want to watch youtube then you have to host a thing called YT2009 using docker

Step 1 
Install Docker 


curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh


Step 2 
Clone the repo

git clone https://github.com/ftde0/yt2009.git
cd yt2009

Step 3
Build The Image

docker build -t yt2009  .

Step 4
Run the Image

docker run -d \
  --name playbook-youtube \
  -p 8080:80 \
  -e YT2009_IP="192.168.40.100" \
  -v yt2009-data:/data \
  --restart unless-stopped \
  yt2009

Step 5

On The Playbook go to the browser app and put 

HTTP://<YOUR_SERVER_IP>:8080

Step 6 
Enjoy!




 






