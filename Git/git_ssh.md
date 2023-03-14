# 使用SSH连接GitHub

**步骤一：生成公钥和私钥**

打开cmd窗口，输入：`ssh-keygen -t rsa -C "xxxx@xx.com"`

```
Generating public/private rsa key pair.
Enter file in which to save the key (C:\Users\233/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in C:\Users\233/.ssh/id_rsa
Your public key has been saved in C:\Users\233/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:IHVzezmGZmDaiJzZiEKzkuF72nUNPr1THoxCE8rz98Q cgying99@qq.com
The key's randomart image is:
+---[RSA 3072]----+
|.o    ..= .      |
|oooo.B.*.+ o .   |
|+o. B+=+. = =    |
|...  .=.=o+o .   |
| . . . *S= E     |
|  + . . + * .    |
| . .     o o     |
|          .      |
|                 |
+----[SHA256]-----+
```

1.默认保存路径；2.“passphrase”密码可以为空

路径为`C:\Users\233\.ssh`，会生成两个文件

id_rsa：代表私钥    id_rsa.pub：代表公钥

**步骤二：在GitHub上添加公钥id_rsa.pub**

打开GitHub，点击右上角头像，选择setting

在左侧选择”SSH and GPG keys“

点击右上角“New SSH key”

用记事本打开“id_rsa.pb”， 复制全部内容到Key 中，title可自由设置



早GitHub上添加公钥后，可以直接在”Git Bash“中使用git clone/push/pull等指令连接仓库