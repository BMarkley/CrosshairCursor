# ![materials](/Applet/CrosshairCursor@BMarkley/icon.png) CrosshairCursor ![materials](/Applet/CrosshairCursor@BMarkley/icons/CrosshairCursorStopped.png)
Changes your mouse cursor into a crosshairs that can be used as a productivity or assistive tool. 


![materials](/Images/Screenshot.png)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 Crosshair Cursor - Creates a Crosshair window that follows your cursor.
By Brian Markley PENG RSE 

<Description>
Changes your mouse cursor into a crosshairs that can be used as a productivity or 
assistive tool.

<Compilation note from oneko developers>
"It seems that it won't work if you use gcc as the compiler. (I've confirmed this myself.) For this reason, I've forced the compiler to compile with cc in the new Imakefile."

<Dependencies>

X Window System
X11 shape extension
based on the oneko cat program, so oneko package dependecies are likely all needed:
libc6(>=2.4)
libx11-6
libxext6
psmisc

<How to Compile>

1. First, unshar this article to extract the source code.

2. Create a Makefile. Change to the oneko directory and run % xmkmf. If you don't have this command, you can also run % imake -DUseInstalled -I/usr/lib/X11/config.

3. Run make.

% make

This will create an executable "CrosshairCursor" program. If you want to put it in /usr/bin/X11 and share it with everyone, run

# make install

(as superuser).

Compilation is now complete. All that's left to do is run

For a foreground terminal application:
% CrosshairCursor

For a background application:
% CrosshairCursor &

senjoy :-)

<Release>
Currently in the process of being released as an applet on Linux Mint cinnamon.
Included is a compiled copy of the code which runs on my system.
I think it should be portable to other 64bit systems, but I do not know.

The applet can be manually installed by putting the CrosshairCursor@BMarkley folder 
in ~/.local/share/cinnamon/applets/CrosshairCursor@BMarkley/CrosshairCursor, and 
then activating the applet from the cinamon applet menu.

<Usage>
When run without options a gray and black fullscreen Crosshair will follow the mouse

Usage can change with options, such as crosshair size, vertical only, horizontal
only, Fixed locations, colours, etc. 

"Options are:",
"-h or -help                       : display this helpful message.",
"-fg <color>                       : foreground color.",
"-bg <color>                       : background/outline color.",
"-nobg                             : no-background.",
"-rv                               : invert colours.",
"-offset <geometry>                : set x and y offset ex: +2-12.",
"-position <geometry>              : set fixed x and y position. ex: 960x540.",
"-width                            : set the width of the cursor.",
"-height                           : set the height of the cursor.",
"-horizontal                       : horizontal Line only.",
"-vertical                         : vertical line only.",
"-time                             : time between updates in microseconds.",
"-display                          : name of display to draw window to.",
"-name                             : name of process.",
"-sync                             : puts you in synchronous mode.",

<Special Thanks>
CrosshairCursor is written by Brian Markley PENG RSE after a code review of oneko 
and the oneko-toggle applet for cinamon desktop.

Original oneko program written by
Masayuki Koba
Modified by
Tatsuya Kato (kato@ntts.co.jp)

oneko-toggle applet is written by kusch31

<Testing and bug reports>
I have only tested this on one computer. My home system running 
Linux Mint 22.3 
Cinamon 6.6.7

Please submit all issues to the Github page CrosshairCursor@Bmarkley.
