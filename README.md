# hello-world

Try to make some edits to this branch.
Doesn't make any sense. 

- create a new branch
- test the edit command
- default using markdown grammar


关于github使用可以参考如下链接的文章:[repo 《GitHub使用指南》](https://raw.githubusercontent.com/xirong/my-git/master/how-to-use-github.md)


### Github SSH Key

关于本地客户端同远程Repository同步数据之间设置公钥的问题，默认使用的使用id_rsa：

1. 登录个人Github主页,进入Account Settings选项；
2. 通过 Settings -> SSH Keys -> New SSH key;
3. Title部分填写 **id_ras.pub**;
4. 在本地客户端如Linux上查看 ~/.ssh/id_ras.pub文件的内容，将其copy到"New SSH Key"中Key的部分，如果本地主机没有该文件，可以通过命令"ssh-keygen -t rsa"生成；
