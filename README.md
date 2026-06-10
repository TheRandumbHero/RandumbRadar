<p align="center">
<img src="/images/RandumbRadar_Logo.png" alt="RR_Logo" style="width:200px;"/>


Theres a few of these online now and I wanted to add my own flair to my own so I set about designing my own code (with the help of ChatGPT) and my own 3D printed case. Whilst this is not a fork or remix it is heavily inspired by @github/arvis91/
The idea was to see whether I could create my own Desktop Radar software with a 3D printed case that only uses friction fit for all the componants and if possible to make it plug and play with no requirement for soldering if you weren't confident. 

Design wise the screen mount is designed around the one I ordered which I have listed below but I have some more coming from AliExpress (to reduce cost) to see if these also fit.

So without further ado please see below!

## Parts List

- 3D Printed Case - [RandumbPrints - Makerworld.com](https://makerworld.com/en/@RandumbPrints)
- ESP32 with header pins - [Amazon UK](https://www.amazon.co.uk/dp/B0DJPZHZ1X?ref=ppx_yo2ov_dt_b_fed_asin_title)
- TFT with header pins - [Amazon UK](https://www.amazon.co.uk/dp/B0DT984Z9V?ref=ppx_yo2ov_dt_b_fed_asin_title)
- Dupont Connectors - [Amazon UK](https://www.amazon.co.uk/Dupont-Female-Solderless-Breadboard-Connectors/dp/B0BLZC3SQ2/ref=sr_1_6?crid=1N48W8881BTLS&dib=eyJ2IjoiMSJ9.yO14LOzrEFclwHQoAP1I5R_AqWJmElwnY-s6Chap6Nf3qBMTf7ESx-EkYT8xGrqkQw4bbDe4enhwPIrw-g919VpkVx5kIrJsKYqTTBkKMXH2P-XUV5DUOkfNFw2QYHIsTopmBv-QdSh0RMkzKQH-8KR5ouC7fmyOKEFMsvllDlSz8q2EGwoTZcyGCsvalM7KBVngKamGn5y9vHFGnqwnnxS79tSjkrRlGSWPzK56BoS7BYhjL63rFF1wPvbQU_HBZVdk2F-k4IAj_cqEIqeT3535cnueO_pIwJDvWQlVm44.-1rOHTg9zxuN4XeC-vnmEvAW5YwQztgF8GetUKX1xRY&dib_tag=se&keywords=dupont+connectors+female&qid=1781080377&sprefix=dupont+connectors+female%2Caps%2C143&sr=8-6) *Optional if you would like to go solderless

# Connecting & Building:

1. Print the case whilst waiting for the parts to arrive.
2. Once you have the case and parts connect the ESP to the TFT using the pin layout below (I used different colours to differenitate but you don't have to do this)
3. Place the Screen into the mount.
4. Push Bars into the slots to hold screen in place (These have been designed as rectangles not squares so will fit better one way than the other
5. Feed board and wires through the main cabinet opening
6. Place the bottom of the screen mount in first at an angle and then push up to click the screen mount into place.
7. Push ESP32 Board into mount on the base
8. Slide cabinet ontop of base.


## Pin Layout
 <div align="center">

  | TFT (Screen Pins)          | ESP32 (Board Pins)       |
  |      :-:     |      :-:     |
  | RST          | D4           |
  | CS           | D5           |
  | DC           | D2           |
  | SDA          | D23          |
  | SCL          | D18          |
  | GND          | GND          |
  | VCC          | 3V3          |
</div>

# Webflasher

> [!CAUTION]
> By Flashing your ESP32 it will wipe any other app you currently have running - I would advice unplugging any other ESP's you may have plugged in just incase you select the wrong COM Port.

Connect the ESP32 to your PC with a USB-C cable and head to [LINK](https://therandumbhero.github.io/RandumbRadar/) this will open up a webflasher - Flash your ESP32 and wait for it to complete.

# Initial Setup

Once the ESP32 boots up for the first time, it will create a Wifi Access Point called RandumbRadar, connect to this on your phone/laptop. Head to 192.168.77.1 on your browser and enter your home WIFI details. You'll get a confirmation page and the device will reboot.

<p align="center">
  <a href="/images/Initial_Setup.png">
    <img src="/images/Initial_Setup.png" width="180" alt="Initial">
  </a>

# First Setup

The Screen should now be displaying a local IP address, so back on your home WIFI you should be able to go to that address and start the first set up. The First thing you need to do is go to [opensky](https://opensky-network.org/) and create an account, once done, on your account page you'll see an option to create an API key. Click this and it will download a file to your PC, there you'll find the ID and Secret. Now head to that IP address you seen on your Radar Screen and click settings. Paste your Client ID and Client Secret into the corresponding boxes (without the speech marks or any other formatting) and click Save. The system will take a few minutes and then start the next scan. The long/lat defaults are Heathrow Airport at a 200km range so expect to see alot of dots first time round!

<p align="center">
  <a href="https://github.com/TheRandumbHero/RandumbRadarOS/blob/main/images/OpenSky_Options.png">
    <img src="/images/OpenSky_Options.png" width="180" alt="OpenSky">
  </a>

  <a href="/images/OpenSky_Options.png">
    <img src="/images/OpenSky_Creds.png" width="180" alt="Creds">
  </a>

  <a href="/images/OpenSky_Options.png">
    <img src="/images/Setting_OpenSky.png" width="180" alt="Settings">
  </a>
</p>

# Customisation

Now is the fun stuff. Head back to the Dashboard, Click Customisations and go crazy! Update your Lon/Lat and range to suit and I've included a couple of customisations options within the app. I hope to add more in the future.

<p align="center">
  <a href="/images/Customisation.png">
    <img src="/images/Customisation.png" width="180" alt="Initial">
  </a>

  <a href="/images/Green_Custom.png">
    <img src="/images/Green_Custom.png" width="180" alt="Green">
  </a>

  <a href="/images/Blue_Custom.png">
    <img src="/images/Blue_Custom.png" width="180" alt="Blue">

  <a href="/images/Red_Custom.png">
    <img src="/images/Red_Custom.png" width="180" alt="Red">
  </a>
   
  </a>
</p>
