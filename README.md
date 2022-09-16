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

### Bill of Materials

* 74HCT138N (PDIP16)
* 74HCT04N (PDIP14)
* 2 x 0.1uF ceramic capacitor (axial, 5mm lead spacing)
* 10K linear potentiometer
* 39-pin single right-angle 0.1" header
* 16-pin double straight 0.1" header
* 16-pin single straight 0.1" header
* 16-pin DIP socket (optional)
* 14-pin DIP socket (optional)

## The Code

The example program `LCD.ZSM` is designed to work on CP/M, and can be built
using [ZSM][2]. Note that the I/O port addresses are hard-coded, and will need
to be changed to reflect your jumper setting.

[1]: https://bread80.com/2020/07/01/connecting-an-lcd-to-a-z80-with-two-glue-chips/
[2]: https://github.com/MiguelVis/zsm
