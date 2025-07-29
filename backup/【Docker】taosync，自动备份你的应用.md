## 简介
TaoSync是一个适用于OpenList v3+的自动化同步工具/Sync for OpenList/AList。同步速度还是很不错的。

<img width="1891" height="657" alt="Image" src="https://github.com/user-attachments/assets/88d14548-a3c2-4e1f-81ce-6cdcdb2a3480" />

![Image](https://github.com/user-attachments/assets/dfe6abef-2f92-4eed-8828-ad37333ab59b)

## 部署
docker-compose如下：
```bash
services:
  taoSync:
    image: dr34m/tao-sync:latest
    container_name: taoSync
    restart: always
    ports:
      - "8023:8023"
    volumes:
      - ./data:/app/data
```
启动项目
```bash
docker-compose up-d 
```
## 使用技巧
- OpenList中存储中添加本地文件
- OpenList中存储添加网盘
- Docker登录后台,查看初始密码
- 登录后可以设置把本地文件备份到网盘

## 排除项规则
taoSync规定的排除项根目录为同步来源或目标目录，例如你的来源目录为/baidu/pan/，使用规则/123321/*将忽略目录/baidu/pan/123321/下的文件；使用/baidu/*不会有效果。

```gitignore
.*              表示忽略所有 . 开头的文件和目录
*.a             表示忽略所有 .a 结尾的文件
/a.jpg          表示仅仅忽略项目根目录下的 a.jpg 文件，不包括 /abc/a.jpg
data/:          表示忽略data目录下的所有内容，不忽略 data 文件
/data:          表示忽略根目录下的data文件
/*.pdf:         表示忽略/a.pdf，不忽略 /doc/a.pdf
**/a.txt:       表示忽略/a.txt,a/a.txt,a/b/a.txt等
a/**/b.txt:     表示忽略a/b.txt, a/x/b.txt,a/x/y/b.txt等
/mtk/do.doc     表示过滤某个具体文件
fd1/*           表示忽略/fd1/，/fd0/df1/等下所有文件
/fd1/*          表示忽略/fd1/下所有文件，不包括/fd0/fd1/,/fd2/fd1/等
```

![Image](https://github.com/user-attachments/assets/35ce8087-8888-4fc3-8231-c0a09896fa78)

## 定时运行设置
每周一早上7点运行
- day_of_week: 1
- hour: 7
![Image](https://github.com/user-attachments/assets/18f4776c-cc1c-4478-891b-e20fab1f7180)

## 参考文章
- [Github TaoSync]https://github.com/dr34m-cn/taosync
- [taoSync排除项简易教程](https://dr34m.cn/2024/09/newpost-60/)
- [cron配置简介](https://dr34m.cn/2024/08/newpost-58/)