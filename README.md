# TG-270 Test Pattern Generator

The TG-270 Test Pattern Generator (TPG270) is a command line utility for
creating some of the test patterns described in the AAPM TG-270: Display
Quality Assurance report.

TPG270 can create the following test patterns:

* TG270-sQC
* TG270-pQC
* TG270-ULN
* TG270-TR

Additional test patterns may be added in the future.

## Command Syntax

Test patterns are generated using commands of the form `php tpg270
tpg:<test-pattern>` where `<test-pattern>` is one of the following:

* sqc
* pqc
* uln
* tr

### TG270-sQC

### TG270-pQC

### TG270-ULN  Test Pattern

The TG-270 ULN test pattern is a series of patterns for evaluating the
uniformity and luminance response of the monitor.

The ULN test patterns consist of images of varying gray levels, with
each individual image being a single uniform gray level.  Following
the TG-270 naming convention, The ULN patterns are named TG270-ULNx-y,
where x is the bit depth of the pattern (8 or 10 bits) and y is the
gray level of the image.

Use the command `php tpg270 tpg:uln` to generate the test patterns.

The command will ask for the size of the test pattern images to be
created, the bit depth of the images, the number of patterns to
generate, and the gray levels for the patterns.

#### Image size

The image size is specified as the number of pixels in the horizontal
and vertical direction, or by selecting from the preset options
provided.

#### Bit depth

Bit depth is specified as either 8 bits (256 gray levels) or 10 bites
(1024 gray levels).

#### Number of images

The number of ULN test pattern images to generate.  Each test pattern
image will be a uniform gray level with a different gray value.  The
maximum number of images that can be generated is the number of
available gray levels for the bit depth selected.

#### Gray levels

The gray levels for each ULN test pattern can be specified.  If only
one test pattern is being generated, the gray level must be provided.
If no gray levels are provided, the gray levels will be evenly spaced
depending on the number of images to be generated.

### TG270-TR

## License

TG-270 Test Pattern Generator is an open-source software licensed
under the GPL-3 (or later) license.
