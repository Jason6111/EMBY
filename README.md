地址1(32位token获取)：https://aliyuntoken.vercel.app/
地址2(280位token获取)：https://alist.nn.ci/tool/aliyundrive/request
地址3【重点】：转存目录的folder id
```
bash -c "$(curl https://raw.githubusercontent.com/Jason6111/EMBY/main/update_new.sh)"
```
每天早6点晚10点清理TXT文档
```
bash -c "$(curl -s https://raw.githubusercontent.com/Jason6111/EMBY/main/aliyun_clear.sh | tail -n +2)" -s 3 -tg
```
```
bash -c "$(curl https://raw.githubusercontent.com/Jason6111/EMBY/main/emby.sh)" -s /媒体库目录  /配置目录
```
```
0 20 * * * docker restart xiaoya
```
