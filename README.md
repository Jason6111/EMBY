## 请勿擅自使用  
m3u转成embyiptv
```
python3 m3utoxml.py
```
一键
```
bash -c "$(curl --insecure -fsSL https://ddsrem.com/xiaoya_install.sh)"
```
启用tvtoken输入  
```
fuckaliyun
```
TVBOX
```
http://xiaoya.host:5678/tvbox/my_ext_jar.json
```
地址1(32位token获取)：https://aliyuntoken.vercel.app/  
地址2(280位token获取)：https://alist.nn.ci/tool/aliyundrive/request  
地址3【重点】：转存目录的folder id  
```
0 5 * * * docker restart xiaoya
```
#方法1
```
bash -c "$(curl https://raw.githubusercontent.com/Jason6111/EMBY/main/update_new.sh)"
```
#方法2
```
bash -c "$(curl https://raw.githubusercontent.com/Jason6111/EMBY/main/update_new.sh)" -host
```
#方法3
```
bash -c "$(curl http://docker.xiaoya.pro/update_new.sh | sed 's#/etc/xiaoya#/mnt/nvme0n1p3/docker/xiaoya#g')" -s host
```

猫影视配置  
```
http://alist:alist@xxx.xxx.xxx.xxx:5678/tvbox/cat/my_cat.json
```
#数据更新
```
bash -c "$(curl http://docker.xiaoya.pro/update_data.sh)"
```
#uccookie
在/etc/xiaoya  下面创建uc_cookie.txt 然后将uc网盘文件页面按F12 出来的界面搜索sort 然后在找cookie 填入，就好了。  
```
docker exec -i xiaoya /check_uc_cookie.sh update
```
#问题  
```
docker exec xiaoya rm -rf /data/data/version.txt  && docker restart xiaoya
```
