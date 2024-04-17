---
layout: post
title: 깃헙 셋팅 및 여러가지 기능
date: 2024-04-08 16:32 +0900
description: 깃헙에 필요한 여러가지 설정을 합니다.
image: ../assets/img/Github.jpg
category: javascript
tags: Githup Git 깃헙
published: true
sitemap: true
---

# Github을 편하게 써보자!!

git은 소스 코드 버전 관리 시스템(VCS, Version Control System) 중 하나로, 소프트웨어 개발에서 코드의 변경 이력을 효과적으로 관리할 수 있게 해주는 도구입니다. Git을 사용하면 여러 개발자들이 동시에 작업하고 있는 프로젝트에서 발생하는 코드의 수정, 추가, 삭제 등의 변경 사항을 효율적으로 추적하고 관리할 수 있습니다.

## Github 초기 설정

깃헙은 커밋할 때 마다 사용자 정보를 기록하고, 편집기 설정에 따라 메세지를 작성할 수 있습니다.

## 작업프롬포트에서 Github 버전 확인하기

터미널을 열어서 버전확인 하고, 없으면 인터넷에 Git검색하고 다운로드 해야됩니다.

![51512](https://github.com/skadbstj12/skadbstj12.github.io/assets/163810643/10082b6f-e618-4bc0-8693-08cfbc8713af)

다운로드를 완료했다면 한번 버전을 확인해 봅시다.

````bash
git --version
git version 2.44.0.windows.1
````

## 터미널에서 Git에 연결하는 방법
````bash
cd document

cd Github
````

name과 email이 자신의 것이 맞는지 확인합니다.

````bash
git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.email=163810643+skadbstj12@users.noreply.github.com
user.name=남윤서
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
````


만약에 내것이 아니라면 이름을 변경해야 합니다.
````bash
Git config --global user.name "사용자명"
Git config --global user.email "사용자 이메일"
````

## 깃 상태 확인하기

````bash
git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
  (commit or discard the untracked or modified content in submodules)
        modified:   class2024 (modified content)
        modified:   skadbstj12.github.io (modified content)

no changes added to commit (use "git add" and/or "git commit -a")
````

## git init 명령은 Git 저장소를 초기화하는 데 사용됩니다.

````bash
git init
Reinitialized existing Git repository in C:/Users/line/Documents/GitHub/.git/
````

## git branch -m main 이 명령은 현재 Git 저장소에서 사용할 기본 브랜치의 이름을 변경합니다.

만약 현재 작업 중인 브랜치가 master라면, master 브랜치가 main으로 이름이 변경됩니다.
만약 이미 다른 브랜치 이름이 main인 경우에는 아무런 변화가 없을 수 있습니다.
````bash
git branch -m main
Your branch has been renamed from 'main' to 'master'
또는
Switched to branch 'master'
````

## git add . 깃에 저장하는 명령어

git add.을 입력하여 commit할 파일을 업로드 시킨 후 git status로 확인

````bash

C:\Users\line\Documents\GitHub\class2024>git add .

C:\Users\line\Documents\GitHub\class2024>git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   effect/index.html
        modified:   json/gineungsaJC2024_01.json

````


## git commit -m "first commit"

깃 커밋명령으로 -m은 메세지이다. ""안에 자기가 지정하고 싶은 히스토리 name을 입력하면 된다.

````bash
git commit -m "first commit"
[main ed1d509] 2024.04.08
 2 files changed, 272 insertions(+), 2 deletions(-)
 create mode 100644 effect/index.html
 ````

## git push -u origin main 입력해서 Gihub에 commit 파일 저장 명령어

프로젝트를 git으로 push하는 최종 명령이다. main위치에 본인이 푸쉬할 장소(브런치)를 입력하면 된다.
````bash
git push -u origin main
info: please complete authentication in your browser...
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 12 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 2.76 KiB | 2.76 MiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/skadbstj12/class2024.git
   d72c9bd..ed1d509  main -> main
branch 'main' set up to track 'origin/main'.
````