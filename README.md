# LearnGit

## 一、前戏
```cpp {.line-numbers}
//查看电脑是否安装git
git
//查看git版本
git --version
//查看包路径
which git
```
## 二、创建 ssh key ，配置git
1. 配置用户名和邮箱
```cpp {.line-numbers}
git config --global user.name "your_name"
git config --global user.email "your_email"
```
2. 生成 ssh key
```cpp {.line-numbers}
ssh-keygen -t rsa -C "your_email"
```
3. 复制 ssh key
```cpp {.line-numbers}
cat .ssh/id_rsa.pub
```
4. 链接验证
```cpp {.line-numbers}
ssh -T git@github.com
```
**如果连接不上去：**
1. 放弃ssh方式，用https方式连接
2. 在 {用户}/.ssh/ 目录下建立config文本文档，输入以下代码，端口指向443
```cpp {.line-numbers}
Host github.com
Hostname ssh.github.com
Port 443
```


