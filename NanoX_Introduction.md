## Overview of the Nano-X, NXlib, Microwindows and FLTK for DOS development environment. ##

Nano-X as it is named today,  is an Open Source project that develops a  graphical windowing system for small and embedded devices.  Nano-X does not require any operating system or other graphics system support, as it writes directly to the display hardware.  Nano-X is designed to be portable, and can run in a wide variety of hardware and software environments. The library provides two programming APIs: one is XWindows compatible, the other is Win32 compatible. This site makes the DOS port of this library available, the primary site of this project is here: http://www.microwindows.org/

### Architecture ###

The Nano-X Window System is a layered design that allows different layers to be used or rewritten to suit the needs of the implementation.  At the lowest level, screen, mouse/touchpad and keyboard drivers provide access to the actual display and other user-input hardware. For DOS an SVGA driver has been written. At the mid level, a portable graphics engine is implemented, providing support for line draws, area fills, polygons, clipping and color models.

At the upper level, two API's are implemented providing access to the graphics applications programmer.  These APIs can provide desktop and/or window look and feel.  Currently, Nano-X supports the Microwindows and Nano-X APIs.  These APIs provide close compatibility with the Win32 and X Window systems, allowing programs to be ported from other systems.

### Licence ###

The project is licensed under the MPL.  Alternatively, the software can be licensed under the GPL, if desired.  This means that the standard Nano-X distribution can be used for commercial purposes, and supports the needs of developers working under non-disclosure or writing proprietary device drivers.  Modifications to source code supplied in the standard distribution must stay open source.  Or the entire project can be converted to GPL, with files added by a developer considered GPL only.

### Port to DOS ###

Nano-X has been ported to DOS using DJGPP. All development based on this library has been done using the DJGPP compiler.

### NXlib ###

NXlib is a wrapper library that provides closer compatibility to the Xlib API for Nano-X. Due to historical reasons, the functions in Nano-X were called differently than in XWindows although they provided almost the same functionality. Using NXlib many XWindows applications can be ported to DOS without major changes.

### Xt, Xaw, Motif ###

NXlib is compatible to just Xlib. If a program uses Xt, Xaw or Motif, you will not be able to port this to DOS. This image shows the relationship of these packages:

![http://nanox-microwindows-nxlib-fltk-for-dos.googlecode.com/files/Xlib-overview.png](http://nanox-microwindows-nxlib-fltk-for-dos.googlecode.com/files/Xlib-overview.png)

### FLTK ###

FLTK stands for Fast Light Tool Kit. It is a C++ GUI toolkit that provides modern GUI functionality with a smaller footprint than GTK+.
FLTK is designed to be small and modular enough to be statically linked which has do be done with DJGPP. FLTK also includes an excellent UI builder called FLUID. FLTK is provided with a GPL licence and allows for static linking.
NXlib provides enough XWindows compatibility that FLTK can be used on the base of the NXlib and Nano-X libraries.

### Applications ###

Based on the DOS port of the Nano-X library and FLTK the browser Dillo has been ported to DOS and is available from this site.

Further applications will be ported and made available here. A calculator application has been added recently.

### External links ###

More information about Nano-X can be found here:
http://www.microwindows.org/microwindows_architecture.html
This page does not yet cover NXlib and the FLTK port and uses the old name microwindows instead of Nano-X.