What?
=====

Combines ImageMagick's `convert` with `ffmpeg` to automate creating time lapse h264 videos from a sequential series of jpegs.

How to use
==========

Here's an example. The first arg is the pattern for file inputs, the second is the first file number to start at, and the third is the output video filename.

    ./lapse ~/Photos/New/IMG_%04d.JPG 8031 ~/Desktop/test.mkv
