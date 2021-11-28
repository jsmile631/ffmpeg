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

## Combining Audio + Image
Command :
```code
ffmpeg -loop 1 -i image.jpg -i audio.mp3 -c:v libx264 -tune stillimage -c:a aac -b:a 192k -pix_fmt yuv420p -shortest out.mp4
```
Description :
- image.jpg : `your image that will be combined with the audio`
- audio.mp3 : `your audio that will be combined with  the image`
- out.mp4 : `video result`
