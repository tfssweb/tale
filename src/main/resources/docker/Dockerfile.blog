#基础镜像:JDK8
FROM java:8

#维护者信息
MAINTAINER tfss 1255791430@qq.com

#镜像的操作指令
COPY ./tale /tale
ENV TZ=Asia/Shanghai
COPY startup.sh /startup.sh

CMD ["sh", "/startup.sh"]

