### Golang IP代理池

#### 安装  
基于Golang 1.9开发
```
go get github.com/CX1ng/proxypool
```
#### 依赖管理  
使用Golang依赖管理工具[glide](https://github.com/Masterminds/glide)进行项目依赖管理。可以使用`glide`命令，亦可使用`make`相关命令进行管理。

下载项目的相关依赖库：  
```
glide install
```
更新依赖库，以获取新版本的依赖，注意清除~/.glide/cache文件夹  
```
glide update
```
#### 编译及启动  

更新依赖文件，同`glide up`  
```
make update_deps
```
下载相关依赖库，同`glide install`  
```
make deps
```
按照当前操作系统进行编译，生成bin文件  
```
make build
```
编译bin文件为linux版本  
```
make linux_build  
```
执行下载和linux编译两个操作，同`make deps;make linux_build`  
```
make
```
编译结束后，会在当前项目下生成bin文件夹，执行以下命令以启动程序  
```
${PROJECT}/bin/proxypool --config config/config.dev.toml
```

### 现已支持的数据源
[快代理](https://www.kuaidaili.com/)  
[西刺代理](http://www.xicidaili.com/nn/1)

### TODO List
- [x] 代理IP验证器  
- [ ] 代理IP定时验证
- [x] Makefile
- [ ] Dockerfile
- [ ] 获取存储的代理IP
- [ ] Restful API
- [ ] log