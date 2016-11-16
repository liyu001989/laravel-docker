# laravel-docker
使用 docker 开发/部署 laravel

包括 nginx，php-fpm，php-cli-daemon(supervisor)，redis，mariadb

除了mariadb，都是使用 alpine 作为基础镜像。

国内用户可以使用 [gfw](https://github.com/liyu001989/laravel-docker/tree/gfw) 分支

## Usage

- 默认的项目放在 www 目录中
- 在 nginx/conf.d 目录中配置每个站点的
- php-cli-daemon 中装了 supervisor，配置 worker 到 supervisor.d 中即可。
- docker-compose up -d
- php-fpm 中装了 composer, 可以进行 composer 安装

## Tips
- alpine 中没有 bash，需要使用 sh 进入。或者通过docker exec 在宿主机执行
- 时区我挂载了/etc/localtime，所有就是宿主机的时区
