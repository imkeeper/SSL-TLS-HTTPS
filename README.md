# SSL-TLS-HTTPS

## Nginx Docs
* [ `ngx_http_ssl_module` ](http://nginx.org/en/docs/http/ngx_http_ssl_module.html)
* [Configuring HTTPS servers](http://nginx.org/en/docs/http/configuring_https_servers.html)
  (3/31)
* [SSL/TLS Offloading, Encryption, and Certificates with NGINX and NGINX Plus](https://www.nginx.com/blog/nginx-ssl/)

## 源码剖析
## 密码套件
* [ECC加密算法入门介绍](https://www.pediy.com/kssd/pediy06/pediy6014.htm) (P)
* [Freebuf:椭圆曲线算法（ECC）学习](http://www.freebuf.com/articles/database/155912.html) (P)
* [Freebuf:安全科普 | 从CTF中初认识RSA](http://www.freebuf.com/articles/rookie/154183.html)
* [__AES简介__](https://github.com/matt-wu/AES)
* [__AES加密与Base64编码__ 快速入门](http://www.wxappclub.com/topic/709)

## TLS1.3
* [Wiki:TLS1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3)
* [快速入门 TLS 1.3:改进延迟，部分握手加密](https://yatesun.com/2017/05/tlsv1.3/)
* [试玩 nginx mainline 1.13 的 TLSv1.3](https://www.starduster.me/2017/04/27/nginx-1-13-with-tls13/)
* [基于TLS1.3的微信安全通信协议mmtls介绍](https://github.com/WeMobileDev/article/blob/master/%E5%9F%BA%E4%BA%8ETLS1.3%E7%9A%84%E5%BE%AE%E4%BF%A1%E5%AE%89%E5%85%A8%E9%80%9A%E4%BF%A1%E5%8D%8F%E8%AE%AEmmtls%E4%BB%8B%E7%BB%8D.md)
* [OpenSSL Blog: Using TLS1.3 With OpenSSL](https://www.openssl.org/blog/blog/2018/02/08/tlsv1.3/)
* [NetScaler TLS 1.3 Testing With OpenSSL](https://support.citrix.com/article/CTX229287)
* [Deploying TLS 1.3: the great, the good and the bad ](https://www.youtube.com/watch?v=0opakLwtPWk) （P）

## HTTPS性能优化实践
* [腾讯HTTPS性能优化实践](http://baijiahao.baidu.com/s?id=1559840813865463&wfr=spider&for=pc)
* [Infoq 罗成:HTTPS的性能优化](http://www.infoq.com/cn/presentations/performance-optimization-of-https)
* [京东金融私有云HTTPS性能优化实践](http://www.infoq.com/cn/articles/jingdong-financial-private-cloud-https-practices)
## 精华
* [TLS/SSL 高级进阶](https://segmentfault.com/a/1190000007283514)
* [__深入TLS实现: golang TLS分析__](http://www.cnhalo.net/2017/03/15/dive-into-tls-with-golang/)

* [Traffic Analysis of an SSL/TLS Session](http://blog.fourthbit.com/2014/12/23/traffic-analysis-of-an-ssl-slash-tls-session)
* [golang与TLS实现](https://hsulei.com/2016/11/29/golang%E4%B8%8ETLS%E5%AE%9E%E7%8E%B0/)

## Git Usage
* git log获取提交的文件列表
 
 ```
 *git log --stat
 * git log --oneline --name-only -2
# --name-only 只显示文件名 
git log --name-only -1
# --pretty=format:"" 格式化commit message 这里什么都不显示
git log --pretty=format:"" -1
# 最终
* git log --pretty=format:"" --name-only  -1 
 ```
* 将master分支内容合并到dev分支:
	* https://blog.csdn.net/qq_34206198/article/details/52055395
  
  ```
  流程如下：
	一、将分支切换到master

	git checkout master

	二、将代码pull到本地
	git pull

	三、修改冲突
	
	四、提交到本地
	git add .

	git commit -m "merge"
	
	五、切换到你所在分支dev

	git checkout dev


	六、merge

	git merge master

	七、将本地内容push到dev分支
	git push

  ```
## 编译nghttp
```
git clone https://github.com/tatsuhiro-t/nghttp2.git
cd nghttp2
git submodule update --init
autoreconf -i
automake
autoconf
./configure --enable-app --prefix=/tmp/nghttp
```
## 杂项
* [***Tmux使用手册](http://louiszhai.github.io/2017/09/30/tmux/)

* [NSS Key Log Format](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/NSS/Key_Log_Format)
* [升级vim8.0](https://www.linuxprobe.com/vim8-0-linux.html)
* 
```
yum install ncurses-devel
wget https://github.com/vim/vim/archive/master.zip
unzip master.zip
cd vim-master
cd src/
./configure
make
sudo make install
vim
```
* [zsh-completions](https://github.com/zsh-users/zsh-completions)
	
	```
对于 CentOS 7，请以根用户 root 运行下面命令：
cd /etc/yum.repos.d/
wget https://download.opensuse.org/repositories/shells:zsh-users:zsh-completions/CentOS_7/shells:zsh-users:zsh-completions.repo
yum install zsh-completions
对于 CentOS 6，请以根用户 root 运行下面命令：
cd /etc/yum.repos.d/
wget https://download.opensuse.org/repositories/shells:zsh-users:zsh-completions/CentOS_6/shells:zsh-users:zsh-completions.repo
yum install zsh-completions
```
*[bash-completion](https://github.com/scop/bash-completion)

	```
	https://unix.stackexchange.com/questions/21135/package-bash-completion-missing-from-yum-in-centos-6
	yum install epel-release.noarch bash-completion.noarch
	https://packages.ubuntu.com/trusty-updates/bash-completion
```
* brew bundle dump 

