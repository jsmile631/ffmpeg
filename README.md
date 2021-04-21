# FFMPEG COMMAND

## Converting Image to Video
Command : 
```code
ffmpeg -y -f lavfi -i anullsrc  -loop 1 -f image2 -i image.jpg  -r 30 -t 10 -pix_fmt yuvj420p -map 0:a -map 1:v video.mp4
```
Description :
- image.jpg : `your image that will be converted`
- video.mp4 : `your video result`

## Edit Video Length
Command :
```code
ffmpeg -i input.mp4 -ss 00:00:00 -t 00:00:10 -async 1 result.mp4
```
Description :
- input.mp4 : `your video that will be edited
- 00:00.00 : `select start time`
- 00.00.01 : `select end time`
- result.mp4 : `vidio in selected start-end time`

## Editing Pitch
Command :
```code
command will be here
```
