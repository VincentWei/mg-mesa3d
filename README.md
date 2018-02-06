# Mesa3D with support for MiniGUI

This is a port of Mesa3D (https://www.mesa3d.org) for MiniGUI.

Naturally, we implement a MiniGUI driver for Mesa EGL implementation.

> The current version of EGL in Mesa implements EGL 1.4. More information 
> about EGL can be found at https://www.khronos.org/egl/.
>
> The Mesa's implementation of EGL uses a driver architecture. 
> The main library (libEGL) is window system neutral. It provides the EGL 
> API entry points and helper functions for use by the drivers. 
> Drivers are dynamically loaded by the main library and most of the EGL 
> API calls are directly dispatched to the drivers.

## Prerequisites

  * MiniGUI: v3.2.0 or later

  * System library dependencies:
    * libelf-dev
    * llvm-3.9-dev

## Building

Mesa3D uses GNU autoconf/automake scripts to configure and build the project.

Run

    $ ./configure --enable-gl --enable-gles2 --enable-egl  \
        --disable-glx \
        --with-platforms=minigui        # include 'x11' if you enable GLX.
    $ make; sudo make install

to configure, make, and install the headers and the libraries (libGL, 
libGLESv2, libEGL). 

Mesa3D also provides some configuration options to customize the features.
For more information, please run

    $ ./configure --help


## Copying

    Copyright © 2010~2018 Beijing FMSoft Technologies Co., Ltd.
    Copyright © 2013-2017 The Khronos Group Inc.
    Copyright © 2011-2014 Intel Corporation
    Copyright © 2011-2014 Emil Velikov <emil.l.velikov@gmail.com>
    Copyright © 2007-2010 Dan Nicholson
    Copyright © 2010-2014 Marek Olšák <maraeo@gmail.com>
    Copyright © 2010-2014 Christian König
    Copyright © 2012-2014 Tom Stellard <tstellar@gmail.com>
    Copyright © 2009-2012 Jakob Bornecrantz
    Copyright © 2009-2014 Jon TURNEY
    Copyright © 2011-2012 Benjamin Franzke
    Copyright © 2008-2014 David Airlie
    Copyright © 2009-2013 Brian Paul

    Permission is hereby granted, free of charge, to any person obtaining a
    copy of this software and associated documentation files (the "Software"),
    to deal in the Software without restriction, including without limitation
    the rights to use, copy, modify, merge, publish, distribute, sublicense,
    and/or sell copies of the Software, and to permit persons to whom the
    Software is furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included
    in all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS
    OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.  IN NO EVENT SHALL
    THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
