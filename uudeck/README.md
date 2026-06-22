# UU 加速器 Steam Deck 插件版

[UU 加速器](https://uu.163.com/) 官方推出的 [Steam Deck 插件版](https://baike.sowellwell.com/router/item/64b8d44c04cb117f2316b062.html)。

本包修改自 [这个 AUR 包](https://aur.archlinux.org/packages/uudeck)，主要修改了如下部分：

* 从官方直接下载对应脚本而无须维护者手动上传；
* 将插件的依赖脚本存放目录从 `/home/${whoami}/uu` 迁移到 `/var/lib/uu`；
* 将插件的配置文件从 `/home/${whoami}/uu/uuplugin_monitor.config` 迁移到 `/etc/uu/uuplugin_monitor.config`；
* 将插件的运行目录从 `/tmp/uu` 迁移到 `/var/lib/uu/run`。

本包修改了官方插件，使其不会到处乱拉依赖文件（附属脚本、配置文件等），同时避免了重启系统后需要在 App 内删除设备重新绑定的麻烦问题。

## 使用

启动 `uuplugin.service` 这个服务，然后在 UU 主机加速 App 中绑定 Steam Deck 即可。注意每次需要加速游戏时都需要启动该服务。您也可以启用该服务以避免每次都需要手动启动。
