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

