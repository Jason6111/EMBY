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
