# laravel-docker
使用 docker 开发 laravel

nginx，php 使用很小的 alpine 作为基础镜像, mariadb 官方还没有 alpine 的 tag，已经有相关的 issue，所以就不纠结了，还是用官方的靠谱。

## Usage
- docker-compose up -d
- 把项目放在 www 目录中
- 在 nginx/config 目录中配置每个站点的
- php-fpm 中装了 composer, 可以进入后进行 install 操作（alpine 中没有 bash，需要使用 sh 进入）
