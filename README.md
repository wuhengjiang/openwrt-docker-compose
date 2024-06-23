# openwrt-docker-compose

互联网上对于 OpenWRT 安装 Docker Compose 的相关内容的结论基本上有三种：安装旧版本、使用 ipk 文件，或者是无法安装

然而其实在 Docker 官方文档里就有着无比简单的方法能够让我们轻松安装 Docker Compose

已在 OpenWRT 上测试过正常运行


使用 docker compose 而非 docker-compose



DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
mkdir -p $DOCKER_CONFIG/cli-plugins
curl -SL https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64 -o $DOCKER_CONFIG/cli-plugins/docker-compose
chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose
docker compose version


DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
mkdir -p $DOCKER_CONFIG/cli-plugins
curl -SL https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-aarch64 -o $DOCKER_CONFIG/cli-plugins/docker-compose
chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose
docker compose version
