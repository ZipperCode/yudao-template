# 基础镜像
FROM redis:6-alpine
# author
MAINTAINER zipper
ENV LANG=C.UTF-8
ENV LC_ALL=C.UTF-8
# 挂载目录
VOLUME /home/yudao/redis
# 创建目录
RUN mkdir -p /home/yudao/redis
# 指定路径
WORKDIR /home/yudao/redis