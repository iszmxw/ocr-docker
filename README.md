# 免费 ocr
一个实用的免费 OCR 服务

## 从 docker 运行

```bash
# 方法 1 后台启动
docker run -itd --name=ocr --net=host iszmxw/ocr:3.0 bash

# 方法 2 指定端口后台启动
docker run -itd --name=ocr -p 3389:3389 -p 1224:1224 iszmxw/ocr:3.0 bash

# 二选一

# 启动拉取过程
Unable to find image 'iszmxw/ocr:3.0' locally
3.0: Pulling from iszmxw/ocr
96d54c3075c9: Already exists 
1db0bfccf166: Already exists 
4cd5305fa16f: Pull complete 
Digest: sha256:11aeaead7c058b8dbcee138f34729d918ccee2da309c4dc2b50a53225159476c
Status: Downloaded newer image for iszmxw/ocr:3.0
60438a50023ef1e86bfd8f6631e95d6d65f43fe49f1a8a7b20b6164ca31c3e15
# 记住启动后的容器id，上面的那一行
```

## 进入容器

```bash
docker exec -it 60438a50023ef1e86bfd8f6631e95d6d65f43fe49f1a8a7b20b6164ca31c3e15 bash
```

## 启动 xrdp 用于远程桌面链接

```bash
service xrdp restart
# 下面这个也启动一下，不然有些抱错日志
service dbus start

# 到这里结束啦 开始退出容器
```


## 好了下面开始使用远程连接来控制服务器

- mac 可以下载一个 `Microsoft Remote Desktop`
<img width="167" alt="image" src="https://github.com/iszmxw/ocr/assets/31272102/16f2ff7f-d5cf-40b5-b06f-1c071402b8b8">

- windows 用户可以使用自带的远程

```
# Win+R 输入
mstsc
# 回车 吊起远程连接
```


## 输入服务器的 ip 地址

- 账号：`wineuser`
- 密码：`ethanyep`

![image](https://github.com/iszmxw/ocr/assets/31272102/d0ec322b-8aa9-4e35-8b91-266be22a73da)


### 右键唤起菜单

<img width="1512" alt="image" src="https://github.com/iszmxw/ocr/assets/31272102/bc0952f9-ee07-4ca5-8e8d-bb51cc56e451">

### 打开终端

<img width="1512" alt="image" src="https://github.com/iszmxw/ocr/assets/31272102/c35e21e2-c879-4c11-ae92-045634d7fb27">

### 启动 OCR 服务

```bash

```

<img width="1512" alt="image" src="https://github.com/iszmxw/ocr/assets/31272102/11a57a9b-a778-4041-a3ff-e53ff10752b5">


### End 好了你可以写你的业务了

### 浏览器输入 http://ip:1224 可以看到 `OCR` 版本号

<img width="432" alt="image" src="https://github.com/iszmxw/ocr/assets/31272102/6e2643aa-348f-43d1-be2b-2444c9a5cc6d">







