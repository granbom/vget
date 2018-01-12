# vget

Wrapper around svtplay-dl and ffmpeg

## Getting Started

Just clone this repo to get the vget bash script file.

### Prerequisites

vget are using

* [svtplay-dl](https://github.com/spaam/svtplay-dl)
* [ffmpeg](https://github.com/FFmpeg/FFmpeg)

Hence, they both need to be installed for vget to work.

### ffmpeg from source

If you are using Ubuntu you can install ffmpeg's prerequisites like this

```bash
sudo apt install autoconf automake build-essential cmake git libass-dev libfreetype6-dev libsdl2-dev libtheora-dev libtool libva-dev libvdpau-dev libvorbis-dev libxcb1-dev libxcb-shm0-dev libxcb-xfixes0-dev mercurial pkg-config texinfo wget zlib1g-dev
sudo apt install yasm libx264-dev libx265-dev libvpx-dev libfdk-aac-dev libmp3lame-dev libopus-dev librtmp-dev libxvidcore-dev ocl-icd-opencl-dev
```

Then clone from either github's mirror or original repository. Below is the original repo. Github one is: `https://github.com/FFmpeg/FFmpeg.git`

```bash
git clone https://git.ffmpeg.org/ffmpeg.git
./configure --enable-pthreads --enable-version3 --enable-avresample --enable-gpl --enable-libass --enable-libfdk-aac --enable-libfreetype --enable-libmp3lame --enable-libopus --enable-librtmp --enable-libvorbis --enable-libvpx --enable-libx264 --enable-libx265 --enable-libxvid --enable-opencl --enable-openssl --enable-nonfree
make
sudo make install
```

### svtplay-dl from source

```bash
git clone https://github.com/spaam/svtplay-dl.git
make
sudo make install
```

### Installing

```bash
git clone https://github.com/granbom/vget.git
```

Copy vget to a directory in your $PATH. If you don't have a `bin` directory in you home folder before it will not be in your $PATH. Create your `~/bin/` and restart.

```bash
/usr/local/bin/ or
~/bin/
```

Don't forget to make it executable

```bash
chmod a+x vget
```

### Usage

Default vget will try to download subtitles and then remux the downloaded video with subtitles into a mkv file. It will set the language metadata for the audio and subtitles to Swedish. After this the mp4 or ts and srt file will be removed.
You can change default behaviour in the created settings file ~/.vget.conf

```bash
vget url-to-video
# to see some options
vget -h
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
