[toc]
# vscode 和 github 牵手方法

## 大致逻辑
实现的目标是 vscode 下的内容再 github 仓库中进行同步；
  - 用 SSH 进行牵手。 **产生密钥** 用的的代码是：
  ```
  ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
  ```
  注意：在 terminal 中运行，引号内的邮件地址进行替换。按 enter 后，除了更改存储位置信息。

- 将密钥记录在电脑上：
```
eval "$(ssh-agent -s)
```
接下来在：
```
ssh-add /Users/you/.ssh/id_rsa
```
注意替换 you 的名称；
- 密钥产生成功

```
Identity added: /Users/you/.ssh/id_rsa
```

详细过程参阅[程式学徒](https://zacklive.com/github-vscode/)

