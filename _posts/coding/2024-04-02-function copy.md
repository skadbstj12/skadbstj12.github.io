---
layout: post
title: 오늘 한 일 2024-04-02
date: 2024-04-02 15:32 +0900
description: 오늘 한 일 적어두는 곳
image: ../assets/img/function.jpg
category: 일상
tags: 인생이란..
published: true
sitemap: true
---

# 함수의 기초
함수(function)란?
함수(function)란 하나의 특별한 목적의 작업을 수행하도록 설계된 독립적인 블록을 의미합니다.

이러한 함수는 필요할 때마다 호출하여 해당 작업을 반복해서 수행할 수 있습니다.
````javascript
function addNum(x, y) {

    return x + y;

}
document.write(addNum(2, 3));
````

## 자바스크립트 함수
자바스크립트에서는 함수도 하나의 타입(datatype)입니다.

 

따라서 함수를 변수에 대입하거나, 함수에 프로퍼티를 지정하는 것도 가능합니다.

또한, 자바스크립트 함수는 다른 함수 내에 중첩되어 정의될 수도 있습니다.

# 함수의 정의

자바스크립트에서 함수의 정의는 function 키워드로 시작되며, 다음과 같은 구성요소를 가집니다.
</br>
</br>
1. 함수의 이름
2. 괄호 안에 쉼표(,)로 구분되는 함수의 매개변수(parameter)
3. 중괄호({})로 둘러진 자바스크립트 실행문
</br>
자바스크립트에서 함수를 정의하는 문법은 다음과 같습니다.
````
function 함수이름(매개변수1, 매개변수2,...) {

    함수가 호출되었을 때 실행하고자 하는 실행문;

}
````
함수 이름(function name)은 함수를 구분하는 식별자(identifier)입니다.

매개변수(parameter)란 함수를 호출할 때 인수(argument)로 전달된 값을 함수 내부에서 사용할 수 있게 해주는 변수입니다.
````
// addNum라는 이름의 함수를 정의함.

function addNum(x, y) {    // x, y는 이 함수의 매개변수임.

    document.write(x + y);

}

addNum(2, 3);              // addNum() 함수에 인수로 2와 3을 전달하여 호출함.
````