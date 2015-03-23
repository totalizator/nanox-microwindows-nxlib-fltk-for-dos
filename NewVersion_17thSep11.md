Several improvements are implemented in this version of 17th September:

  * modified keyboard driver for improved ALT-key support

  * added an Alt-comma key combination to switch temporarily to text mode and back refreshing the screen. This allows debugging with GDB.

  * wrote an event-driven mouse driver to improve performance

  * screen driver will redirect STDOUT to the NUL device when enabling SVGA mode. Text output to STDOUT did corrupt the SVGA display.

  * added the NANOSCR environment variable to set the screen resolution and color mode

  * added a default directory in the FLTK editor example

  * added missing image to libimages.a so the mdemo.c example will compile