### 查看SSD是否开启了Trim支持
以管理员身份运行CMD，输入``fsutil behavior query disabledeletenotify``如果显示结果为``DisableDeleteNotify=0``，说明已启用，如果为``DisableDeleteNotify=1``说明未启用。

### 开启trim
以管理员身份运行CMD，输入``fsutil behavior set disabledeletenotify 0``

### 关闭trim
以管理员身份运行CMD，输入``fsutil behavior set disabledeletenotify 1``