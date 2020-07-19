# Ufiformat - A format utility for USB floppy disk devices.

My clone of ufiformat repository. Currently only for backup purposes and possible future build patches as it was abandoned by the author.

## README - a formated version of the original README

This is a format utility for USB floppy disk devices.
    
Usage: ufiformat [OPTION]... [DEVICE]
Format a floppy disk in a USB floppy disk DEVICE.
    
 * -f, --format [SIZE]  <br> specify format capacity SIZE in KB <br> without -f option, the format of the current media will be used
 * -F, --force          <br> do not perform any safety checks
 * -i, --inquire        <br> show device information, instead of performing format <br> without DEVICE argument, list USB floppy disk devices
 * -v, --verbose        <br> show detailed output
 * -q, --quiet          <br> suppress minor output
 * -h, --help           <br> show this message
    
NOTE: ufiformat supports only the following format capacities.

 * 1440/1232/1200 (for 2hd disk)
 * 720/640        (for 2dd disk)
 
 The device should also support the capacities, otherwise ufiformat will show an error message.
    
 The above format capacities are predefined in the program, but each usb floppy device also has a limited set of formats (defined internally) that it can format media to. The allowed format capacities are obtained by querying the device, but this only returns the total format capacity and not CHS (cylinder, heads and sectors), hence a mapping is required in the program.
    
This program is based around the following document:
 *   "Universal Serial Bus Mass Storage Class - UFI Command Specification", Revision 1.0 December 14 1998, http://www.usb.org/developers/devclass_docs/usbmass-ufi10.pdf
  
---

## The original author

 * Kazuhiro Hayashi <https://github.com/tedigh>
