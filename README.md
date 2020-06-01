# Ubuntu

[![Docker Automated Status](https://img.shields.io/docker/cloud/automated/docker4cn/ubuntu.svg)](https://hub.docker.com/r/docker4cn/ubuntu/builds/)
[![Docker Build Status](https://img.shields.io/docker/cloud/build/docker4cn/ubuntu.svg)](https://hub.docker.com/r/docker4cn/ubuntu/builds/)
[![Docker Stars](https://img.shields.io/docker/stars/docker4cn/ubuntu.svg)](https://hub.docker.com/r/docker4cn/ubuntu/)
[![Docker Pulls](https://img.shields.io/docker/pulls/docker4cn/ubuntu.svg)](https://hub.docker.com/r/docker4cn/ubuntu/)
[![License](https://img.shields.io/github/license/docker4cn/ubuntu.svg)](https://github.com/docker4cn/ubuntu/blob/master/LICENSE)

这是为中国定制的Ubuntu镜像，上游是Docker官方的[ubuntu](https://hub.docker.com/_/ubuntu)镜像。
它是[docker4cn]项目的一部分。

[docker4cn]:https://docker-4.cn/

## 定制

Ubuntu镜像替换为以下源：

| 机构     | 源       | 域名                           | 信息链接                                           |
| ----     | --       | ----                           | --------                                           |
| 阿里巴巴 | `aliyun` | `mirrors.aliyun.com`           | <https://developer.aliyun.com/mirror/>             |
| 中科大   | `ustc`   | `mirrors.ustc.edu.cn`          | <https://mirrors.ustc.edu.cn/repogen/>             |
| 清华     | `tuna`   | `mirrors.tuna.tsinghua.edu.cn` | <https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/> |
| 华为     | `huawei` | `mirrors.huaweicloud.com`      | <https://mirrors.huaweicloud.com/>                 |
| 网易     | `163`    | `mirrors.163.com`              | <https://mirrors.163.com/>                         |

除了换源，还做了以下改进：

- 预装`ca-certificates`证书包，使用`https`的方式下载软件包。
- 设置时区为中国的`+8`区（`Asia/Shanghai`）。
- 增加PyPI、NPM、Gradle的镜像或代理。

## 使用示例

```sh
docker pull docker4cn/ubuntu:20.04-aliyun
```

默认`lastest`使用`aliyun`，因为它是Ubuntu官方镜像中排名第一的。
目前的`latest`是`20.04-aliyun`。
但它不一定是最合适的源，推荐通过tag选择特定镜像。
通过`ping <域名>`，找到最近的源，往往会有更好的使用效果。

维护中的tag：

- 20.04
    - [latest], [20.04-aliyun]
    - [20.04-huawei]
    - [20.04-ustc]
    - [20.04-tuna]
    - [20.04-163]
- 18.04
    - [18.04-aliyun]
    - [18.04-huawei]
    - [18.04-ustc]
    - [18.04-tuna]
    - [18.04-163]
- 16.04
    - [16.04-aliyun]
    - [16.04-huawei]
    - [16.04-ustc]
    - [16.04-tuna]
    - [16.04-163]

[latest]:https://github.com/docker4cn/ubuntu/blob/master/20.04/aliyun/Dockerfile
[20.04-aliyun]:https://github.com/docker4cn/ubuntu/blob/master/20.04/aliyun/Dockerfile
[20.04-huawei]:https://github.com/docker4cn/ubuntu/blob/master/20.04/huawei/Dockerfile
[20.04-ustc]:https://github.com/docker4cn/ubuntu/blob/master/20.04/ustc/Dockerfile
[20.04-tuna]:https://github.com/docker4cn/ubuntu/blob/master/20.04/tuna/Dockerfile
[20.04-163]:https://github.com/docker4cn/ubuntu/blob/master/20.04/163/Dockerfile
[18.04-aliyun]:https://github.com/docker4cn/ubuntu/blob/master/18.04/aliyun/Dockerfile
[18.04-huawei]:https://github.com/docker4cn/ubuntu/blob/master/18.04/huawei/Dockerfile
[18.04-ustc]:https://github.com/docker4cn/ubuntu/blob/master/18.04/ustc/Dockerfile
[18.04-tuna]:https://github.com/docker4cn/ubuntu/blob/master/18.04/tuna/Dockerfile
[18.04-163]:https://github.com/docker4cn/ubuntu/blob/master/18.04/163/Dockerfile
[16.04-aliyun]:https://github.com/docker4cn/ubuntu/blob/master/16.04/aliyun/Dockerfile
[16.04-huawei]:https://github.com/docker4cn/ubuntu/blob/master/16.04/huawei/Dockerfile
[16.04-ustc]:https://github.com/docker4cn/ubuntu/blob/master/16.04/ustc/Dockerfile
[16.04-tuna]:https://github.com/docker4cn/ubuntu/blob/master/16.04/tuna/Dockerfile
[16.04-163]:https://github.com/docker4cn/ubuntu/blob/master/16.04/163/Dockerfile

## 其它

更多[docker4cn]定制Docker基础镜像，请访问：<https://docker-4.cn/>

更多Ubuntu镜像，参考：[Official Archive Mirrors for Ubuntu](https://launchpad.net/ubuntu/+archivemirrors)。

如果希望更新、改进，请提[issues]或PR。

[issues]:https://github.com/docker4cn/ubuntu/issues/new
