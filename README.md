<p align="center"><img src="https://i.imgur.com/DIpuNTI.jpg"></p>

<p align="center">
    <a href="https://twitter.com/thewhiteh4t">
      <img src="https://img.shields.io/badge/-TWITTER-black?logo=twitter&style=for-the-badge">
    </a>
    &nbsp;
    <a href="https://twc1rcle.com/">
      <img src="https://img.shields.io/badge/-THE WHITE CIRCLE-black?logo=&style=for-the-badge">
    </a>
    &nbsp;
    <a href="https://thewhiteh4t.github.io/">
      <img src="https://img.shields.io/badge/-BLOG-black?logo=dialogflow&style=for-the-badge">
    </a>
</p>

<p align="center">
  <br>
  <b>Available in</b>
  <br>
  <img src="https://i.imgur.com/1wJVDV5.png">
</p>


Concept behind Seeker is simple, just like we host phishing pages to get credentials why not host a fake page that requests your location like many popular location based websites. Read more on <a href="https://github.com/Rahulkilaparthi/Location-seeker.git"> thewhiteh4t's Blog </a>.Seeker Hosts a fake website which asks for Location Permission and if the target allows it, we can get :

* Longitude
* Latitude
* Accuracy
* Altitude - Not always available
* Direction - Only available if user is moving
* Speed - Only available if user is moving

Along with Location Information we also get **Device Information** without any permissions :

* Unique ID using Canvas Fingerprinting
* Device Model - Not always available
* Operating System
* Platform
* Number of CPU Cores - Approximate Results
* Amount of RAM - Approximate Results
* Screen Resolution
* GPU information
* Browser Name and Version
* Public IP Address
* Local IP Address
* Local Port

**Automatic IP Address Reconnaissance** is performed after the above information is received.

**This tool is a Proof of Concept and is for Educational Purposes Only, Seeker shows what data a malicious website can gather about you and your devices and why you should not click on random links and allow critical permissions such as Location etc.**

## How is this Different from IP GeoLocation

* Other tools and services offer IP Geolocation which is NOT accurate at all and does not give location of the target instead it is the approximate location of the ISP.

* Seeker uses HTML API and gets Location Permission and then grabs Longitude and Latitude using GPS Hardware which is present in the device, so Seeker works best with Smartphones, if the GPS Hardware is not present, such as on a Laptop, Seeker fallbacks to IP Geolocation or it will look for Cached Coordinates.  

* Generally if a user accepts location permsission, Accuracy of the information recieved is **accurate to approximately 30 meters**

* Accuracy depends on multiple factors which you may or may not control such as :
  * Device - Won't work on laptops or phones which have broken GPS
  * Browser - Some browsers block javascripts
  * GPS Calibration - If GPS is not calibrated you may get inaccurate results and this is very common

## Templates

Available Templates : 

* NearYou
* Google Drive (Suggested by @Akaal_no_one)
* WhatsApp (Suggested by @Dazmed707)
* Telegram
* Zoom (Made by @a7maadf)
* Google reCAPTCHA (Made by @MrEgyptian)

Create your own template ! 
Steps to let you create your template is described in this [how-to](./createTemplate.md)

Once your template is ready, **do not forget to propose it to the community via a PR (pull request)**

## Tested On :

* Kali Linux
* BlackArch Linux
* Ubuntu
* Fedora
* Kali Nethunter
* Termux
* Parrot OS
* OSX - Monterey v.12.0.1

## Installation

### Kali Linux

```
$Sudo su (root kali)
$https://github.com/Rahulkilaparthi/Location-seeker.git
$cd seeker
$sudo ./install.sh
$sudo python3 seeker.py
$(Select tamplate)
$-2
$Give logo title 
#Profile pic(download image in jpg format and paste it in desktop and open properties and copy path way of image) 
#Like – paste that path way in kali 
$Home/desktop/logo.png(name)
#After that  change tab:
#Download cloudflared .deb from browser
	$Sudo apt install  gdebi
	$(Go to download folder go to properties of cloudflared go to edit and install pkg)
	$Cloudflared -url localhost:8080

```


