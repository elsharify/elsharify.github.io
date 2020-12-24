Some of the Daily needed cmdlets:
1- Setting proxy system wide:
# /etc/environment
http_proxy="http://user:Paswd@proxy:8080/"
https_proxy=$http_proxy
ftp_proxy=$http_proxy
HTTP_PROXY=$http_proxy
HTTPS_PROXY=$http_proxy
FTP_PROXY=$http_proxy
no_proxy=localhost,127.0.0.0,127.0.1.1,127.0.1.1,*local,172.21,*wrm.ae,*.wrm.abudhabi.ae,*.drm.gov.abudhabi,*.local

2- Setting proxy for apt:
# /etc/apt/apt.conf.d/proxy.conf
Acquire::http::Proxy "http://user:Paswd@proxy:8080/";

3- Setting proxy for yum:
/etc/yum.conf
proxy=http://proxy:8080/
proxy_username=User
proxy_password=Paswd

4- Setting VIM style:
#/home/drmadmin/.vimrc
colo desert
syntax on
set autoindent
set number
set bg=dark

5- Set no password for 
#/etc/sudoers.d/drmadmin
drmadmin        ALL=(ALL)       NOPASSWD:ALL
