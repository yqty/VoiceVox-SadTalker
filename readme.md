Voicevox-SadTalker
概要
当输入文本、话者ID和图像ID后，会生成一个与图像中人脸进行唇部同步的视频。
运行环境
Windows 11
WSL2 Ubuntu 20.04 LTS
Docker 版本 23.0.5，构建版本 bc4487a
示例
克隆存储库

$ git clone https://github.com/yqty/VoiceVox-SadTalker.git

使用 docker-compose 进行构建和启动

$ docker-compose build && docker-compose up

服务器启动后，执行以下示例命令

$ curl -X POST  -H "Content-Type: application/json"  -d '{"text":"这是一个测试。", "speaker_id":1, "image_id":1}' localhost:8080/create/video/


注意事项
videoServer/dockerfile 使用 nvidia/cuda:11.7.0-base-ubuntu22.04 作为基础环境进行搭建。由于执行环境可能不适用于某些计算机，请在出现问题时先检查一下。

参考
https://hub.docker.com/r/nvidia/cuda
注意需要大约10GB的内存。
