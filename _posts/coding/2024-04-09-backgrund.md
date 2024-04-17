---
layout: post
title: 배경(Background)명령어 정리
date: 2024-04-09 17:42 +0900
description: 백그라운드 명령어를 정리해봅시다
image: ../assets/img/background.jpg
category: javascript
tags: Background 배경
published: true
sitemap: true
---

# <span style="color:Navy">배경(Background)</span>
배경의 색상, 이미지, 반복 여부, 위치, 고정 여부 등을 각각 기술할 수도 있고, 이 모든 속성을 한 줄로 표기할 수도 있습니다.

# <span style="color:Navy">01 backgrund-color
<details>
<summary>접기/펼치기 버튼</summary>
<div markdown="1">

요소의 배경 색상을 지정하는 속성으로, 다음과 같이 표현합니다.
````
background-color: #원하는 색상코드;
````
|**속성값**|**속성설명**|
|-----|----|
|**색상값**|<span style="color:blue"> 색상명, HEX값, RGB값, HSL값, RGBA값, HSLA값
|**tranparent**|<span style="color:blue"> 투명(기본값)

</div>
</details>

# <span style="color:Navy">02 backgrund-image
<details>
<summary>접기/펼치기 버튼</summary>
<div markdown="2">

요소의 배경에 들어갈 이미지를 지정하는 속성으로, 다음과 같이 표현합니다
````
backgrund-image: url(img/이미지이름.png);
````
용량이 큰 이미지는 속도를 저하시키는 요인이 되므로, 배경에 해상도가 크거나 크기가 큰 이미지는 꼭 필요한 경우가 아니면 사용하지 않도록 합니다.

|**속성값**|**속성설명**|
|:-----:|:---:|
|**url(~)**| <span style="color:blue"> 이미지의 경로와 파일명을 기술함
|**none**| <span style="color:blue"> 배경 이미지 없음(기본값)

- 다음 예제에서는 배경 이미지를 지정하고, 그대로 두면 배경 이미지가 반복되는 것을 볼 수있습니다

<pre><code>
&lt;!DOCTYPE html&gt;
&lt;html lang="ko"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;배경이미지&lt;/title&gt;
    &lt;style type="text/css"&gt;
        p{
            width: 500px;
            padding: 20px;
            <p style="color: black;background-color: yellow; display: inline;">background-color: #원하는 색상;</p>
            <p style="color: black;background-color: yellow; display: inline;">background-image: url(이미지 위치);</p>
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p&gt;
        집 가고 싶다
    &lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;

</code></pre>

</div>
</details>

# <span style="color:Navy">03 background-repeat
<details>
<summary>접기/펼치기 버튼</summary>
<div markdown="3">

배경 이미지를 어떻게 반복시킬지를 지정하는 속성으로, 다음과 같이 표현합니다.
````
background-repeat: no-repeat;
````
|**속성값**|**속성 설명**|
|:---:|:---:|
|**repeat**| <span style="color:blue"> 배경 이미지를 가로 세로 반복하여 배치함(기본값)|
|**no-repeat**| <span style="color:blue"> 배경 이미지를 한 개만 배치함|
|**repeat-x**|<span style="color:blue">  배경 이미지를 가로로만 반복하여 배치함|
|**repeat-y**|<span style="color:blue">  배경 이미지를 세로로만 반복하여 배치함|
|**space**|  <span style="color:blue"> 배경 이미지를 반복하다가 마지막 이미지가 가로로 잘리지 않도록 배치하기 위해 이미지 사이가 벌어짐|
|**round**| <span style="color:blue"> 배경 이미지를 반복하다가 이미지가 세로로 잘리지 않도록 배치하기 위해 이미지가 납작하게 찌그러짐|


다음 예제에서는 배경 이미지를 반복시키지 않도록 속성을 부여하고 있습니다. 배경 이미지가 요소 안의 콘텐츠와
겹치지 않도록 하기 위해서는 안여백 padding 속성과 함께 사용합니다.

<pre><code>
&lt;!DOCTYPE html&gt;
&lt;html lang="ko"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;배경이미지&lt;/title&gt;
    &lt;style type="text/css"&gt;
        p{
            width: 500px;
            padding: 20px;
            background-color: #원하는 색상;
            background-image: url(이미지 위치);
            <p style="color: black;background-color: yellow; display: inline;">background-repeat: no-repeat;</p>
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;p&gt;
        집 가고 싶다
    &lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;

</code></pre>
<span style="color:red">※ padding: 100px; 은 요소의 내부에 위, 아래, 왼쪽, 오른쪽 모두 100px 여백을 주라는 뜻입니다. ※</span>

</div>
</details>

# <span style="color:Navy">04 backgrund-position 
<details>
<summary>접기/펼치기 버튼</summary>
<div markdown="4">

배경 이미지를 원하는 위치로 옮겨주는 속성으로, 다음과 같이 표현합니다.
````
backgrund-position: 50% top;
````
배경 이미지를 반복시키지 않고 한 개만 배치할 경우 기본적으로 요소 안의 좌측 상단에 나타나게 되는데
backgrund-position을 이용하여 가로 위치와 세로 위치를 지정할 수 있습니다. 위 예문은 배경 이미지를 가로로는 가운데, 세로로는 상단에 위치시킨다는 의미를 가지고 있습니다.
|**위치**|**속성설명**|
|:-----:|:---:|
|**가로 위치**|<span style="color:blue"> left, right, center, px값, %값 등 (기본값:left)
|**세로 위치**|<span style="color:blue"> top, bottom, center, px값, %값 등 (기본값:top)

위치 속성을 %로 부여했을 때 한가지 주의할 점이 있는데, %가 가지는 정확한 의미에 주목해야 합니다.

px와 %를 비교해 보는 것이 좋습니다.
````
background-position: 150px 130px;
````
이 예문은 배경 이미지가 요소의 좌측으로부터 150px, 상단으로부터 130px 떨어진다는 뜻입니다.
````
background-position: 50% 30%;
````
이 예문은 **배경 이미지의 가로 50% 지점을 요소의 가로 50% 지점**에 배치하고,</br>
**배경 이미지의 세로 30% 지점을 요소의 30% 지점**에 배치한다는 뜻입니다.</br>
</br>

예를 들어 **background-position:** 100% 100%;라는 문장은 이미지의 가로 세로 끝이 요소의 가로 세로 끝에 붙도록 배치하라는 뜻으로, 즉 **background-position: right bottom**; 과 같은 결과가 됩니다.
</br>
</br>
다음 예제에서는 순서 없는 목록들에 글머리 기호를 붙이기 위해 **background-position** 속성을 부여하고,
요소 바닥에 패턴을 깔기 위해 **background-repeat** 속성을 부여하고 있습니다. 글머리 기호를 배경 이미지로 붙이기 위해 콘텐츠와 겹쳐지지 않도록 자리를 확보해야 하므로 안여백(**padding**)을 주어야 합니다.

<pre><code>
&lt;!DOCTYPE html&gt;
&lt;html lang="ko"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;배경이미지&lt;/title&gt;
    &lt;style type="text/css"&gt;
       ul{
        <p style="color: red;background-color: skyblue; display: inline;">padding-bottom: 30px;</p>
         ① <p style="color: black;background-color: yellow; display: inline;">background-image: url(이미지 위치);</p>
         ② <p style="color: black;background-color: yellow; display: inline;">background-repeat: repeat-x;</p>
         ③ <p style="color: black;background-color: yellow; display: inline;">background-position: bottom;</p>
       }
       li{
         ④ <p style="color: black;background-color: yellow; display: inline;">list-style-type: none;</p>
        <p style="color: red;background-color: skyblue; display: inline;">padding-bottom: 30px;</p>
         ⑤ <p style="color: black;background-color: yellow; display: inline;">background-image: url(이미지 위치);</p>
         ⑥ <p style="color: black;background-color: yellow; display: inline;">background-repeat: repeat-x;</p>
         ⑦ <p style="color: black;background-color: yellow; display: inline;">background-position: 0 50%;</p>
       }
        ⑧ <p style="color: black;background-color: yellow; display: inline;">ul:nth-child(2) li{</p>
            <p style="color: red;background-color: skyblue; display: inline;">padding-bottom: 10px 30px;</p>
           ⑨ <p style="color: black;background-color: yellow; display: inline;">background-image: url(이미지 위치);</p>
       }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;h3&gt;최근 게시물&lt;/h3&gt;
    &lt;ul&gt;
          &lt;li&gt;PC 사양 알아보기&lt;/li&gt;
          &lt;li&gt;미니타워와 미들타워의 차이&lt;/li&gt;
          &lt;li&gt;어깨의 통증과 발목의 통증&lt;/li&gt;
    &lt;/ul&gt;
    &lt;ul&gt;
          &lt;li&gt;PC 사양 알아보기&lt;/li&gt;
          &lt;li&gt;미니타워와 미들타워의 차이&lt;/li&gt;
          &lt;li&gt;어깨의 통증과 발목의 통증&lt;/li&gt;
    &lt;/ul&gt;
&lt;/body&gt;
&lt;/html&gt;

</code></pre>



※ padding-bottom: 30px;은 하단의 배경 자리 확보를 위해 아래 여백을 30px 주라는 뜻입니다.</br>
※ padding: 0 20px;은 좌츽의 배경 자리 확보를 위해 좌우 여백을 각각 20px 주라는 뜻입니다.</br>
※ padding: 10px 30px;은 세로 간격을 벌리기 위해 내부에 상하 여백 10px을, 좌측 배경 자리 확보를 위해 좌우 여백 30px 주라는 뜻입니다.</br>
① ul 요소의 배경 이미지를 (**이미지 이름**)으로 지정하고,</br>
② ul 요소의 배경 이미지를 가로로만 반복하도록 지정하고,</br>
③ ul 요소의 배경 이미지를 바닥에 배치함</br>
④ li에 새로운 글머리 기호를 달기 위해 원래 기본으로 붙어 있는 글머리 기호를 제거함</br>
⑤ li 요소의 배경 이미지를 (**이미지 이름**)으로 지정하고</br>
⑥ li 요소의 배경 이미지를 반복 없이 한 개만 배치하고,</br>
⑦ li 요소의 배경 이미지를 가로로는 왼쪽에, 세로로는 가운데 배치함</br>
⑧ 두 번째 요소였던 ul의 li에만 따로 속성을 부여함</br>
⑨ 두 번째 요소였던 ul의 li에만 배경 이미지를 (**이미지 이름**)으로 지정함

</div>
</details>

# <span style="color:Navy">05 backgrund-attachment
<details>
<summary>접기/펼치기 버튼</summary>
<div markdown="5">

배경 이미지를 요소 내에 고정시킬지 화면에 고정시킬지에 대한 속성으로, 다음과 같이 표현합니다.
````
backgrund-attachment: fixed;
````
|**속성값**|**속성설명**|
|:-----:|:---:|
|**scroll**|<span style="color:blue">  배경 이미지가 요소 바닥에 붙은 것처럼 화면을 스크롤하면 따라감 (기본값)
|**fixed**|<span style="color:blue">  배경 이미지가 화면 바닥에 붙은 것처럼 화면을 스크롤해도 따라가지 않음

다음 예제에서는 화면을 스크롤했을 때 마치 카메라를 이용하여 이미지를 상하 방향으로 촬영하는 듯한 효과를 주기 위해 backgrund-attachment 속성을 부여하고 있습니다.

<pre><code>
&lt;!DOCTYPE html&gt;
&lt;html lang="ko"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;배경이미지&lt;/title&gt;
    &lt;style type="text/css"&gt;
       ul{
          min-height: 200px;
          <p style="color: black;background-color: yellow; display: inline;">background-image: url(이미지 위치);</p>
          <p style="color: black;background-color: yellow; display: inline;">background-position: repeat-x;</p>
          <p style="color: black;background-color: yellow; display: inline;">background-attachment: fixed;</p>
       }
       .btm {
          min-height: 200px;
          background: #595;
       }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
      &lt;p&gt;
          집 가고 싶다
      &lt;/p&gt;
       <p style="color: black;background-color: yellow; display: inline;">&lt;p class="이미지 이름"&gt;&lt;/p&gt;</p>
       &lt;p class="btm"&gt;집 가 고 싶 다.&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;

</code></pre>

화면을 스크롤 해보면 배경 이미지의 사진 자체는 요소들을 따라 올라가지 않고 배경이 보이는 창(영역)만 올라가는 것을 알 수 있습니다.</br>
</br>
지금까지의 배경 관련 속성들을 띄어쓰기 하는 것만으로 한 줄로 기술할 수 있는데,</br>
다음과 같이 **backgorund** 속성으로 기술하면 됩니다.
````
background: #f00 url(이미지이름) no-repeat 50px 100px fixed;
````
이 예문은 배경색은 빨간색, 배경 이미지 (**이미지 이름**), 배경은 반복하여 좌측에서 50px, 위에서 100px 떨어진 곳에 배치하고 화면에 고정한다는 뜻입니다. 또한 **background**: 를 사용하시면서 속성을 생략할 경우 앞에 기술한 대로 각 속성은 기본값을 가지므로 다음 두 문장은 같은 결과를 갖게 됩니다.
````
background: url("이미지 위치");
background: transparent url("이미지 위치") repeat left top scroll;
````
다음은 **backfround**: 의 틀린 예문입니다.
````
background: #fdddd url ("이미지 위치")no-repeat 50px;
````
이 예문에서는 url과 괄호 사이가 떨어져 배경 이미지가 나타나지 않을 것입니다. 또한 no-repeat 앞에 띄어쓰기 하지 않을 경우에도 **IE** 구버전에서 배경 이미지가 나타나지 않을 수 있으므로 주의해야 합니다.
</div>
</details>

# <span style="color:Navy">06 backgrund-size
<details>
<summary>접기/펼치기 버튼</summary>
<div markdown="6">

CSS3에서 배경 이미지의 크기를 변경할 수 있는 속성으로, 다음과 같이 표현합니다.
````
backgrund-size: 120px 90px;
````
|**속성값**|**속성설명**|
|:-----:|:---:|
|**background-size: 80px 60px;**|<span style="color:blue"> ● 배경 이미지의 가로 크기 80px,세로 크기 60px </br> ● 이미지의 원래 비율이 찌그러질 수 있음
|**background-size: 150px;**| <span style="color:blue"> ● 배경 이미지의 가로 크기 150px,세로 크기 150px </br> ● 이미지의 원래 비율이 찌그러질 수 있음
|**background-size: 50% 100%;**| <span style="color:blue"> ● 배경 이미지의 크기를 요소의 크기의 가로 50%, 세로 100% </br> ● 이미지의 원래 비율이 찌그러질 수 있음
|**background-size: auto;**| <span style="color:blue"> ● 배경 이미지의 원래 크기로 배치하고 남는 공간은 비움 </br> ● 이미지의 원래 비율을 유지함
|**background-size: contain;**| <span style="color:blue"> ● 배경 이미지의 잘리지 않도록 배치하고 남는 공간은 비움 </br> ● 이미지의 원래 비율을 유지함
|**background-size: cover;**| <span style="color:blue"> ● 배경 이미지를 빈공간 없이 요소에 꽉 채우고 나머지는 잘림 </br> ● 이미지의 원래 비율을 유지함
</div>
</derails>

|<p style="color: green;">**NOTE**</p>|
|---|
|배경 이미지의 크기를 고정된 px 값으로 지정하는 것은 어려울 게 없으나, 모바일 App을 만들 경우 기기 의 사이즈도 나날이 다양해지는 현실에서 단순하게 px 값으로만 지정할 수가 없습니다. 여타의 이유로 인해 cover 또는 contain도 유용하게 사용되고 있습니다.|

다음 예제에서는 위 속성 값을 비교해 볼 수 있습니다.
<pre><code>
&lt;!DOCTYPE html&gt;
&lt;html lang="ko"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;배경이미지&lt;/title&gt;
    &lt;style type="text/css"&gt;
       .who {
          height: 150px;
          magin-bottom: 10px;
          <p style="color: black;background-color: yellow; display: inline;">background: #677582 url(이미지 위치); no-repeat;</p>
       }
         .who1{① <p style="color: black;background-color: yellow; display: inline;">background-size: 100px 200px;</p> }
         .who2{② <p style="color: black;background-color: yellow; display: inline;">background-size: auto;</p>}
         .who3{③ <p style="color: black;background-color: yellow; display: inline;">background-size: 80% 150%;</p>}
         .who4{④ <p style="color: black;background-color: yellow; display: inline;">background-size: cover;</p>}
         .who5{⑤ <p style="color: black;background-color: yellow; display: inline;">background-size: contain;</p>}
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
      &lt;div class="who <p style="color: black;background-color: yellow; display: inline;">who1</p>"&gt;&lt;/div&gt;
      &lt;div class="who <p style="color: black;background-color: yellow; display: inline;">who2</p>"&gt;&lt;/div&gt;
      &lt;div class="who <p style="color: black;background-color: yellow; display: inline;">who3</p>"&gt;&lt;/div&gt;
      &lt;div class="who <p style="color: black;background-color: yellow; display: inline;">who4</p>"&gt;&lt;/div&gt;
      &lt;div class="who <p style="color: black;background-color: yellow; display: inline;">who5</p>"&gt;&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

① 배경 이미지 크기를 100px 200px로 줄여 나타내고 남는 공간은 비움</br>
② 배경 이미지 크기를 원래 크기대로 나타내고, 남는 공간은 비우고 넘치는 부분은 잘림</br>
③ 배경 이미지 가로 크기는 요소 영역의 80%, 세로 크기는 요소 영역의 150% 크기로  나타내다 보니 이미지가 찌그러지고 남는 공간은 비우고 넘치는 부분은 잘림</br>
④ 배경 이미지는 길쭉한 이미지여서 가로 100% 로 채우고 넘치는 부분은 잘림 (납작한 이미지는 반대)</br>
⑤ 배경 이미지가 조금도 가려지지 않도록 축소하여 나타내고 남는 공간은 비움</br>

- **backgrund-size** 속성은 아래와 같이 background:의 맨 뒤에 '/'로 구분하여 지정할 수 있습니다.
````
background: url(이미지이름) no-repeat center / cover;
````
그러나 구형 브라우저와 구형 모바일 기기에서 작동이 안 될 수 있으니 반드시 확인한 후 사용하고 고객의 크로스크라우징 요청이 명확하지 않다면 그냥 background-size로 사용하기 바랍니다.
</div>
</derails>

# <span style="color:Navy"> 07 background-origin

<details>
<summary>접기/펼치기 버튼</summary>
<div markdown="7">

CSS3 에서 배경 이미지의 시작점을 정하는 속성으로, 다음과 같이 표현합니다
````
background-origin: border-box;
````

|**속성값**|**속성설명**|
|:-----:|:---:|
|**border-box**| 배경 이미지가 테두리의 좌측 상단 모퉁이에서 시작함
|**paadding-box**| 배경 이미지가 안여백의 좌측 상단 모퉁이에서 시작함 (기본값)
|**content-box**| 배경 이미지가 콘텐츠의 좌측 상단부터 시작함

</br>
다음 예제에서는 위 세 영역이 구체적으로 어디인지 보여주고 있습니다.

<pre><code>
&lt;!DOCTYPE html&gt;
&lt;html lang="ko"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;배경이미지의 원점&lt;/title&gt;
    &lt;style type="text/css"&gt;
       .div {
          width: 550px;
          <p style="color: black;background-color: yellow; display: inline;">padding: 25px;</p>
          magin-bottom: 20px;
          <p style="color: black;background-color: yellow; display: inline;">border: 15px double rgba(0,0,0,0,6);</p>
          background: url(이미지 위치) no-repeat;
       }
         .ori1{① <p style="color: black;background-color: yellow; display: inline;">background-origin: border-boxx;</p> }
         .ori2{② <p style="color: black;background-color: yellow; display: inline;">background-origin: padding-box;</p>}
         .ori3{③ <p style="color: black;background-color: yellow; display: inline;">background-origin: content-box;</p>}
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
      &lt;div class="ori1"&gt;It's impossible not only stating good but also keeping it firm!!&lt;/div&gt;
      &lt;div class="ori2"&gt;It's impossible not only stating good but also keeping it firm!!&lt;/div&gt;
      &lt;div class="ori3"&gt;It's impossible not only stating good but also keeping it firm!!&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>
 ① border: 15px double rgba(0,0,0,0,6);는 반투명한 검정색으로 15px 굵기의 테두리를 치라는 의미입니다.</br>
 ② 배경 이미지가 좌측 상단 테두리를 포함한 영역부터 채워짐</br>
 ③ 배경 이미지가 좌측 상단 테두리를 제외한 안쪽부터 채워짐</br>
 ④ 배경 이미지가 좌측 상단 여백을 제외한 안쪽부터 채워짐</br>


</div>
</derails>

# 08<span style="color:Navy"> background-clip

<details>
<summary>접기/펼치기 버튼</summary>
<div markdown="8">

CSS3에서 배경의 영역을 정하는 속성으로, 다음과 같이 표현합니다.
````
background-clip: border-box;
````

|**속성값**|**속성설명**|
|:-----:|:---:|
|**border-box**| 배경이 테두리를 포함한 영역에 배치 (기본값)
|**paadding-box**| 배경이 테두리를 제외한 안쪽 영역에 배치됨
|**content-box**| 배경이 안여백을 제외한 콘텐츠 영역에만 배치됨
</br>
다음 예제에서는 위 세 영역이 구체적으로 어디인지 보여주고 있습니다.
</br>
</br>
<pre><code>
&lt;!DOCTYPE html&gt;
&lt;html lang="ko"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;배경이미지의 영역&lt;/title&gt;
    &lt;style type="text/css"&gt;
       .div {
          width: 550px;
          padding: 25px;
          magin-bottom: 20px;
       >border: 15px double rgba(0,0,0,0,6);
          background: #e5cadd;
       }
         .clip1{① <p style="color: black;background-color: yellow; display: inline;">background-clip: border-boxx;</p> }
         .clip2{② <p style="color: black;background-color: yellow; display: inline;">background-clip: padding-box;</p>}
         .clip3{③ <p style="color: black;background-color: yellow; display: inline;">background-clip: content-box;</p>}
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
      &lt;div class="clip1"&gt;It's impossible not only stating good but also keeping it firm!!&lt;/div&gt;
      &lt;div class="clip2"&gt;It's impossible not only stating good but also keeping it firm!!&lt;/div&gt;
      &lt;div class="clip3"&gt;It's impossible not only stating good but also keeping it firm!!&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

① 배경이 테두리를 포함한 영역에 채워짐</br>
② 배경이 테두리를 제외한 안쪽 영역에 채워짐</br>
③ 배경이 여백을 제외한 콘텐츠 영역에 채워짐</br>


</div>
</derails>


# 09<span style="color:Navy"> Image Sprite

<details>
<summary>접기/펼치기 버튼</summary>
<div markdown="9">

이미지가 많아지면 웹페이지의 로딩 속도도 느려집니다. 웹페이지의 로딩 속도를 줄여주기 위해 배경으로 사용할 여러 이미지들을 하나로 저장하고 **background-position**을 이용하여 잘라 사용하는 것이 **image sprite**입니다.
</br>

만약 세 번째 이미지만 추출하여 사용하려 할 때 **background-position** 은 몇일까요? 많은 사람들이 0 200px; 일거라고 생각하지만 반대입니다.

세로 값 양수는 이미지 판을 아래 방향으로 밀어 내린다는 뜻이고, 음수는 위로 밀어 올린다는 뜻입니다. 이미지를 잘라내기 위한 칼은 그대로 있고 바닥 이미지를 움직이는 격입니다. 따라서 세 번째 아이콘
을 잘라낸다는 것은 이미지를 **위로 200px** 밀어야 한다는 뜻이기 때문에 정답은 **background-position: 0 -200px**;입니다.
</br>
</br>
<pre><code>
&lt;!DOCTYPE html&gt;
&lt;html lang="ko"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;배경이미지의 영역&lt;/title&gt;
    &lt;style type="text/css"&gt;
       li { ① <p style="color: black;background-color: yellow; display: inline;">list-style-type: none;</p>
            margin 5px;
          }

       .lnb li a {
<p style="color: red;background-color: skyblue; display: inline;">display: block;</p>
<p style="color: red;background-color: skyblue; display: inline;">padding-left: 30px;</p>
          text-decoration: none;
          font: 25px Times;
          color #000;
          background: url(이미지 위치) no-repeat;
          ② background-size: 26px 176px;
        }
        ③  <p style="color: black;background-color: yellow; display: inline;">.lnb li:nth-child(1) a {background-position: 0 0;}</p>
        ④  <p style="color: black;background-color: yellow; display: inline;">.lnb li:nth-child(2) a {background-position: 0 -50px;}</p>
        ⑤  <p style="color: black;background-color: yellow; display: inline;">.lnb li:nth-child(3) a {background-position: 0 -100;}</p>
        ⑥  <p style="color: black;background-color: yellow; display: inline;">.lnb li:nth-child(4) a {background-position: 0 -150;}</p>
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
      &lt;ul class="lnb"&gt;
       &lt;li&gt;&lt;a href="#"&gt;Theater&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt;&lt;a href="#"&gt;Secret Garden&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt;&lt;a href="#"&gt;Concert Hall&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt;&lt;a href="#"&gt;Animal Farm&lt;/a&gt;&lt;/li&gt;
      &lt;/ul&gt;
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

① 목록의 고유 글머리 기호를 제거함</br>
② 이미지의 크기를 원래 사이즈 52px X 352px의 1/2로 줄임</br>
③ 첫 번째 메뉴 Theater 앞의 보라색 배경 이미지가 이미지의 좌측 상단에 있으므로 0 0</br>
④ 두 번째 메뉴 Secret Garden 앞의 남색 배경 이미지가 상단으로부터 100px 아래에 있으므로 0 -100px이어야겠지만
이미지 사이즈를 반으로 줄였으므로 이 길이도 반으로 줄어서 0, -50px</br>
⑤ 같은 맥락에서 세 번째 메뉴는 0 -200px이 아닌 0 -100px</br>
⑥ 네 번째 메뉴도 0 -300px이 아닌 0 -150px</br>

</div>
</derails>