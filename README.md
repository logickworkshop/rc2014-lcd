# RC2014 16x2 LCD Display Module

## The Module

The schematic for this module is based on an excellent blog post about
[connecting an LCD to a Z80 with two glue chips][1] by Mike Sutton (or more
accurately, on my own attempt to do the same thing, reaching nearly the same
design, then finding Mike's blog post and adopting his design wholesale). One
of eight I/O ports can be selected using a jumper, and the command and
character modes use two adjacent addresses.

The PCB provides a 16-pin header compatible with standard 16x2 LCD modules,
and should fit many of them within the footprint of the board if the headers
are soldered at the top of the module.

Note that at the nominal 7.3728Mhz clock speed of the RC2014, the enable
signal will only be held for about 68ns. Check the timing diagram in your LCD
display module's datasheet to ensure compatibility.

## The Code

The example program `LCD.ZSM` is designed to work on CP/M, and can be built
using [ZSM][2].

[1]: https://bread80.com/2020/07/01/connecting-an-lcd-to-a-z80-with-two-glue-chips/
[2]: https://github.com/MiguelVis/zsm
