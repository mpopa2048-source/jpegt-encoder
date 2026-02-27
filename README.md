# JPEGT Encoder
A JPEGT encoder and viewer.

From http://fileformats.archiveteam.org/wiki/JPEGT:

**JPEGT** and **JPEGT+** (**JPEG** **T**ransparent or **JPEG** with **T**ransparency) are image formats created by myself. It's the successor of Hemera Photo-Object.

It's just JPEG with transparency, a feature that didn't come out until earlier with JNG and Hemera Photo-Object.

Likewise, it's being used for clip art, logos, photos, you name it.

## Identification
### JPEGT
The file starts with `JPGT%%` and then `0x31 0x41 0x59 0x26 0x53 0x58` which it's the first 12 BCD encoded digits of pi.

Then the JPEG picture comes in, and the PNG mask comes in. A variation of this is mostly the same, but the PNG mask is deflated with Pako, in this case it starts with `CMPR`.

That variation is not longer used, and the current version is using the correct formats.

The idea was also used by Hemera Photo-Object, but the signature is not the same, but how it works it's the same.

### JPEGT+
The file starts with `JPGT%%` and then `0x58 0x53 0x26 0x59 0x41 0x31` which it's the first 12 BCD encoded digits of pi, but each byte is in reversed order.

Then the JPEG picture comes in, and the JPEG mask comes in.

## Disclaimer
This piece of software was vibe-coded using Claude 3.5 Sonnet

on Websim. When I didn't have a account, I used Ștefan's account for this.

Now is further vibe-coded using Gemini 3 Flash to remove Pako.
