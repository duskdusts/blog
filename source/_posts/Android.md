title: hexo-theme-melody v1.5 supports iframe & slides
date: 2018-03-06 19:57:52
layout: slides
---

## Slide 1

## A paragraph with some text and a [link](http://hakim.se).



## 工具 termux
## 开始
### 安装依赖
```shell
pkg install -y nodejs-lts
pkg install -y git
pkg install openssh
npm install -g hexo-cli
```
### 创建
```shell
mkdir blog
hexo init blog
cd blog
```
### 再安装依赖
```shell
npm install
npm install hexo-renderer-pug
hexo-renderer-stylus --save
npm install hexo-deployer-git --save
git clone -b master https://github.com/Molunerfinn/hexo-theme-melody themes/melody
```
### 安装完成
## 部署
### ssh
```shell
git config --global user.name "duskdust"
git config --global user.email "czy@live.in"
ssh-keygen -t rsa -C "czy@live.in"
cat ~/.ssh/id_rsa.pub
ssh -T git@e.coding.net
```
### deploy
```shell
hexo clean&&hexo g&&hexo d
```
### 修改
```shell
termux-setup-storage
cp -rv ~/blog ~/storage/shared/blog
```
    坑: repo : 不要用https 用 git 





---
## Slide 2

---

## Slide 3