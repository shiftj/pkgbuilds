#pngnq-s9
A modified pngnq: convert png images to 256 colours.
[Source](http://sourceforge.net/projects/pngnqs9/)

#Description
pngnq-s9 is a modified version of pngnq, the neural network colour quantizer for png images.

Like pngnq, pngnq-s9 takes a full 32 bit RGBA png image, selects a palette of up to 256 colours, and 
then redraws the image in 8 bit indexed mode. The resulting image can be up to 70% smaller than the
original.

pngnq-s9 adds several new options to pngnq including the ability to augment a user-supplied palette, 
the ability to quantize in the YUV colour space, and the ability to give more or less weight to specific 
colour components when quantizing. The program also includes a few bug fixes relative to the most 
recent version of pngnq.

Currently, pngnq-s9 is in alpha release. The .tar.gz file on this page is known to compile on Unix type 
systems, including Cygwin. The only external dependencies are libpng and zlib.

For Windows users, we now have a binary release, pngnq-s9-2.0.1-win32.zip, that should run as is on 
most modern Windows machines. (If you try it, please let us know!)

#Features
- Quantizes 32 bit RGBA png images down to 256 colours or fewer, just like pngnq.
- selectable internal colour space (either RGBA or YUVA)
- use different sensitivities for each colour component
- supply your own fixed palette, and optionally select additional colours as well. Very useful if you 
need particular colours to remain stable.
- better colour selection through longer learning and improved rejection of duplicate colours
- various options to alter colour selection policy (see -x, -u)
- options to stop alpha values of 0 and 255 being 'smudged' to nearby values
- selectable level of Floyd-Steinberg style dithering
- suppresses writing of png gAMA chunk by default
- suppresses writing of png background colour chunk
- bug fix for occasional remapping to the wrong colour (relative to pngnq 1.1)
- bug fix for a relatively harmless flaw in implementation of Floyd-Steinberg dithering (relative to pngnq 1.1)

