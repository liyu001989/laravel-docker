FROM php:7.0-alpine
# 同步时区
RUN apk update && apk add ca-certificates && \
    apk add tzdata && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone
    # 
    # dpkg-reconfigure -f noninteractive tzdata