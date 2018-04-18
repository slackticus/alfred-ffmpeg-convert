# alfred-ffmpeg-convert
Alfred Workflow to Convert a video to MP4 with hinted streaming for web.  Reduces file size significantly without much video reduction.

####################
### Dependencies ###
####################

Alfred - 3.6.1+

ffmpeg (recomend installing with Homebrew: https://brew.sh/)


### Flags ###
These are the flags I started out with.  I don't know if I will rember to update the readme if I change them:
-codec:v libx264 -crf 21 -bf 2 -flags +cgop -pix_fmt yuv420p -codec:a aac -strict -2 -b:a 256k -r:a 48000 -movflags faststart

If you want to change them, you will need to do so in the bash script. 



### Directions ###
Open Alfred and type "encode", space, then the name of the file to convert.  I will put the updated version in the same place, but will add -encoded.mp4 to the name.

Example:
encode example.mov

Big movies will take a while to encode so it will let you know when it starts and when it finishes with big type on the screen and a sound.
