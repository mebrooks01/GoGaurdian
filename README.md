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
 
__**This is a place holder and needs to be rewriten to be more user freindly**__

### Step 1. Create a Bootdrive

create a bootable media with a usb(lightweight linux distro)

### Step 2. Enter Recovery Mode 

 then press esc +refresh+power

### Step 3. Switch to Dev Mode

then press ctrl+h then j then k then l then press it should say OS verification is off. this is your new start up screen.  
then press ctrl L if it does not boot into chrome os then this will not work (would say your administrator has disabled developer mode)  

### Step 4. Bash Magic

once you are in chrome OS press ctrl alt T type in shell. then "sudo bash" then type "crossystem dev_boot_usb=1 dev_boot_legacy=1"  

### Step 5. Boot from USB Drive

it will now boot from the usb drive  
  
then we restart  
  
put in the usb flash drive before it boots  
  
start it up then spam ctrl L  
then press esc  
choose the usb that you inserted  

### Step 6. Finishing Up

DO NOT INSTALL LINUX  
  
also you are on a different OS so there would not be any GoGuardian. wanna get back into chrome os just reboot then remove usb drive then press ctrl c boom your in  
  
also doing this clears all of your files


## Fuck Chromebooks and get a windows system

If both of these dont work this is your last opption
Pretty Simple go buy a windows laptop or maybe find one for almost free localy.
