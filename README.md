# FFMPEG COMMAND

## Change resolution from 4K to 1080
Command
```code
ffmpeg -i input4kvid.mp4 -vf scale=1920:1080 -c:a copy output1080vid.mp4
```

## Compressing to reduce file size
Command
```code
ffmpeg -i input.mp4 -vcodec libx265 -crf 28 output.mp4
```
- input.mov : `video file which will be compressed`
- output.mp4 : `video file which has ben compressed`

## Converting video format to another video format
Command
```code
ffmpeg -i input.mov -qscale 0 output.mp4
```
- input.mov : `video file which will be converted`
- output.mp4 : `video file which has ben converted`

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

## Trims video
Command :
```code
ffmpeg -ss 00:01:00 -to 00:02:00 -i input.mp4 -c copy output.mp4
```
