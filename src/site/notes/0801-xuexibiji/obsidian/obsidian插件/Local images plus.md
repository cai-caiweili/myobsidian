---
{"dg-publish":true,"aliases":null,"tags":["Local images plus","插件","obsidian插件","本地化图片"],"title":"Local images plus","permalink":"/0801-xuexibiji/obsidian/obsidian插件/Local images plus/","dgPassFrontmatter":true,"noteIcon":""}
---

## 用法

只需复制任何 Web 内容、Word/Open Office 内容并将其粘贴到常规笔记或画布中的笔记中。

从版本 0.15.0 开始，该插件还可以处理所有附件（文件/音频记录的屏幕截图/拖放）。

![00-fujian/b9171cf35ded9b38ea518fbaf8ac8183_MD5.gif](/img/user/00-fujian/b9171cf35ded9b38ea518fbaf8ac8183_MD5.gif)

在命令/菜单模式或自动模式下使用它（在设置中切换“自动处理”选项）：

![00-fujian/3967b5de94081e1b3933000a210ae633_MD5.png](/img/user/00-fujian/3967b5de94081e1b3933000a210ae633_MD5.png)

![00-fujian/b94d1aa2191541a1a5de5d9a999de6a1_MD5.png](/img/user/00-fujian/b94d1aa2191541a1a5de5d9a999de6a1_MD5.png)

`Download all media files (Plugin folder)`- 您的活动页面将被处理，附件将保存在插件设置中预先配置的文件夹中。

或者

`Download all media files (Obsidian folder)`- 您的活动页面将被处理，附件将保存在黑曜石设置中预先配置的文件夹中。

或者

`Download media files for all your notes`- 将处理您的保管库中的所有页面，对应于插件设置中的**“包含”参数。**

**注意：此插件可以一次更改您的所有笔记，因此您应该考虑定期备份文件。**

## 您还可以插入任何文件，例如：

`![mypdf](http://mysite/mypdf.pdf)`

`![mylocalfile](file:///mylinuxdisk/mysong.mp3)`

文件将被复制或下载到您的附件文件夹中。

![00-fujian/c5cb59490674c5ccb3fd781b145637eb_MD5.gif](/img/user/00-fujian/c5cb59490674c5ccb3fd781b145637eb_MD5.gif)

**注意：我不建议使用此插件来复制非常大的文件，因为尚未实现从磁盘读取缓冲。**

## 从版本 0.15.6 开始，该插件还允许您通过运行命令删除未使用的附件：

`Remove all orphaned attachments (Plugin folder)`

和

`Remove all orphaned attachments (Obsidian folder)`

第一个在活动笔记旁边的文件夹中搜索孤立的内容，而第二个则在所有未使用的附件中搜索所有笔记。（这需要您在黑曜石设置中设置一些根子文件夹）

从0.14.5版本开始，附件名称是根据MD5生成的，因此它们在保管库中非常唯一。

这意味着您可以将附件文件放置在保管库中的任何位置，用文件名替换标签中的绝对路径，Obsidian 仍将在您的注释中显示它。