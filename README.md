
## 部署步骤

1. fork本仓库
2. 在`Dockerfile`内第3-5行修改自定义设置，说明如下：

`AUUID`：用来部署节点的UUID，如有需要可在[uuidgenerator](https://www.uuidgenerator.net/)生成

`CADDYIndexPage`：伪装站首页文件

`ParameterSSENCYPT`：ShadowSocks加密协议

3. 去[Docker Hub](https://hub.docker.com/)注册一个账号，如有账号可跳过
4. 编辑Actions文件`docker-image.yml`，按照“name: Docker Hub ID/自定义镜像名称”格式修改第13行
5. 添加Actions的Secrets变量，变量说明如下

`DOCKER_USERNAME`：Docker Hub ID

`DOCKER_PASSWORD`：Docker Hub 登录密码

6. 打开某容器云主页，新建一个应用
7. 应用配置如下所示

`Docker Image`：Docker Hub镜像地址，格式为“docker.io/Docker Hub ID/自定义镜像名称”

`Container size`：部署配置，一般默认即可

`Port`：80

Environment variables：`Key`：PORT，`Value`：80
`Name`：自己定义
