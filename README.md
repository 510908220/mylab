# mylab
整理自己平时的开发环境并打包到vagrant box内,  这样可以在家或公司迅速的得到一把`瑞士军刀`.

默认进去是`vagrant`用户. `su root`输入`vagrant`切换到`root`用户.

## 工具

- `Oh-My-Zsh`
- `python 3.6`: 输入`python`启动.
- `httpie`: 输入`http`启动. 可以替代wget等.
- `mycli`:  输入`mycli`启动. mysql命令行增强.
- `docker`
- `jupyter`


## portainer

docker ui, 点击http://192.168.0.88:9000 打开,密码:`letmegoletmego`

## Jenkins

点击[http://192.168.0.88:32770/](http://192.168.0.88:32770/)进入jenkins首页:

- 账号:`admin`
- 密码:`letmegoletmego`

要是jenkins插件安装失败的话,可以手动下载插件，然后拷贝到jenkins的插件目录:

- `docker exec  -it jenkins /bin/bash`
- 拷贝插件到`/var/jenkins_home/plugins`
- `docker restart jenkins`

## 数据库

> ip都为192.168.0.88

| 数据库   | 端口/账号/密码                  | 描述   |
| ----- | ------------------------- | ---- |
| mysql | 32768/root/letmegoletmego |      |
| mongo | 32780/admin/25CllgIcQNDM  |      |
| redis | 32772                     |      |

## 使用

- 下载`lab.box`, 下载地址:[http://pan.baidu.com/s/1gfBUWoV](http://pan.baidu.com/s/1gfBUWoV)
- `git clone https://github.com/510908220/mylab.git `
- `cd mylab && vageant up`

