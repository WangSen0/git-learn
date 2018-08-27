# aptly-cli #
aptly是一个deb包管理软件。
# aptly-cli的获取
## 从源码编译安装
由于aptly使用go语言编写，如果选择源码编译，还请安装好[go语言环境](https://golang.org/doc/install)。guldan proxy 使用glide进行依赖包的管理，所以还请安装[glide](https://github.com/Masterminds/glide)。
```
git clone this repo to your GOPATH/src
cd aptly-cli
glide install
go build
```
在aptly-cli顶层目录下，你就得到了`aptly-cli`的启动文件
# aptly-proxy的使用
```
`./aptly-cli -help`会列出所有可以使用的命令
列出所有仓库        aptly-cli repo list
创建仓库            aptly-cli repo create -distribution=dis -component=com testing
增加分支            aptly-cli repo add -distribution=dis -component=com testing
删除分支            aptly-cli repo delete -distribution=dis -component=com testing
查询仓库下的包      aptly-cli repo search distribution prefix
移除仓库下的某个包  aptly-cli repo remove -distribution=dis -component=com -key=key prefix
上传文件到仓库      aptly-cli file upload -filepath=filepath -distribution=dis -component=com testing
查看版本            aptly-cli version
```