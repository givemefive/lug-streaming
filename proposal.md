

lug streaming setup
-------------

### hardware:
  * streaming laptop 
  * hdmi cloner
  * hdmi to usb3 device
  * web cam
  * audio mixer / soundcard
  * microphone?
    * hand held
    * clip on / ear


### sources:

video sources:
  * web cam of overall presentation (wide view of presenter)
  * projector output from presenter's notebook fed into hdmi to usb3 device
  
audio sources:
  * notebook
  * microphones

### targets: 
  * rtmp server like youtube
  * disk

### fact-finding

determine capabilities of hardware

  * encoding capability of notebook 
  * hardware glitches / bugs in linux


### software:
#### shell
---
Some configuration of system and reloading of system/software will be needed to get hardware/drivers to cooperate.
#### gstreamer
---
Gstreamer is advantageous because prototyping can be done using gst-launch.  Then C can be used to create a program that will implement required functionality.

### development strategy:
---

create most simple implementation possible. the most important feature in this project is reliability. we do not want the meeting delayed because of technical issues due to streaming.  
hdmi->usb3 -> h264 encoder -> mux -> rtmp sink


Use this simple pipe line and make the system robust to any action the user could do while plugging in hardware or playing/pausing/restarting the stream.


Add any essential features for usability.


Revisit more complicated features like on screen text, video scenes, picture-in-picture, audio selection mixing, audio dsp, etc.

### personnel:

I can work on it throughout the summer.  I would need access to the hardware during scheduled periods.  Goal would be to have project complete by first meeting in the Fall.
