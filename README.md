What?
=====

Combines ImageMagick's `convert` with `ffmpeg` to automate creating time lapse h264 videos from a sequential series of jpegs.

How to use
==========

Sequential Files
----------------

Perhaps your files are already numbered nicely and you know what number you want to start at. You can use `--input-pattern` and `-n` together to create a video that runs until it runs out of sequential files.

Here's an example. The first arg is the pattern for file inputs, the second is the first file number to start at, and the third is the output video filename.

    ./lapse --input-pattern ~/Photos/New/IMG_%04d.JPG -n 8031 -o ~/Desktop/test.mkv

Files listed on standard input
------------------------------

Perhaps you have a multi layer directory tree but `sort` puts the filenames in the right order. You can use --stdin to decide the input images.

    find ~/mytimelapseframes -type f|sort|./lapse --stdin -o test.mkv

Options
=======

Use `lapse -h` to see additional options and their details. `--max-geometry` will preserve aspect ratio while fitting within a specified bounding box size (it will not be letterboxed).
