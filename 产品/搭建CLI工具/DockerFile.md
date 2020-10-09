### Dockerfile

```dockerfile
FROM nginx
COPY ./dist /usr/share/nginx/html
COPY nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80
```

### 生成镜像

```shell
docker build -t jevin:test .
```

### Docker镜像导入导出

```shell
// 导出
docker save jevin:test > ./jevin.tar.gz
// 导入
docker load>jevin.tar.gz
```

### 部署

通过Docker镜像进行部署，提供南瑞docker镜像，以及补充的参数

支持的参数

1. nginx反代的地址：BACKEND_URL(http 地址)和BACKEND_URL2(websocket的地址)
2. 全局变量的地址：可以通过APP_*的方式进行部署

