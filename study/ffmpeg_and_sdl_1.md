#[ffmpeg and SDL](http://dranger.com/ffmpeg/tutorial01.html)
## 概述
视频文件包含一些基本组件， 首先，文件本身被称为**容器(*container*)**，容器的类型决定了文件中的信息的类型。如AVI 和 Quicktime。 然后， 有了一连串的**流(*streams*)**，音频流和视频流。 stream 中的数据元素被称为**帧（frames）**，不同的流有不同的编码格式，codec 定义了数据到底是怎么编码 和 解码的。** 包（packets）** 包含一个个数据块， 最后可以decode成可以被我们app操作的raw frames。当packet是音频数据的时候， 它可能包含多个frame。

从最基本的流程来看， 处理音视频是非常简单的。

**1:**  open video_stream frame video file*(or network*)

**2:**  READ packet FROM video_stream INTO frame

**3:**  IF frame NOT COMPLETE GOTO **2:**

**4:**  DO SOMETHING WITH frame

**5:**  GOTO **2:**
