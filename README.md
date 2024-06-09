# 4.1

![手写笔记1.1](C://Users//Honey//Desktop//sxbj1_1.jpg "悬停标题")

![手写笔记1.2](C://Users//Honey//Desktop//sxbj1_2.jpg "悬停标题")

---
---
# 4.2
## 设备认证
### 1.如何让网站的账户与设备绑定，后续完成代码的管理，上传下载
	
	git init //创建本地仓库 `后续对仓库的操作，都要在仓库位置（master）`

	git config --list //查看git的配置文件
	
	git config --global user.email ”邮箱“

	git config --global user.name ”用户名“

	ssh-keygen -t rsa -C ”注册邮箱“ //创建本地密文

去对应的目录查找密文文件

	rsa.pub 复制密文，粘贴 settings->SSH`（远程访问）` key and GPG->new ssh key->粘贴

	ssh -T git@github.com//测试关联是否成功

### 2.为仓库起别名，定位目标仓库，后续上传

	git remote add origin ”ssh地址" //为ssh仓库地址创建别名为origin

	git remote remove origin //删除origin别名

	git remote add origin “ssh地址” //为ssh仓库地址创建别名为origin

## 本地设备与云端仓库的交互逻辑

![手写笔记1.3](C://Users//Honey//Desktop//sxbj1_3.jpg "悬停标题")

git add //添加内容

git rm //删除本地文件并删除仓库数据

git restore //恢复被删除（仓库存在）

## 代码更新的依赖关系被破坏

	本地内容要比云端新，完成更新替换，但是如果直接修改云端内容，导致，本地内容无法再次提交

先拉取git pull 云端内容 与本地内容合并或操作，而后再次推即可

	git pull --rebase origin master

	git rebase --skip “忽略本地内容 保留云端内容”

	git rebase --abort “忽略本地内容 保留云端内容”

	git rebase --continue “忽略本地内容 保留云端内容”

## 下载开源代码

	git clone “https仓库地址” //下载开源项目code资源

## 分支Branch

关于分支的相关命令，创建分支，选择分支，合并分支等等

## Markdown 语言

	github可以编写readme，文本修饰语言

---
---
# 4.3

Markdown，文本修饰语言，用特殊符号修饰正文效果<br>

## 标题修饰符\#

# 标题修饰符（一级标题）
## （二级标题）
### （三级标题）
#### （四级标题）
##### （五级标题）


## 正文内容

   输入正文内容，但是如果需要换行，用\<br\> 标签

## 修饰正文

  *一段测试文本*

  **一段测试文本**

  ***一段测试文本***

  ~~一段测试文本~~

  这是一段测试文本，将`关键字`重点显示

## 分割线

  用\-\-\- 表示分割线

---

## 引用效用\>表示
> 你自己就是一座金矿，关键在于如何挖掘和利用自己
>> 苏格拉底
>>> 三级引用
>>>> 四级引用

## 列表修饰符
### 无序列表 \*
* 二次元游戏
  * 原神
    *神里绫华
* 大逃杀类
  * PUBG
  * APEX

## 有序列表 1.
1. 物理学
   1. 粒子物理
   2. 原子核物理
   3. 凝聚态物理
2. 计算机科学
   1. 分布式架构
   2. 云计算
### 混合列表
1. 测试一级
   * 测试二级
   2. 测试三级

### 表格
名称|技能|排行
--|:--:|--:|
蝙蝠侠|有钱|32
海王|游泳|16
闪电侠|跑|18

### 代码片段

```c
	#include<stdio.h>
	int main(void)
	{
		printf("test code\n");
		return 0;
	}
```

```cpp
	#include<iostream>
```
```python
	import<os>
```
```bash
	echo "测试"
	pwd
	ps aux
	ls -l
```

### 超链接技术

[Github](https://www.github.com "点击访问")

### 插入图片

![壁纸截图](C://Users//Honey//Desktop//1.png "悬停标题")
