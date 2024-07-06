# 基础镜像
FROM mysql:8
# author
MAINTAINER zipper
ENV LANG=C.UTF-8
ENV LC_ALL=C.UTF-8
ENV TZ=Asia/Shanghai
# 复制conf文件到路径
COPY ./conf/my.cnf /etc/mysql/conf.d/my.cnf
RUN chmod -R 644 /etc/mysql/conf.d/my.cnf
# 执行sql脚本
ADD ./*.sql /docker-entrypoint-initdb.d/
RUN chmod -R 775 /docker-entrypoint-initdb.d
