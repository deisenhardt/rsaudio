# rsaudio
This script is my way of addressing audio issues with MacOS &amp; Google Chrome which originated sometime around the release of Catalina and/or Monterrey.  I first began work on this in Monterrey but have tested it fixes the same root cause in a Catalina system, but I do not remember any similar issues prior to Catalina.  It also works with Ventura & Sonoma. These problems are rarer with Sonoma but not completely gone.

Macs connected to a thunderbolt dock (only tested with TB3 and newer devices, theoretically it could also impact TB2) or with USB (whether 2.0/3.0/3.1/3.2gen2 with either USB-C or USB-A connection) dock, DAC, headset, or other audio device may suffer from suddenly having no audio.  This can be, but is not always related to sleep/suspend. 

Several symptoms that are fixed with this method include:

* The mac audio was fine before going to sleep but since waking/login there is no audio (possibly for one device or for any if there are multiple)

* a video/audio that was streaming when the display went to sleep or screen saver engaged will stop playing arbitrarily afterward, and will remain frozen/no audio on that device after waking.  May also overlap the above symptoms.

* For notebooks, if the charger is disconnected during playback in addition to the above symptoms.

* For macs with a dock (independent of whether the dock provides PD or has a separate power source) if the dock becomes disconnected & reconnects, and (typically labeled USB Audio) sound is present but macOS has no ability to adjust the volume.  In this case, the audio may still work but the inability to adjust the volume is fixed with this method.

* For macs with a DAC or USB mic preamp, it is less common to lose audio output but any of the above can result in noise/grainy audio out.  This method resolves these issues.  This is more likely if the device shows a specific name (such as 'Focusrite Scarlett 4i4' as opposed to 'USB Audio') in the volume adjustment.

* For a USB headset that powers off due to low battery or other hardware timeout, when turning back on either there is audio but no volume adjustment, stuck very low or max volume, or no audio, this method resolves these issues.


There are probably more situations we have encountered but not documented as separate instances. We do not use Bluetooth enough to test anything specific, the one time we encountered an issue with Bluetooth headst Google Chrome needed to be restarted anyway (see below).

This script also has the ability to kill & reopen Google Chrome. While most other apps (Apple Music, Spotify, VLC) typically will pause playback when the issue occurs, or may become frozen but recover once coreaudio is killed (Spotify), Google Chrome often needs to be restarted after the fix.  In this case, referring to the fix may be this script (if killing CoreAudio is needed) or in the case of unplugging a device, plugging back and waiting a moment. Typically if you need to restart Chrome you can tell with any other audio program playback is normal but Chrome will have no sound or distorted audio on any page/tab/service. This will not interfere with your preference of Chrome's behaviour to either reopen tabs/windows, or not.
