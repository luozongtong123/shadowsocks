# shadowsocks
```
sudo touch /etc/shadowsocks.json
sudo nano /etc/shadowsocks.json
sudo nano /etc/rc.local
```


add below to /etc/shadowsocks.json

```
{
    "server":"*.*.*.*",
    "server_port":8388,
    "local_address": "127.0.0.1",
    "local_port":1080,
    "password":"*",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false
}
```


add this line to /etc/rc.local
```
ssserver -c /etc/shadowsocks.json -d start
```

