# pccold

**douyu斗鱼 自动化工具 主播上线通知 & 视频自动录制 & 弹幕抓取 & 下载斗鱼视频**

2019/2/19 by DKZ


**streamlink无法下载直播的问题，请结合[pccold_puppeteer](https://github.com/davidkingzyb/pccold_puppeteer)使用**

## Install

use pip3

`$ sudo pip3 install pccold`

or download source code

`$ sudo python3 setup.py install`

## Usage

### 自动录像

`$ pccold`

后台运行
`$ nohup pccold &`

### 弹幕抓取

`$ pccolddanmu`

### 下载斗鱼视频

`$ pccoldvideo`

编辑下载列表
格式`[文件名](URL路径)`

`$ pccoldvideolist`

## Setting

`$ sudo vi /etc/pccold.conf`

```
room_id="cold" #斗鱼房间ID
room_num=20360 #斗鱼房间数字ID
video_author="vJGdy0qrKwXy"
stream_type="medium" #录像质量 source|medium|low
is_cut=true #是否分段
how_long=1800 #录像分段长度(秒)
is_bypy=true #是否使用bypy上传百度云
is_bypy_rm=false #上传百度云后删除
download_path="/home/dkz/download" #录像保存路径
videolist_path="/home/dkz/videolist.md" #批量下载斗鱼视频列表
log_path="/home/dkz/pccold.log"
env="dev"

#邮件配置
my_email="recv@xx.com"
mail_sender="send@xx.com"
mail_passwd="xxx"
mail_host="xxx"
mail_port=25 #exmail.qq 465 or 25
pccold_contact="\n\npccold by DKZ \n---------------------\ngithub:https://github.com/davidkingzyb/pccold\ncontact:davidkingzyb@qq.com  @__DKZ__\naboutme:https://davidkingzyb.tech\n"

#danmu
username="visitor9986987"
uid="1167614891"

```

## Dependence

- python3
- [streamlink](https://github.com/streamlink/streamlink)
- [bypy](https://github.com/houtianze/bypy)
- [psutil](https://github.com/giampaolo/psutil)
- [websocket-clinet](https://github.com/websocket-client/websocket-client)
- [pystt](https://github.com/dust8/pystt)








