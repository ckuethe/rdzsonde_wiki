# OLED/TFT display configuration

## Screen config (0=automatic, 1-5=predefined, other=custom).
Selects the screen layout file to be used (value X selects file screensX.txt)
Value 0 makes an automated selection based on other configuration parameters:
Display type OLED (SSD1306 or SH1106): screens1.txt
Display type ILI9225: Orientation 1 or 3 (landscape): screens2.txt, otherweise (portrait) screens3.txt
Display type ILI9341/9342: Orientation 1 or 3 (landscape): screens4.txt, otherwise (portrait) screens5.txt

Make sure to select a screens file that fits to your hardware config.
Other custom screen files can be created, uploaded, and selected here.

(Selecting a different screen config probably requires rebooting the TTGO.)

## Display screens
Defines which screens from the screen layout file (screensX.txt) should be used. On the left, all entries from the screens#.txt file are shown. Enter a list of numbers. The first number should be a "Scan" layout. After that, you can put a sequence of numbers corresponding to screens you can cycle through with a button.

## No-RX-timeout
If set to -1, screen will remain active forever even if no signal is received anymore. Any other value X will cause the TTGO to switch back to Scan mode after X seconds (assumes that the screens#.txt contains "N" as the timer action value)

## TFT orientation
You can use this value to rotate the TFT display (0=portrait, 1=landscape, 2=portrait rotated 180°, 3=landscape rotated 180°.
For the OLED display, 0,1,2 all mean "normal", 3 means "rotated 180°". 90° rotation is not supported on the OLED display.
