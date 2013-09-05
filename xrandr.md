Multiple Monitor Setup 
======================

Query the displays for their names and available modes,

`xrandr -q`

To reset the displays,

`xrandr --auto`

Shows each display's optimal (`+`) and current (`*`) resolution "mode". LVDS is the laptop screen, and eg. CRT1 is the external display.

To (turn on) and change the resolution,

`xrandr --output SCREEN_NAME --mode WIDTHxHEIGHT`

To position one display relative to another,

`xrandr --output SCREEN1_NAME --right-of SCREEN2_NAME`

* --above
* --below
* --right-of
* --left-of

(Some setups may not be possible.)

To sort a screen first in RandR and Xinerama,

`xrandr --output SCREEN1_NAME --primary`

It's easiest to set in one command
----------------------------------

`xrandr --output LVDS --mode 1280x720 --pos 0x-720 --output VGA1 --mode 1280x720 --pos 0x0`

