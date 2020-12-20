

# docs

 hello world



![在这里插入图片描述](https://gitee.com/imeichuan/imghosting/raw/master/img/20200709124001723.png)

``` \#!/bin/bash # 以下命令在原本的 bash 窗口中运行 cd /www/wwwroot/xxx.com git add -A git commit -m "backup" # 当运行到这一句的时候，ssh-agent 新建了一个 bash 窗口 # 而你也看到了这个窗口 ssh-agent bash # 但是下面这两句仍然是在原本的 bash 窗口中运行的 ssh-add /root/github git push -u origin master # 只是因为你执行完 ssh-agent bash 之后，切换到了新的 bash 窗口 # 所以你并不会看到这两句命令执行的回显 # 实际上 ssh-add 将会因为我前面说过的原因而不能添加密匙 # 所以 git push 自然会因为没有密匙而失败
`
```