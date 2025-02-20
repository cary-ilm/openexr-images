..
  SPDX-License-Identifier: BSD-3-Clause
  Copyright Contributors to the OpenEXR Project.

Unusual Pixel Images
####################

A few OpenEXR files with unusual numbers in their pixels.  The files
can be used to test how application programs behave when they
encounter pixels with very small, very large or non-finite pixel
values.

.. list-table::
   :align: left

   * - ``WideColorGamut.exr``

     - Some pixels in this RGB image have extremely saturated colors,
       outside the gamut that can be displayed on a video monitor
       whose primaries match Rec. ITU-R BT.709.  All RGB triples in
       the image correspond to CIE xyY triples with xy chromaticities
       that represent real colors.  (In a chromaticity diagram, the
       pixels are all inside the spectral locus.)  However, for pixels
       whose chromaticities are outside the triangle defined by the
       chromaticities of the Rec. 709 primaries, at least one of the
       RGB values is negative.

   * - ``AllHalfValues.exr``

     - The pixels in this RGB HALF image contain all 65,536 possible
       16-bit floating-point numbers, including positive and negative
       numbers, normalized and denormalized numbers, zero, NaNs,
       positive infinity and negative infinity.

   * - ``WideFloatRange.exr``

     - This image contains only a single G channel of type FLOAT.  The
       values in the pixels span almost the entire range of possible
       32-bit floating-point numbers (roughly -1e38 to +1e38).

   * - ``BrightRings.exr``

     - This RGB image contains a number of rather bright rings, with
       pixel values over 1000, on a gray background.  The image is
       useful for testing how filtering and resampling algorithms
       react to high- dynamic-range data.  (Some filters, for example,
       convolution kernels with negative lobes, tend to produce
       objectionable artifacts near high-contrast edges.)  Note that
       the rings in the image are smooth, although on most displays
       clamping of the pixel values introduces aliasing artifacts.  To
       see that the rings really are smooth, view the image with
       and exposure of -10.

   * - ``BrightRingsNanInf.exr``

     - This image is the same as ``BrightRings.exr``, except for a few
       pixels near the center, which contain NaNs and infinities.

   * - ``SquaresSwirls.exr``

     - This image contains colored squares and swirling patterns
       against a flat gray background.  Applying lossy compression
       algorithms to this image tends to highlight compression
       artifacts.

