### 项目简介
1. 由于B站限制国外直播，所以我们要自建一台在国内的推流转发服务器，假装在国内。
建议选择阿里云上海的ECS，比腾讯云稳定很多。OBS可以配置3000kbps video + 129kbps audio, 1080p 30fps不是事

2. 同时由于Boston直接推到国内服务器掉帧很严重，所以我们还需要一台在香港的中转推流服务器。

### 关于配置文件的解释说明
服务器的配置安装过程在NUCSSA IT部门的wiki里搜索**Streaming Server Build**,
按步骤操作即可，这里只分享最终推流所需的config文件，存放位置wiki文章里有说明。
#### hk/nginx.conf
这是境外中转推流服务器conf，建议购买Google Cloud香港的VM.
记得防火墙开放端口1935

#### china/nginx.conf
这是国内最终推流到B站的中站推流服务器conf, 建议购买阿里云上海的ECS.
记得防火墙开放端口1935
