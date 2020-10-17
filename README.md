# Scripts
My simple scipts

### Lossy compress video (recorded by recCall)
 - by CPU
```bash
ffmpeg -i input.mkv -c:v libx264 -preset veryslow -crf 30 -c:a copy output.mkv
```
 - by GPU
```bash
ffmpeg -i input.mkv -c:a copy -c:v h264_nvenc -pix_fmt yuv420p -preset slow -rc constqp -qp 30 output.mkv
```

