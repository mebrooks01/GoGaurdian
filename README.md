# Bypassing GoGaurdian

This should work on any chromebook as of Febuary 2021. If it is not working you can send me a message on discord and I can try to help you (Mebrooks01#3354) or send me a message on github.

## Disclaimer 

Do this at your own risk I hold no responsiblity if you fuck up and brick your chromebook. 

## Your Options

You have 3 opptions to deal with it and I will go into as much detail about them as I can.

## Using Inspect 

Most schools have disabled developer tools on there chromebooks `Crt + Shift + I`  but if you are one of the lucky ones that can use inspect your in luck. There is a very easy way for you to get around GoGaurdian. 

Go to [chrome://extensions/](chrome://extensions/) The make sure you have turned on deveolper mode. 
![Where to turn on dev mode](https://i.imgur.com/KJhqkEb.png)

(For this example I will use a different extention but this will work for all of them) \
Once you have dev mode on scroll down to GoGaurdian once you find it there will be a spot that says `backround page` 

![Background Page](https://imgur.com/kAOBpeQ.png)
Click on it and it will open a new window that looks like this 
![Console](https://imgur.com/JwtcOiI.png)

When you have this open you you will then want to type out 
```javascript
window:close()
```
then hit enter and boom the window will close and GoGuardian is gone. But you will need to do this everytime you start your chromebook.

## Reinazlite Chrome OS 

### Step 1. Create a Bootdrive

You will need to create a bootable USB Drive with linux on it (I would use [mint](https://www.linuxmint.com/) but any distro will work)\
To start go download the ISO file for your linux distro (If you are using mint you can get it [here](http://linuxfreedom.com/linuxmint/linuxmint.com/stable/20.1/linuxmint-20.1-cinnamon-64bit.iso). Once you have the ISO file downloaded you will need to go to the Chrome Web Store and install the [Chromebook Recovery Utility](https://chrome.google.com/webstore/detail/chromebook-recovery-utili/jndclpdbaamdhonoechobihbbiimdgai?utm_source=chrome-app-launcher-info-dialog) Then launch the application it should something like this.
![Chrome Recovery Utility](https://imgur.com/eqK8nI1.png)

You will now want to click on the settings icon in the upper right corner and then click Use Local Image
![Use Local Image](https://imgur.com/iQj3Vck.png) and then find the ISO file you downloaded earlyer if you cant find it make sure your browzing for all files 

On chrome OS
![Show All files](https://imgur.com/HU3aJYa.png)

On Windows
![Show All files](https://imgur.com/JgZ3g5u.png)

Now that you have found and selected the ISO file you will need to plug in your USB drive and select it then Click continue and wait it will let you know when its done.

### Step 2. Enter Recovery Mode 

Now you need to boot the chromebook in recovery mode to do this you will hold the `esc` and `reload` (the 4th key to the left) buttons then you will hit the power button and it will take a sec and then boot into a recovery mode and it will look like this
![Chrome recovery mode](https://imgur.com/TKclj6q.png)

### Step 3. Switch to Dev Mode

Now that you are in recovery mode we need to switch it to dev mode to do this me will hit `Crt` and then `D` this will open a screen asking if you want to turn off OS verification you will need to hit `enter` now it will ask you to turn it back on but if hit `enter` this will but it in Dev mode. if when you do this it says dev mode is disabled this will not work for you.

### Step 4. Bash Magic

If all of this has worked once you have loaded into chrome OS you can hold `ctr` and `alt` then hit `T` this will open a terminal window where you will want to type 
```bash
sudo bash
```
then hit enter and type 
```bash
crossystem dev_boot_usb=1 dev_boot_legacy=1
```
this will let you boot from USB

### Step 5. Boot from USB Drive

Now that we have set everything up you can turn off the chromebook and plug in the USB drive. Then turn on the chromebook and hold `ctr` and spam `L` then you want to hit `esc` and select the USB device you have installed linux on.

### Step 6. Finishing Up

**__DO NOT INSTALL LINUX__**
  
This will be an OS running linux and will not have GoGuardian if you ever want to go back to chrome OS just turn off the computer and remove the USB drive and boom your back.

## Fuck Chromebooks and get a windows system

If both of these dont work this is your last opption
Pretty Simple go buy a windows laptop or maybe find one for almost free localy.
