---
{"dg-publish":true,"aliases":"电脑主板","tags":["华擎 bios itx"],"title":"华擎 J3455-ITX 升级 BIOS 固件及设置","permalink":"/0201//nas/j3455-itx-bios/","dgPassFrontmatter":true,"noteIcon":""}
---


**查看【 [Synology 与 XPEnology](https://divineengine.net/more/special/synology-and-xpenology/) 】专题可浏览更多内容**

## 升级 BIOS 固件

暴风二期的主板是华擎的「J3455-ITX」，在开始使用前需要先升级一下 BIOS 固件，如果你不知道你当前的固件版本，将暴风二期重启，按 `F2` 或 `Delete` 键进入 UEFI：

![[00 fujian/d17950d96813bc2a31f0ff71ecca621a_MD5.webp]]

如上图，你可以在底部左侧按钮修改语言为「简体中文」。

然后在「主画面」下的「UEFI 版本」查看版本，我这里已经升级到「P1.80」了，如果你的是旧版本就升级吧。

![[00 fujian/39729c5443ee8ecfa8c0289629b14c31_MD5.webp]]

可以在「工具」界面里更新，截至写稿时最新的固件为「P1.80」，且需要注意，如果你的固件版本低于「P1.60」需要先更新至「P1.70」再更新到「P1.80」。

华擎 J3455-ITX BIOS 固件下载：[官网下载](https://www.asrock.com/mb/Intel/J3455-ITX/#BIOS) | [天翼云盘](https://cloud.189.cn/t/3MnEfuveEfum)

在上面给出的官方网站下载固件后，将压缩包如 `J3455-ITX(1.70)ROM.zip` 里的固件 `APLITX1.70` 解压出来放到 FAT32 格式的 U 盘里即可。

接着将 U 盘接上暴风二期并重启，按 `F2` 或 `Delete` 键再次进入 BIOS 的「工具」界面（可以使用键盘的上下左右方向键移动菜单），选择「Instant Flash」并回车，可以看到如上图，再次回车。

![[00 fujian/8bc0bda032a3a3fe4a145b4d14dbc117_MD5.webp]]

选择「是」。

![[00 fujian/cc0810068c17357cebfaa181a0098413_MD5.webp]]

按回车重启，依然按 `F2` 或 `Delete` 键再次进入 BIOS。

## 设置 BIOS 固件

![[00 fujian/f66f1f5cbd4cf389a154900c60835fc5_MD5.webp]]

进入「高级」下的「CPU 配置」：

-   将「Intel SpeedStep 技术」及「CPU C 状态支持」设置为「关闭」；
-   将「Intel 虚拟化技术」及「VT-d」设置为「开启」；
-   将「Power Gear」设置为「Sport Mode」；

![[00 fujian/9e2a1a159a6f995433222b42f5dc07fa_MD5.webp]]

按 `Esc` 回到上一层然后进入到「芯片组配置」：

-   将「板载 LAN」设置为「开启」以启用板载网卡；
-   如果需要在断电后来电时自动启动可以将「交流/电源断电恢复」设置为「开启」；

![[00 fujian/2b9d8ee3600e38a64a7b36c0010667a5_MD5.webp]]

回到上一层然后进入到「ACPI 配置」：

-   如果需要网卡唤醒将「PCIE 设备开机」设置为「开启」；

![[00 fujian/c7abe847e651eb77bba6a54c3143b80e_MD5.webp]]

然后在「退出」界面选择「保存更改并退出」然后回车选择「是」即可。

到这里 BIOS 就设置完成了。

另外，使用黑群晖 DSM918+ 开机进入系统慢可查看 [华擎 J3455 使用 XPEnology DSM918+ 启动慢解决方法](https://divineengine.net/article/asrock-j3455-xpenology-dsm918-slow-boot-solution/)
已经修改完毕！