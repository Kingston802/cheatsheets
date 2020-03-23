# ffmpeg
[ffmpeg](https://www.ffmpeg.org) is a cli tool for all things video and audio. it's useful for changing filetypes, removing audio etc.

## changing filetypes
```bash
ffmpeg -i video.mp4 video.avi
ffmpeg -i video.flv video.mpeg
```
for a list of a supported formats
```bash
ffmpeg -formats
```
optional parameter to preserve quality of source file
```bash
ffmpeg -i input.webm -qscale 0 output.mp4
```
## remove audio/video 
```bash
ffmpeg -i input.mp4 -an output.mp4
ffmpeg -i input.mp4 -vn output.mp3
```
## merge/split audio/video files
```bash
ffmpeg -f concat -i join.txt -c copy output.mp4
```
where join.txt contains a list of files like 
```
file /home/myvideos/part1.mp4
file /home/myvideos/part2.mp4
file /home/myvideos/part3.mp4
file /home/myvideos/part4.mp4
```
## need more help?
```bash
man ffmpeg
```
