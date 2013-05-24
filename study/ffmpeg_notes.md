#FFmpeg
###什么是FFmpeg
开源的音视频编解码库， 2004，由Fabrice Bellard 发起， 由Michael Niedermayer维护。 

很多开源项目使用了FFmpeg， e.g. ffmpeg2theora, vlc, mplayer, handbrake, blender, google chrome, etc.

###FFmpeg 包含的组件
**Programs**

ffmpeg - 支持各种多媒体文件格式的转码工具*(command line tool)*

ffserver - 支持直播的多媒体流服务器

ffplay - 基于 *SDL* 和 *FFmpeg库* 的多媒体播放器

ffprobe - 简单的多媒体流分析工具

**Libraries**

libavutil - 包含了很多用于简化编程的function， 包括：随机数生成器， 数据结构， 数学例程， 核心多媒体工具集，etc.

libavcodec - audio/video 编解码库

libavformat - muxsers and demuxsers for multimedia container formats

libavdevice - 包含input/output devices for grabbing from

libavfilter - media filters

libswscale - 图片处理， 高度优化， 图片缩放， 色彩空间， 像素格式转换。

what i need to learn is： *libavcodec* and *libavformat*


###音视频基础
**比特率(bit rate)**

一秒钟音频数据编码所需的位数(**bits**)

**采样率(sampling frequency)**
 
how often or how much the sound is *described*

比特率 和 采样率 的关系： 非压缩音频格式， 比特率和采样率成正比

**计算**

bit rate = (sampling rate) x (bit depth)  x (number of channels)

file size(**bytes**) = (sampling rate) x (bit depth) x (total channels) x (seconds)/8

**帧率(frame rate)**

帧率指的是，一秒钟播放多少张连续图片。 每张图片被称为*帧(frame)*

PAL (europe and some parts of Asia) uses 25fps

NTSC (US and Japan) uses 29.97fps

 