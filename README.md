# images-sysncer

## 修改镜像名

文件名：.github/workflows/sync-image-example.yml
 修改内容：
```shell
- name: Use Skopeo Tools Sync Image to Docker Hub
      run: |
         skopeo copy docker://docker.io/dzzoffice/centos_bt_imagick_ffmpeg:latest docker://registry.cn-hangzhou.aliyuncs.com/nookvoice/centos_bt_imagick_ffmpeg:latest
      # 使用 skopeo 工具将镜像同步到阿里云个人仓库中，使用时请自行源和目标修改仓库名称和镜像名称 
```

## 提交触发部署
Actions 界面查看部署状态

##  下载 
同步成功后可在私有仓库查看和下载镜像
```shell
docker pull registry.cn-hangzhou.aliyuncs.com/nookvoice/seatunnel:2.3.8
```

重新命名镜像：
```shell
docker tag registry.cn-hangzhou.aliyuncs.com/nookvoice/seatunnel:2.3.8 apache/seatunnel:2.3.8
```
