##  **Attach new display to ubuntu unity based desktop**  
Example i want to connect a monitor of 1360x768 resolution.

``` cvt 1360 768 60 ``` 

this will report the following configurations 

``` 
# 1360x768 59.80 Hz (CVT) hsync: 47.72 kHz; pclk: 84.75 MHz
Modeline "1360x768_60.00"   84.75  1360 1432 1568 1776  768 771 781 798 -hsync +vsync
 ```

Here copy all the content after Modeline 

```xrandr --newmode "1360x768_60.00"   84.75  1360 1432 1568 1776  768 771 781 798 -hsync +vsync```

This will create a new mode. 

```xrandr --query | grep connected```

Find the display name.

```xrandr --addmode DVI-0 "1360x768_60.00"```

Add the new mode.

```xrandr --output DVI-0 --mode "1360x768_60.00"```

Apply the resolution. 

reference [page at askubuntu](http://askubuntu.com/questions/189246/how-set-my-monitor-resolution)	 
