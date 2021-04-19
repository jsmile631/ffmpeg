# FFMPEG COMMAND

## Image to Video
Command : 
```code
ffmpeg -y -f lavfi -i anullsrc  -loop 1 -f image2 -i image.jpg  -r 30 -t 10 -pix_fmt yuvj420p -map 0:a -map 1:v video.mp4
```
Description :
- image.jpg : `your image that will be converted`
- video.mp4 : `your video result`


## Edit Pitch
Command :
```code
command will be here
```
