# JPEGT Encoder
A JPEGT encoder and viewer.

From http://fileformats.archiveteam.org/wiki/JPEGT:

**JPEGT** (**JPEG** **T**ransparent or **JPEG** with **T**ransparency) is a image format created by myself. It's the successor of Hemera Photo-Object.

It's just JPEG with transparency, a feature that didn't come out until earlier with JNG and Hemera Photo-Object.

Likewise, it's being used for clip art, logos, photos, you name it.

## Identification

The file starts with `JPGT%%` and then `0x31 0x41 0x59 0x26 0x53 0x58` which it's the first 12 BCD encoded digits of pi.

Then the JPEG picture comes in, and the PNG mask comes in. The idea was also used by Hemera Photo-Object, but the signature is not the same, but how it works it's the same.

## Disclaimer
This piece of software is vibe-coded using Claude 3.5 Sonnet

on Websim. When I didn't have a account, I used Ștefan's account for this.
