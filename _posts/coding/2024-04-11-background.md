---
layout: post
title: CSS background 주요 속성 정리
date: 2024-04-11 12:31 +0900
description: 
image: ../assets/img/background.jpg
category: Coding
tags: background
published: true
sitemap: true
---


# background-color
CSS background 단축 속성은 색상, 이미지, 원점, 크기, 반복 등 여러 배경 스타일을 한 번에 지정합니다.

````css
background-color: pink;
````

기본값은 transparent, 투명색이며 색상명이나 색상 코드를 사용할 수 있습니다.

**background-color**는 CSS에서 요소의 배경색을 지정하는 속성이야. 그냥 요소의 배경을 어떤 색으로 표시할 건지 정할 수 있어. 이 색은 키워드, HEX 코드, RGB 값 등으로 지정할 수 있어. 요소의 시각적인 모습을 바꿀 때 자주 사용됩니다.

## background-image

두 번째로 살펴볼 속성은 베경 이미지를 지정할 때 사용하는 background-image입니다.
````css
background-image: url("");
````
기본값은 none, 없음이며 이미지의 위치를 상대 경로 또는 절대 경로를 통해서 나타낼 수 있습니다.
속성값을 명시할 때는 url() 함수를 사용하며, 경로에 공백나올 것을 대비하여 쌍따옴표로 묶어주어야 합니다.

## background-repeat

**background-repeat** 속성은 배경 이미지가 주어진 영역에 꽉 차지 않는 경우 이미지를 반복할 방식을 결정합니다.

기본값은 repeat인데 배경 이미지를 가로와 세로 모든 방향으로 반복을 해줍니다. 
repeat-x는 가로 방향으로만 repeat-y는 세로 방향으로만 배경 이미지를 반복합니다. 
no-repeat는 반복을 원하지 않을 때 사용합니다.

````css
    background-repeat: repeat;
    background-repeat: repeat-x;
    background-repeat: repeat-y;
    background-repeat: no-repeat;
````
- repeat: 배경 이미지를 수평과 수직으로 반복하여 채움.
- repeat-x: 배경 이미지를 수평으로만 반복하여 채움.
- repeat-y: 배경 이미지를 수직으로만 반복하여 채움.
- no-repeat: 배경 이미지를 반복하지 않고 한 번만 표시함.

## background-position
**background-position** 속성은 배경 이미지가 주어진 영역에서 어디에 위치할지를 결정합니다.

이 속성은 background-repeat 속성을 대부분 no-repeat로 설정해놓고 사용하는 합니다. 왜냐하면 배경 이미지가 반복된다면 위치를 지정하는 게 의미가 없어지기 때문입니다.
기본값은 배경 이미지를 좌측 상단에 위치시켜 주는 0% 0%이며 절대/상대 단위를 사용하여 좌측 상단으로 부터 얼마나 떨어져야하는지를 지정할 수 있습니다.
보통 top, bottom, left, right, center와 같은 방향 키워드가 많이 사용됩니다.
````css
    background-position: 0% 0%;
    background-position: top;
    background-position: bottom;
    background-position: left;
    background-position: right;
    background-position: center;
````

> 한줄 설명
- 0% 0% 또는 top left: 배경 이미지를 요소의 왼쪽 상단에 위치시킴.
- top: 배경 이미지를 요소의 상단에 위치시킴.
- bottom: 배경 이미지를 요소의 하단에 위치시킴.
- left: 배경 이미지를 요소의 왼쪽에 위치시킴.
- right: 배경 이미지를 요소의 오른쪽에 위치시킴.
- center: 배경 이미지를 요소의 가운데에 위치시킴.

## background-size
background-size 속성은 배경 이미지의 크기를 결정합니다.
기본값은 auto인데 배경 이미지의 실제 크기를 사용합니다. 절대/상대 단위를 사용해서 특정값을 지정해줄 수 있으며, 주어진 영역에 따라 이미지의 크기를 자동으로 조절해주는 키워드도 있습니다.
cover 키워드는 배경 이미지가 짤리더라도 주어진 영역을 완전히 덮을 수 있도록 이미지를 크기를 맞춰줍니다. contain 키워드는 빈 공간이 생기더라도 배경 이미지가 주어진 영역에 안에 모두 들어올 수 있도록 이미지의 크기를 맞줘줍니다.
````css
    background-size: auto;
    background-size: 200px 50px;
    background-size: cover;
    background-size: contain;
````
 이 속성 값으로 cover를 사용할 때는 background-position 속성을 center로 설정하는 경우가 많은데요. 그러지 않으면 이미지의 중앙이 좌측상단으로 치우쳐져서 어색해보일 수 있기 때문입니다.
````css
  background-position: center;
  background-size: cover;
````

- auto: 배경 이미지를 원본 크기로 표시함.
- cover: 배경 이미지를 요소의 전체 영역에 맞추어 크기를 조절하여 표시함. 가로 또는 세로 중 한쪽이 요소의 크기와 맞지 않을 경우, 이미지가 잘릴 수 있음.
- contain: 배경 이미지를 요소의 영역 안에 최대한 맞추어 크기를 조절하여 표시함. 이미지가 요소보다 크거나 작을 때는 비율을 유지하면서 크기를 조절함.

## background-attachment
**background-attachment** 속성은 스크롤 시 배경 이미지가 주어진 영역과 함께 따라갈지 그대로 있을지를 결정합니다.

scroll 키워드를 사용하면 배경 이미지가 주어진 영역과 함께 스크롤되고, fixed 키워드를 사용하면 배경 이미지가 주어진 영역이 스크롤되더라도 고정됩니다.
````css
    background-attachment: scroll;
    background-attachment: fixed;
````
- scroll: 배경 이미지가 요소와 함께 스크롤됨.
- fixed: 배경 이미지가 뷰포트에 고정되어 있어 요소를 스크롤해도 배경 이미지가 움직이지 않음.

## background
마지막으로 살펴볼 속성은 지금까지 살펴본 모든 속성을 아우를 수 있는 background 단축(shortcut) 속성입니다. 
이 속성을 활용하면 배경 스타일을 위해서 작성해야하는 CSS 코드를 줄일 수 있는데요. 
아래와 같이 background 속성에 여러 가지 값을 같이 쓰더라도 대부분의 경우 잘 작동을 하기 때문입니다.
예시를 보여드리겠습니다.
````css
    background: green;
````
````css
     background: url("test.jpg") repeat-y;
````
````css
    background: no-repeat center/80% url("../img/image.png");
````
