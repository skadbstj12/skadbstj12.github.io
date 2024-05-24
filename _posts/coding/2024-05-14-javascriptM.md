---
layout: post
title: 자바스크립트 part1 (면접용)
date: 2024-04-14 12:31 +0900
description: 자바스크립트 면접용
image: ../assets/img/css01.png
category: 면접질문
tags: 면접질문
published: true
sitemap: true
---

# 자바스크립트 면접용

자바스크립트(JS)는 현대 웹 개발에서 가장 널리 사용되는 프로그래밍 언어 중 하나입니다. 이 언어의 특징, 장단점, 그리고 몇 가지 주요한 개념들을 살펴보겠습니다.

## 자바스크립트의 장단점
**장점**
> 웹 브라우저에서 실행 가능: 모든 주요 웹 브라우저에서 지원되며, 클라이언트 측 스크립트 언어로 사용됩니다.
> 동적으로 실행되는 언어: 코드를 즉시 실행하여 결과를 확인할 수 있어 빠르게 개발할 수 있습니다.
> 다양한 용도로 사용 가능: 웹 개발뿐만 아니라 서버 개발 (Node.js), 모바일 앱 개발 (React Native 등), 게임 개발 등 다양한 분야에서 사용됩니다.

**단점**
> 브라우저 호환성: 모든 브라우저에서 동일하게 동작하지 않을 수 있습니다.
> 동적 타입: 동적 타입 언어로써 개발자의 실수로 인한 버그 발생 가능성이 높습니다.
> 비동기 처리의 복잡성: 비동기 코드를 작성할 때 콜백 지옥(callback hell)과 같은 문제가 발생할 수 있습니다.
데이터 타입과 형 변환


## 자바스크립트의 기본 데이터 타입

**원시 타입(Primitive types)**
- number: 숫자 (정수 및 부동 소수점 수)
- string: 문자열
- boolean: 불리언 (true 또는 false)
- null: 값이 없음을 나타내는 특별한 값
- undefined: 정의되지 않은 값
- symbol: 고유하고 변경할 수 없는 값
**참조 타입(Reference types)**
- object: 객체 (배열, 함수, 객체 등)

형 변환은 데이터를 다른 타입으로 변환하는 과정을 말합니다. 자바스크립트에서 형 변환은 명시적(explicit) 및 암시적(implicit) 형 변환이 있습니다.

**명시적 형 변환 예시**

````javascript
let num = '10';
num = Number(num); // 문자열 '10'을 숫자 10으로 변환
````
**암시적 형 변환 예시**

````javascript
let result = 10 + '5'; // 숫자 10이 문자열로 변환되어 '105'가 됨
````
**프로토타입과 상속**
자바스크립트는 프로토타입 기반 언어이며, 상속을 프로토타입 체인(Prototype Chain)을 통해 구현합니다. 모든 객체는 부모 역할을 하는 프로토타입 객체를 가지고 있습니다.

````javascript
function Person(name) {
  this.name = name;
}

Person.prototype.greet = function() {
  return 'Hello, ' + this.name;
};

let person1 = new Person('Alice');
console.log(person1.greet()); // 출력: Hello, Alice
````
위의 예제에서 Person 함수 객체의 prototype 프로퍼티를 통해 greet() 메서드를 정의하고, person1 객체는 이를 상속받아 사용합니다.

## var, let, const 차이
> var: 함수 스코프를 가지며, 재선언 가능하고 호이스팅 됩니다.
> let: 블록 스코프를 가지며, 재선언 불가능하고 호이스팅 됩니다.
> const: 블록 스코프를 가지며, 재할당이 불가능하고 선언과 동시에 초기화되어야 합니다.
````javascript
var x = 10;
let y = 20;
const z = 30;
````
위의 예제에서 x는 var로 선언되었기 때문에 함수 스코프를 가지고 재할당 및 재선언이 가능합니다. y는 let으로 선언되었기 때문에 블록 스코프를 가지며 재할당은 가능하지만 재선언은 불가능합니다. z는 const로 선언되었기 때문에 재할당과 재선언이 모두 불가능합니다.