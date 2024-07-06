
FROM eclipse-temurin:11-jre
MAINTAINER zipper
ENV LANG=C.UTF-8
ENV LC_ALL=C.UTF-8

# 挂载目录
VOLUME /home/yudao
# 创建目录
RUN mkdir -p /home/yudao
# 指定路径
WORKDIR /home/yudao

## 设置 TZ 时区
ENV TZ=Asia/Shanghai
## 设置 JAVA_OPTS 环境变量，可通过 docker run -e "JAVA_OPTS=" 进行覆盖
ENV JAVA_OPTS="-Xms512m -Xmx512m -Djava.security.egd=file:/dev/./urandom"

## 应用参数
ENV ARGS=""

## 暴露后端项目的 48080 端口
EXPOSE 48080
CMD ["ls", "-a"]
# 启动认证服务
ENTRYPOINT java ${JAVA_OPTS} -jar yudao-server.jar $ARGS
## 启动后端项目
# CMD java ${JAVA_OPTS} -jar app.jar $ARGS
