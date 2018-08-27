# aptly-proxy
aptly-proxy是一个deb包管理软件。
# aptly-proxy获取
## 从源码编译安装
由于gudlan proxy使用go语言编写，如果选择源码编译，还请安装好[go语言环境](https://golang.org/doc/install)。guldan proxy 使用glide进行依赖包的管理，所以还请安装[glide](https://github.com/Masterminds/glide)。
```
cd aptly-proxy
glide install
go build
```
在aptly_proxy顶层目录下，你就得到了`aptly-proxy`的启动文件
# aptly-proxy的启动
`./aptly-proxy -help`会列出所有可以使用的命令
```
 -config string
        config file (default "./config.yaml")
  -help
        show help
  -version
        print current version
```
## config参数的值表示配置文件。以下是几个重要配置项的说明：
    - name   项目名字
    - appkey 项目的key
    - logformat  日志格式文件位置
    - logfile    日志文件位置
    - listen     服务监听端口号，例如8080
    - domain     aptly-proxy服务地址，例如http://192.168.1.2:8080
    - auth       单点登录地址，例如http://bigdata-view.cootekservice.com:50200
    - aptlyUrl   aptly服务地址，例如http://192.168.1.3:8080