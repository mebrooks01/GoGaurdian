# Bypassing GoGuardian

This should work on any Chromebook as of Febuary 2021. If it's not working, you can send me a message on Discord (Mebrooks01#3354) or GitHub and I can try to help you.

## Disclaimer 

Do this at your own risk. I hold no responsiblity if you fuck up and brick your Chromebook. 

## Your options

You have 3 options to deal with it, and I will go into as much detail about them as I can.

### Use Inspect Element

Most schools have disabled Developer Tools on their Chromebooks (<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>I</kbd>), but if yours hasn't, you're in luck. There is a very easy way for you to get around GoGuardian.

Go to [chrome://extensions/](chrome://extensions/), then make sure you have turned on Developer Mode. 

![Where to turn on dev mode](https://i.imgur.com/KJhqkEb.png)

(For this example I will use a different extension but this will work for all of them).

Once you have enabled dev mode, scroll down to GoGuardian. Once you've found it, there will be a spot that says **backround page**:

![Background Page](https://imgur.com/kAOBpeQ.png)

Click on it, and it will open a new window that looks like this:

![Console](https://imgur.com/JwtcOiI.png)

Once you have this open you'll then want to type out:

```js
window.close()
```

Then hit <kbd>Enter</kbd> and boom! The window will close and GoGuardian is gone. But you will need to do this every time you start your chromebook.

### Reinitialize ChromeOS

#### 1. Create a bootdrive

You will need to create a bootable USB Drive with Linux on it (I would use [mint](https://www.linuxmint.com/) but any distro will work). To start, go download the ISO file for your distro (for Mint, you can get it [here](http://linuxfreedom.com/linuxmint/linuxmint.com/stable/20.1/linuxmint-20.1-cinnamon-64bit.iso)). Once you have the ISO file you will need to go to the Chrome Web Store and install the [Chromebook Recovery Utility](https://chrome.google.com/webstore/detail/chromebook-recovery-utili/jndclpdbaamdhonoechobihbbiimdgai?utm_source=chrome-app-launcher-info-dialog). Then, launch the application. It should look something like this.

![Chrome Recovery Utility](https://imgur.com/eqK8nI1.png)

You will now want to click on the settings icon in the upper right corner and then click on **Use local image**

![Use Local Image](https://imgur.com/iQj3Vck.png)

Then, find the ISO file you downloaded earlier. If you can't find it, make sure you're browsing for all files.

On ChromeOS:

![Show all files](https://imgur.com/HU3aJYa.png)

On Windows:

![Show all files](https://imgur.com/JgZ3g5u.png)

Once you've found and selected the ISO file you will need to plug in your USB drive and select it, then click **continue** and wait. It will let you know when it's done.

#### 2. Enter Recovery Mode 

Now, you need to boot the Chromebook in recovery mode. To do this, you will hold the <kbd>Esc</kbd> and <kbd>Reload</kbd> (the 4th key to the left) buttons, then hit the power button. It will take a second and then boot into a recovery mode. It will look like this:

![Chrome recovery mode](https://imgur.com/TKclj6q.png)

#### 3. Switch to Dev Mode

Now that you're in recovery mode, we need to switch to dev mode. To do this, hit <kbd>Ctrl</kbd> + <kbd>D</kbd>. This will open a screen asking if you want to turn off OS verification, you will need to hit <kbd>Enter</kbd>. Now it will ask you to turn it back on, but if you hit <kbd>Enter</kbd> it will in dev mode. If, once you do this, it says that dev mode is disabled, this won't work for you.

#### 4. Bash magic

If all of this has worked, once you've loaded into ChromeOS, you can hold <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>T</kbd>. This will open a terminal window where you will want to type:

```bash
sudo bash
```

Then, hit <kbd>Enter</kbd> and type:

```bash
crossystem dev_boot_usb=1 dev_boot_legacy=1
```

This will let you boot from USB.

#### Step 5. Boot from USB Drive

Now that we have set everything up you can turn off the Chromebook and plug in the USB drive. Then turn it back on and hold <kbd>Ctrl</kbd> and spam <kbd>L</kbd>. Then, you want to hit <kbd>Esc</kbd> and select the USB device you have installed Linux on.

#### Step 6. Finishing up

**__DO NOT INSTALL LINUX__**
  
This will be an OS running Linux, and will not have GoGuardian. If you ever want to go back to ChromeOS, just turn off the computer, remove the USB drive, and boom, you're back.

### Fuck Chromebooks and get a Windows system

If neither of these worked this is your last option.

It's pretty simple. Go buy a Windows laptop or maybe find one for almost free locally.
