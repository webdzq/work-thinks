# ffmpeg

- FFmpeg 是一个强大的开源跨平台多媒体处理工具，集录制、转换、流化音视频于一体，其功能丰富，应用场景广泛.工作中涉及到视频剪辑、拼接和logo处理等。

## ffmpeg安装

- `brew install ffmpeg`
- `ffmpeg -version`

## 常用命令

- 将视频压缩到指定大小

```bash
ffmpeg  -i  Desktop/input.mp4  -fs 10MB  Desktop/output.mp4

-fs 10 : 表示文件大小最大值为10MB
```

- 设置视频的帧率为20fps

```bash
ffmpeg  -i  Desktop/input.mp4  -r 20  Desktop/output.mp4

-r 20：表示帧率设置为 20fps
```

- 设置视频的码率

```bash
ffmpeg  -i  Desktop/input.mp4  -b:v 1M  Desktop/output.mp4

-b:v :指定视频的码率

-b:a : 指定音频的码率

1M：码率的值 1M 表示 1Mb/s
```

- 设置视频的分辨率

```bash
ffmpeg  -i  Desktop/input.mp4  -s 1920x1080  Desktop/output.mp4

-s 1920x1080表示分辨率为1920x1080

```

- 可以结合上面的命令一起来使用

```bash
ffmpeg  -i  Desktop/input.mp4  -s 1920x1080  -b:v 1M  -r 20  Desktop/output.mp4
```

## 参考文献

- [https://github.com/FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg)
