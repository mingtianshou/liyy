---
title: wagtail手机搭建
---

1 安装termux
2更新一下termux
 $pkg update
3更换termux源
 $termux-change-repo
 $sed -i 's@^\(deb.*stable main\)$@#\1\ndeb https://mirrors.tuna.tsinghua.edu.cn/termux/apt/termux-main stable main@' $PREFIX/etc/apt/sources.list
 $apt update && apt upgrad
4安装Python及换源
 $pkg install python
pip换源
 $pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple    
用 pip config list来查看你换的源


安装wagtail
 23:26:49
1. 安装库：$pip install wagtail
2. 初始化项目：$wagtail start mysite
3. 进入目录：$cd mysite
4. 安装依赖：$pip install -r requirements.txt
5. 初始化数据库：$python manage.py migrate
6. 新建超级管理员：$ 
7. 启动项目：$ 

### 安装库

``` bash
$ hpip install wagtail
```

### 初始化项目

``` bash
$ wagtail start mysite
```

### 进入目录

``` bash
$ cd mysite
```

### 安装依赖
``` bash
$ pip install -r requirements.txt
```

### 初始化

```bash
$ python manage.py migrate
```

### 新建超级管理员
``` bash
$ python manage.py createsuperuser
```

### 启动
```bash
$ python manage.py runserver
```