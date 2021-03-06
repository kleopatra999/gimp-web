Title: How It All Started...
Date: 2015-07-29T14:40:35-05:00
Modified: 2015-07-29T14:40:43-05:00
Author: Pat David
Summary: 


## July 1995 - Two questions

At the end of July 1995, Peter Mattis posted a message in several newsgroups related to X11 and Linux application development, asking two questions and giving hints about an interesting program...

<pre style='font-size: 0.75rem; white-space: pre-wrap; border: solid 1px #ccc; padding: 1rem;'>
<b>From:</b> Peter Mattis
<b>Subject:</b> Image Manipulation Program Features
<b>Date:</b> 1995-07-29
<b>Message-ID:</b> <<a href="http://groups.google.com/group/comp.os.linux.development.apps/msg/ffa0c060f527159b">petm-2907952329370001@charnley.hip.berkeley.edu</a>>
<b>Newsgroups:</b> comp.windows.x,comp.windows.x.apps,comp.os.linux.x,comp.os.linux.development.apps

Suppose someone decided to write a graphical image manipulation program
(akin to photoshop). Out of curiousity (and maybe something else), I have a
few (2) questions:

  What kind of features should it have? (tools, selections, filters, etc.)
  What file formats should it support? (jpeg, gif, tiff, etc.)

Thanks in advance,
 Peter Mattis
</pre>

## July 1995 - A program using plug-ins?

Two weeks before, he was mentioning some program using plug-ins...

<pre style='font-size: 0.75rem; white-space: pre-wrap; border: solid 1px #ccc; padding: 1rem;'>
<b>From:</b> Peter Mattis
<b>Subject:</b> Re: Best way to write plug-ins?
<b>Date:</b> 1995-07-16
<b>Message-ID:</b> <<a href="http://groups.google.com/group/comp.os.linux.development.apps/msg/a385210efec43df3">3ua2hd$bbv@agate.berkeley.edu</a>>
<b>Newsgroups:</b> comp.os.linux.development.apps

In article <3u7amh$...@felix.cc.gatech.edu>,
Jeff Garzik <jgar...@cc.gatech.edu> wrote:
>I am writing an application for a my company, and I am interested in
>making it very easy to hook into internal program data (like a
>PhotoShop Plug-In, if you know what one of those is).  What would be
>the best way to do this?
>
>I can only think of two ways to do it right offhand, but I would like
>to avoid the second (call me a purist):
>
>* Allocate shared memory to a child process, which is either an
>  a.out or ELF binary.
>* Write the data out to a temporary file, or pipe, which the child
>  executable then reads.
>
>Is there a better way?

Well, I'm currently writing an application that uses plug-in modules. The
technique I use is to use pipes to handle communication and to use shared
memory to pass large data structures back and forth. (Well, I guess they
aren't really "passed" when using shared memory, now are they. :)

It is, however, not very easy to hook into internal program data. I set up
a fairly simple message passing system to handle requests for data. It works
fine for my purposes, but it wouldn't easily expand to allow access to 
arbitrary data structures in the main application.

Mail me if you want more specifics.

Peter Mattis
</pre>

## November 1995 - An Announcement

And then in November comes the first announcement of a beta release of the General Image Manipulation Program, "The GIMP" (later renamed to just "GIMP").

<pre style='font-size: 0.75rem; white-space: pre-wrap; border: solid 1px #ccc; padding: 1rem;'>
<b>From:</b> Peter Mattis
<b>Subject:</b> ANNOUNCE: The GIMP
<b>Date:</b> 1995-11-21
<b>Message-ID:</b> <<a href="http://groups.google.com/group/comp.os.linux.development.apps/msg/b5a9a98ef1e9fd4d">48s543$r7b@agate.berkeley.edu</a>>
<b>Newsgroups:</b> comp.os.linux.development.apps,comp.os.linux.misc,comp.windows.x.apps

The GIMP: the General Image Manipulation Program
------------------------------------------------

The GIMP is designed to provide an intuitive graphical interface to a
variety of image editing operations. Here is a list of the GIMP's 
major features:

 Image viewing
 -------------

   *  Supports 8, 15, 16 and 24 bit color.
   *  Ordered and Floyd-Steinberg dithering for 8 bit displays.
   *  View images as rgb color, grayscale or indexed color.
   *  Simultaneously edit multiple images.
   *  Zoom and pan in real-time.
   *  GIF, JPEG, PNG, TIFF and XPM support.

 Image editing
 -------------

   *  Selection tools including rectangle, ellipse, free, fuzzy, bezier 
      and intelligent.
   *  Transformation tools including rotate, scale, shear and flip.
   *  Painting tools including bucket, brush, airbrush, clone, convolve,
      blend and text.
   *  Effects filters (such as blur, edge detect).
   *  Channel & color operations (such as add, composite, decompose).
   *  Plug-ins which allow for the easy addition of new file formats and
      new effect filters.
   *  Multiple undo/redo.

Requirements
------------

 *  The operating system must support shared memory. 
 *  X11 R5 or R6\. (Actually, it may work on R4, but we have not had a
    chance to test it).
 *  The X-server must support the X shared memory extension. (The
    X-server does not actually need to support shared memory so this is
    only a temporary situation until we integrate the configure
    information with the source code).
 *  Motif 1.2 or above.

The GIMP has been tested (and developed) on the following operating
systems: Linux 1.2.13, Solaris 2.4, HPUX 9.05, SGI IRIX.

Currently, the biggest restriction to running the GIMP is the Motif
requirement. We will release a statically linked binary for several
systems soon (including Linux). 

URLs
----

http://www.csua.berkeley.edu/~gimp
ftp://ftp.csua.berkeley.edu/pub/gimp
mailto:gimp@soda.csua.berkeley.edu

Brought to you by
-----------------

  Spencer Kimball (spencer@soda.csua.berkeley.edu)
  Peter Mattis (petm@soda.csua.berkeley.edu)

NOTE
----

This software is currently a beta release. This means that we haven't
implemented all of the features we think are required for a full,
unqualified release. There are undoubtedly bugs we haven't found yet
just waiting to surface given the right conditions. If you run across
one of these, please send mail to gimp@soda.csua.berkeley.edu with
precise details on how it can be reliably reproduced.
</pre>

## February 1996 - GIMP 0.54

GIMP 0.54, the (in)famous Motif release, is announced in February 1996.

<pre style='font-size: 0.75rem; white-space: pre-wrap; border: solid 1px #ccc; padding: 1rem;'>
<b>From:</b> Peter Mattis
<b>Subject:</b> The GIMP v0.54 -- General Image Manipulation Program
<b>Date:</b> 1996-02-15
<b>Message-ID:</b> <<a href="http://groups.google.com/group/comp.os.linux.announce/msg/e1c97862ec4e89b1">cola-liw-824385260-28937-1@oravannahka.helsinki.fi</a>>
<b>Followup-To:</b> comp.os.linux.development.apps
<b>Newsgroups:</b> comp.os.linux.announce

A new version of the GIMP has been released. 0.54 features some
improvements over earlier versions and many bug fixes. (I tried my
hand at using Purify and found out what an extremely cool tool it
is). Also available are precompiled binaries for HP's, Suns (both
Sunos 4.1.x and Solaris), SGI's, and Linux a.out. I'm attaching the
README file to the end of this message which contains the url's for
getting the source and binaries.

This is a partial list of changes from earlier versions:

  * Fixed lots of other shit...added targa (tga) and pnm support...
  * Fixed a bit of stupid programming that caused some memory in
    autodialogs to never be freed.
  * Windows tend to retain their scale when using plug-ins which
    create new images now. (Such as "duplicate").
  * Used purify and found some stupid memory bugs. These include
    creating several arrays 1 byte too small and using unitialized memory
    in one instance.
  * Fixed a bug in bezier selections when an anchor point was outside
    of the image.
  * Implemented a dirty bit for images. Modified images will prompt to
    be saved before being closed.
  * Made a slight modification to the way the file overwrite dialog works.
 

Future plans
------------
 
During Christmas break we encountered Photoshop 3.0 and discovered the
"joy of layers". This functionality was deemed absolutely necessary
and will part of the next release of the GIMP. This will involve major
changes to many parts of the GIMP and is not expected to be ready for
several months. The other major item being changed is a reworking of
the interface (and perhaps the dropping of Motif!). Please do not bug
us about when these changes will be ready. It only distracts us and
slows us down. (Suffice it to say, we think the changes will be worth
the wait).

The GIMP: the General Image Manipulation Program
------------------------------------------------

The GIMP is designed to provide an intuitive graphical interface to a
variety of image editing operations. Here is a list of the GIMP's 
major features:

 Image viewing
 -------------

   *  Supports 8, 15, 16 and 24 bit color.
   *  Ordered and Floyd-Steinberg dithering for 8 bit displays.
   *  View images as rgb color, grayscale or indexed color.
   *  Simultaneously edit multiple images.
   *  Zoom and pan in real-time.
   *  GIF, JPEG, PNG, TIFF and XPM support.

 Image editing
 -------------

   *  Selection tools including rectangle, ellipse, free, fuzzy, bezier 
      and intelligent.
   *  Transformation tools including rotate, scale, shear and flip.
   *  Painting tools including bucket, brush, airbrush, clone, convolve,
      blend and text.
   *  Effects filters (such as blur, edge detect).
   *  Channel & color operations (such as add, composite, decompose).
   *  Plug-ins which allow for the easy addition of new file formats and
      new effect filters.
   *  Multiple undo/redo.

Requirements
------------

 *  The operating system must support shared memory. 
 *  X11 R5 or R6\. (Actually, it may work on R4, but we have not had a
    chance to test it).
 *  The X-server must support the X shared memory extension. (The
    X-server does not actually need to support shared memory so this is
    only a temporary situation until we integrate the configure
    information with the source code).
 *  Motif 1.2 or above.

The GIMP has been tested (and developed) on the following operating
systems: Linux 1.2.13, Solaris 2.4, HPUX 9.05, SGI IRIX.

Currently, the biggest restriction to running the GIMP is the Motif
requirement. We will release a statically linked binary for several
systems soon (including Linux). 

URLs
----

http://www.xcf.berkeley.edu/~gimp
ftp://ftp.xcf.berkeley.edu/pub/gimp
mailto:gimp@xcf.berkeley.edu

Brought to you by
-----------------

  Spencer Kimball (spencer@xcf.berkeley.edu)
  Peter Mattis (petm@xcf.berkeley.edu)

NOTE
----

This software is currently a beta release. This means that we haven't
implemented all of the features we think are required for a full,
unqualified release. There are undoubtedly bugs we haven't found yet
just waiting to surface given the right conditions. If you run across
one of these, please send mail to gimp@xcf.berkeley.edu with
precise details on how it can be reproduced.

</pre>

For historical interest, the Internet Archive has a copy of the link in Peter's email above:  
[http://www.xcf.berkeley.edu/~gimp](https://web.archive.org/web/19970711112615/http://www.xcf.berkeley.edu/~gimp/)

The story continues in "[A Brief (and ancient) History of GIMP](ancient_history.html)".
