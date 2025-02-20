..
  SPDX-License-Identifier: BSD-3-Clause
  Copyright Contributors to the OpenEXR Project.

Display Window
##############

A series of OpenEXR files that can be used to test if a program that
displays images on the screen properly places, crops and pads the
images.  All files contain the same set of 400 by 300 pixels, but the
data window, display window, and pixel aspect ratio differ between
files.

.. list-table::
   :align: left
           
   * - ``t01.exr``

     - The display window and the data window are the same.  All pixels
       in the data window should be visible in the display window.

   * - ``t02.exr``, ``t03.exr``, ``t04.exr``, ``t05.exr``, ``t06.exr``, ``t07.exr``, ``t08.exr``

     - The display window and the data window overlap, but they are
       not the same.  Portions of the data window that are outside the
       display window should not be displayed.  Portions of the
       display window that are outside the data window should be
       filled with a suitable background color.

   * -  ``t09.exr``, ``t10.exr``, ``t11.exr``, ``t12.exr``

     - The display window and the data window do not overlap.  The
       entire display window should be filled with the background
       color.

   * - ``t13.exr``

     - The display window and the data window have only one pixel in
       common.  The data window's lower right pixel should be visible
       in the upper left corner of the display window.

   * - ``t14.exr``

     - The display window and the data window have only one pixel in
       common.  The data window's upper left pixel should be visible in
       the lower right corner of the display window.

   * - ``t15.exr``

     - The display window and the data window are the same as in
       ``t07.exr``, but the pixels have an aspect ratio (width divided by
       height) of 1.5.  On a screen with square pixels, both the
       display window and the data window should be stretched
       horizontally.

   * - ``t16.exr``

     - The display window and the data window are the same as in
       ``t07.exr``, but the pixels have an aspect ratio of 0.667.  On a
       screen with square pixels, both the display window and the
       data window should be stretched vertically.

