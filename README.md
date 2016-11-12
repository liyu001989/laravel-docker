# laravel-docker
使用 docker 开发/部署 laravel

包括 nginx，php-fpm，php-cli-daemon，redis，mariadb

除了mariadb，都是使用 alpine 作为基础进项。

## Usage
- 默认的项目放在 www 目录中
- 在 nginx/conf.d 目录中配置每个站点的
- docker-compose up -d
- php-fpm 中装了 composer, 可以进入后进行 install 操作（alpine 中没有 bash，需要使用 sh 进入）
- php-cli-daemon 中是 php-cli-daemon/supervisor ，配置 worker 到 supervisor.d 中即可。
