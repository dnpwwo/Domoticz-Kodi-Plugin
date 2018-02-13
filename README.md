# Domoticz-Kodi-Plugin
Full version of Kodi Python Plugin for Domoticz home automation

Controls a single Kodi on your network.  If you have more than one you can create multiple instances of the plugin via the Hardware page, one per Kodi.

## Key Features

* Creates four Domoticz devices per Kodi
  1. Basic status indicator, On/Off. Also has icon for Kodi Remote popup.
  2. Selector switch for content source: Video, Music, TV Shows, Live TV.
  3. Volume level.  Icon mutes/unmutes, slider shows/sets volume.
  4. Playing indicator: Icon Pauses/Resumes, slider shows/sets percentage through media.
* Ships with 3 different, user selectable, icons sets: Default, Black and Round.
* Will send onscreen notifications to the Kodi if a Notifier name is specified.
* When network connectivity is lost the Domoticz UI will optionally show the device(s) with Red banner

## Installation

Python version 3.4 or higher required & Domoticz version 3.87xx or greater.

To install:
* Go in your Domoticz directory using a command line and open the plugins directory.
* Run: ```git clone https://github.com/dnpwwo/Domoticz-Kodi-Plugin.git```
* Restart Domoticz.

In the web UI, navigate to the Hardware page.  In the hardware dropdown there will be an entry called "Kodi Players".

## Updating

To update:
* Go in your Domoticz directory using a command line and open the plugins directory then the Domoticz-Kodi-Plugin directory.
* Run: ```git pull```
* Restart Domoticz.

## Configuration

### Kodi

The Kodi itself must be set to allow it to be controlled by external programs. Google will tell you how to do that.

### Domoticz

| Field | Information|
| ----- | ---------- |
| IP Address | Will handle DNS names and IP V4 addresses (e.g 192.168.xxx.xxx) |
| Port | The port that the Kodi is listening on. Default 9090, will work unless you specifically changed it on your Kodi.  Do not set this to 80 or 8080. The plugin does not use a web interface on the Kodi |
| Icon | Dropdown to allow icon set selection |
| Notifications | If true it will send notifications to the Kodi that will popup on the screen |
| Notifier Name | Only used if 'Notifications' is true. This name will appear in the list of notification targets when you use the 'Notifications' Button. Notifications you send to this target will appear on screen |
| Time Out Lost Devices | When true, the devices in Domoitcz will have a red banner when network connectivity is lost to the Kodi |
| Debug | When true the logging level will be much higher to aid with troubleshooting |

## Change log

| Version | Information|
| ----- | ---------- |
| 1.9.0 | Initial upload version |
| 2.0.6 | Add support for GUI.Screensaver events |
| 2.1.6 | Add option to activate Screensaver on 'Shutdown' or 'Off' |
| 2.2.1 | "Sleep" option changed to use UDP ActivateScreensaver call |
| 2.2.3 | Bug fix: Source selector selecting wrong source. Added 'Weather' source. |
