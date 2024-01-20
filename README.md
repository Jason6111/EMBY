## 请勿擅自使用  
地址1(32位token获取)：https://aliyuntoken.vercel.app/  
地址2(280位token获取)：https://alist.nn.ci/tool/aliyundrive/request  
地址3【重点】：转存目录的folder id
```
bash -c "$(curl https://raw.githubusercontent.com/Jason6111/EMBY/main/update_new.sh)"
```
```
bash -c "$(curl https://raw.githubusercontent.com/Jason6111/EMBY/main/emby.sh)" -s /媒体库目录  /配置目录
```
```
bash -c "$(curl https://raw.githubusercontent.com/Jason6111/EMBY/main/resilio.sh)" -s /媒体库目录  /配置目录
```
/每日更新/电视剧
```
BHB7NOQ4IQKOWZPCLK7BIZXDGIOVRKBUL
```
/每日更新/电影
```
BCFQAYSMIIDJBWJ6DB7JXLHBXUGYKEQ43
```
/电影/2023
```
BGUXZBXWJG6J47XVU4HSNJEW4HRMZGOPL
```
/纪录片（已刮削）
```
BDBOMKR6WP7A4X55Z6BY7IA4HUQ3YO4BH
```
config
```
BHKGO66XO6IE6JMWLUYXQWT4WCMRSEJV5
```
chmod -R 777 xxx/xxx//每日更新/电视剧等

# xiaoya-tvbox
```
docker run -d -p 4567:4567 -p 5344:80 -e ALIST_PORT=5344 -v /mnt/nvme0n1p3/docker/xiaoya:/data --restart=always --name=xiaoya-tvbox haroldli/xiaoya-tvbox:latest
```
清理
```
bash -c "$(curl -s https://raw.githubusercontent.com/Jason6111/EMBY/main/aliyun_clear.sh | tail -n +2)" -s 5
```
24小时不间断同步和保持emby开启并同步emby config的方法，保留你自己的配置（用户，密码，播放记录。。。）

前提：config的同步目录是 /媒体库目录/config_sync （/媒体库目录 是你自己设置的，千万不要直接输入“/媒体库目录"，它可以是  /mnt/emby 或者 /volume1/Docker/xiaoya/emby .....）
第一次自己
mkdir /媒体库目录/config_sync && chmod 777 /媒体库目录/config_sync
然后把resilio的同步config保存到这个目录（也就是容器里的 /sync/config_sync )，resilio 的docker安装
bash -c "$(curl http://docker.xiaoya.pro/resilio.sh)" -s /媒体库目录
如果配置文件夹不是默认的 /etc/xiaoya，那么添加额外的参数
bash -c "$(curl http://docker.xiaoya.pro/resilio.sh)" -s /媒体库目录  /你的xiaoya配置目录

自己设置crontab定时任务，下面是每天早上6点更新emby config一次
0 6 * * * bash -c "$(curl http://docker.xiaoya.pro/sync_emby_config.sh)" -s /媒体库目录
或者是每隔3天早上6点更新emby config一次
0 6 */3 * * bash -c "$(curl http://docker.xiaoya.pro/sync_emby_config.sh)" -s /媒体库目录
