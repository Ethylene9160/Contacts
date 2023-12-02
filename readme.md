Thx to Liferlifer. There's a [Perfact chatting paper](https://github.com/LiferLifer/TransferChan).

# 使用github对现有仓库进行修改

## 克隆仓库

首先，克隆某个github仓库。例如，克隆这个仓库：

```bash
git clone https://github.com/Ethylene9160/Contacts.git
```

## 新建分支

点击进入克隆的仓库文件夹`Contaact`，然后重新**在`Contact`文件夹中**打开命令行工具，输入：

```bash
git remote add origin https://github.com/Ethylene9160/Contacts.git
```

然后添加分支：

```bash
git checkout -b your_branch_name
```

其中，`your_branch_name`表示你的分支名。这个命令会创建一个`your_branch_name`的分支，并直接切换至其中。

## 更改文件

直接在Contact文件夹里修改文件。

## 推送

分为三步

添加文件：

```bash
git add .
```

添加注释：

```bash
git commit -m"your comments"
```

推送：

```bash
git push origin your_branch_name
```

其中，`your_branch_name`表示您的分支名。

## 切换分支

切换分支前，可以在该本地仓库的命令行中使用命令

```bash
git branch -a
```

查看远程分支。

* 切换到另一个分支

假设要切换的分支为`another_branch_name`

```bash
git checkout another_branch_name
```

即可切换到另一个分支。

* 切换回上一个分支：

```bash
git checkout -
```

即可切换回上一次使用的分支。

## 拉取分支

在您当前分支中，使用：

```bash
git pull origin other_branch_name
```

可以将`other_branch_name`分支中的内容获取到。

# 强制回滚

首先，进入你希望回滚的分支，并在命令行中输入：

```bash
git log
```

能够获取到多个该分支的创建信息。界面上会出现：

```
commit 一串版本号哈希数值 (HEAD -> branch_name, ...)
Author: xxx<xxx@xx.com>
Data: Set 时间信息
	(comments)
	
...
```

除此以外，也可以在github官网上查看。

将希望回到的目标分支的版本号哈希数值编码记录下来，然后输入：

```bash
git reset --hard 你所记录的版本号哈希数值
```

完成回滚。需要注意的是，该分支该回滚到目标版本时间点后的提交将**不再存在**。
