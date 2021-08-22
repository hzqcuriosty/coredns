> 部署coredns 需colnecredns.yaml

    git clone https://github.com/hzqcuriosty/coredns.git

> 部署coredns

    cd conredns
    kubectl  apply -f coredns.yaml
    
> 验证

    kubectl apply -f busybox.yaml
    
    #注意使用1.28.4之前的版本之后的版本有bug

>coredns 镜像

    如coredns yaml文件中的镜像image: docker.io/coredns/coredns 不能下载可修改为image: huochaoying/coredns:v1

>注意pod启动失败：

    如部署报探测失败可以注释  livenessProbe   readinessProbe 探针
