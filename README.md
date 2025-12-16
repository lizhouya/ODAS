# ODAS
ODAS代码架构思维导图
```mermaid
mindmap
  root((ODAS 源码<br/>深度映射))
    核心算法
      SSL 声源定位
        原理: SRP-PHAT / GCC
        代码文件
          📄 src/module/mod_ssl.c
          📄 src/signal/steer.c
      SST 声源追踪
        原理: Kalman / Particle Filter
        代码文件
          📄 src/module/mod_sst.c
          📄 src/signal/kalman.c
          📄 src/signal/particle.c
      SSS 声源分离
        原理: GSS / Beamforming
        代码文件
          📄 src/module/mod_sss.c
          📄 src/signal/demixing.c
    系统架构
      入口与配置
        📄 demo/odaslive/main.c
        📄 demo/odaslive/configs.c
      基础与几何
        📄 src/general/mic.c
        📄 src/general/dsptools.c
    数据流 IO
      输入 Source
        📄 src/source/src_alsa.c
        📄 src/source/src_file.c
      输出 Sink
        📄 src/sink/snk_tracks.c
        📄 src/sink/snk_pots.c
