---
layout: post
title: CSS background 대해서 알아봅니다.
date: 2024-04-17 12:31 +0900
description: 
image: ../assets/img/background.jpg
category: Coding
tags: background
published: true
sitemap: true
---


## background
CSS background 단축 속성은 색상, 이미지, 원점, 크기, 반복 등 여러 배경 스타일을 한 번에 지정합니다.

### 구성 속성
background는 단축 속성으로서 다음의 하위 속성을 포함합니다.   
````css
background-attachment
background-clip
background-color
background-image
background-origin
background-position
background-repeat
background-size
````

### 구문
````css
/* <background-color> 사용 */
background: green;

/* <bg-image>와 <repeat-style> 사용 */
background: url("test.jpg") repeat-y;

/* <box>와 <background-color> 사용 */
background: border-box red;

/* 단일 이미지, 중앙 배치 및 크기 조절 */
background: no-repeat center/80% url("../img/image.png");
````