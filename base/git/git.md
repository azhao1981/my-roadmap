# GIT
<!-- MarkdownTOC autolink="true" -->

- [基础用法](#%E5%9F%BA%E7%A1%80%E7%94%A8%E6%B3%95)
    - [Getting Start](#getting-start)
- [git flight-rules](#git-flight-rules)
- [github-profile-summary](#github-profile-summary)
- [解决冲突工具](#%E8%A7%A3%E5%86%B3%E5%86%B2%E7%AA%81%E5%B7%A5%E5%85%B7)
- [revert 多个commit](#revert-%E5%A4%9A%E4%B8%AAcommit)
- [bare 建库](#bare-%E5%BB%BA%E5%BA%93)
- [cannot-update-paths](#cannot-update-paths)
- [error: pathspec 'add_hz_p2_production' did not match any file\(s\) known to git.](#error-pathspec-add_hz_p2_production-did-not-match-any-files-known-to-git)
- [git review](#git-review)
- [git remote update](#git-remote-update)
- [git 管理](#git-%E7%AE%A1%E7%90%86)
- [git config](#git-config)
- [忽略已经提交的文件](#%E5%BF%BD%E7%95%A5%E5%B7%B2%E7%BB%8F%E6%8F%90%E4%BA%A4%E7%9A%84%E6%96%87%E4%BB%B6)
- [删除远程分支](#%E5%88%A0%E9%99%A4%E8%BF%9C%E7%A8%8B%E5%88%86%E6%94%AF)
- [git tool](#git-tool)
- [checkout tag](#checkout-tag)
- [全局忽略](#%E5%85%A8%E5%B1%80%E5%BF%BD%E7%95%A5)
- [引用](#%E5%BC%95%E7%94%A8)
- [删除](#%E5%88%A0%E9%99%A4)
- [取得commit hash](#%E5%8F%96%E5%BE%97commit-hash)
- [找一个父结点](#%E6%89%BE%E4%B8%80%E4%B8%AA%E7%88%B6%E7%BB%93%E7%82%B9)

<!-- /MarkdownTOC -->

## 基础用法

### Getting Start
+ 安装
`brew install git`
`apt install git`

+ 设置
+ 初始化项目 使proj目录下会产生一个 .git 目录

```bash
cd proj
git init .
git add .
git commit -a -m "xxx"
```

```bash
git show

# 合并上次提交
git commit --amend
git commit --amend -m 'xxxxxxx'

# I want to remove a file from a commit
git checkout HEAD^ myfile
git add -A
git commit --amend

# 删除最后一个提交
git reset HEAD^ --hard
git push -f [remote] [branch]
git reset --soft HEAD@{1}  # 没有提交

#取消已经暂存的文件。即，撤销先前"git add"的操作
git reset HEAD <file>...

# git reset --hard 错了
git reflog     # 显示 HEAD@{N}
git reset --hard SHA1234

# 缓存当前修改
git stash
git stash list
git stash apply
```

## git flight-rules

[git飞行守则](https://github.com/k88hudson/git-flight-rules)

[git飞行守则中文版](https://github.com/k88hudson/git-flight-rules/blob/master/README_zh-CN.md)

## github-profile-summary

个人GITHUB的介绍主页

https://github.com/tipsy/github-profile-summary

## 解决冲突工具

https://github.com/mkchoi212/fac

## revert 多个commit

https://codeday.me/bug/20170417/2196.html

$ git revert --no-commit D
$ git revert --no-commit C
$ git revert --no-commit B
$ git commit -m 'the commit message'

or
$ git checkout -f A -- .
$ git commit -a

## bare 建库

git init --bare udesk_chat.git
git init --bare udesk_ichat.git
git init --bare udesk_vistor.go.git
git init --bare udesk_sentry.git

git remote set-url origin  ud-ichat:/srv/git/udesk_ichat.git
git remote set-url origin  udhz-vistor1:/srv/git/udesk_vistor.go.git
git remote set-url udesk  udhz-sentry:/srv/git/udesk_sentry.git

git clone /srv/git/udesk_sentry.git

## cannot-update-paths

<http://stackoverflow.com/questions/22984262/cannot-update-paths-and-switch-to-branch-at-the-same-time>

## error: pathspec 'add_hz_p2_production' did not match any file(s) known to git.

原因: remote 分支里有多个分支是一样的
解决: 手动指定远程库

```bash
git checkout origin/add_hz_p2_production -b add_hz_p2_production
```

## git review

* 建立  review 分支 (本地) `git checkout origin/xxx -b review/xxx`
* 需要进行review的commit
* 使用 fdi 打开
* git rev-list --boundary feature_IM-2031_msg_drive_assign...develop | grep "^-" | cut -c2-
  [引用](http://stackoverflow.com/questions/1527234/finding-a-branch-point-with-git)
*

## git remote update

git remote update
git checkout -b Feature3 origin/Feature3

## git 管理

sublime text:

https://github.com/kemayo/sublime-text-git/wiki

## git config

  http://stackoverflow.com/questions/23918062/simple-vs-current-push-default-in-git-for-decentralized-workflow
  push
    default = simple / current / matching

  如果用matching,会出现把所有的本地与origin名字相同的都上推,如果一担用了git push -f 会强推覆盖,造成不想要的结果
π
  最好用 current

## 忽略已经提交的文件

https://segmentfault.com/q/1010000000430426

git rm --cached logs/xx.log，然后更新 .gitignore
commit

## 删除远程分支

```shell
  git push origin :serverfix
  git push origin :Develop

  git -r -d 遠端branch 刪除一個 tracking 的遠端 branch，例如git branch -r -d wycats/master
```

## git tool

https://github.com/paulirish/git-recent 显示本地分支最后的修改

https://github.com/so-fancy/diff-so-fancy/

https://hub.github.com/ github 工具

## checkout tag

git checkout -b tag_name tag_name
git checkout -b v3.2.1 v3.2.1

git config --global https.proxy 'socks5://127.0.0.1:1080'

## 全局忽略

git config --global core.excludesfile ~/.gitignore_global

## 引用

[Git 情境劇](http://gogojimmy.net/2012/02/29/git-scenario/)

## 删除

git clean -f -d
git clean -f -X

## 取得commit hash

git show -s --format=%h
git show -s --format=%H

git rev-parse HEAD

git rev-parse --verify HEAD
git for-each-ref
git show-ref

## 找一个父结点

https://stackoverflow.com/questions/1527234/finding-a-branch-point-with-git

git rev-list --boundary branch-a...master | grep "^-" | cut -c2-
[alias]
    diverges = !sh -c 'git rev-list --boundary $1...$2 | grep "^-" | cut -c2-'
$ git diverges branch-a master


FROM=$1

function parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e "s/* \(.*\)/\1/"
}

echo "git rev-list --boundary $(parse_git_branch)...$FROM"

function git_from_commit() {
    git rev-list --boundary $(parse_git_branch)...$FROM | grep "^-" | cut -c2-
}

git log $(git_from_commit)


