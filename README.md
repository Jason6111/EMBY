```
bash -c "$(curl https://raw.githubusercontent.com/Jason6111/EMBY/main/update_new.sh)"
```
每天早6点晚10点清理TXT文档
```
bash -c "$(curl -s https://raw.githubusercontent.com/Jason6111/EMBY/main/aliyun_clear.sh | tail -n +2)" -s 3 -tg
```
```
bash -c "$(curl https://raw.githubusercontent.com/Jason6111/EMBY/main/emby.sh)" -s /媒体库目录
```
