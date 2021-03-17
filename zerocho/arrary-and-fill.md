# 로또추첨기 Arrary & fill

## 배열을 만드는 방법

보통 배열은 대괄호\[ \] 안에 넣어서 만들었지만  
Array\(숫자\)를 이용해 배열을 만드는 방법도 있다. 하지만 추천하지 않는다.

```javascript
var 후보군 = Array(45);    //45개 들어갈 수 있는 빈공간을 만듬
[undefined, undefined, undefined].forEach(function(요소){
    console.log(요소)
});
```

★empty의 특징  
반복문 불가!

## fill

fill 메서드는 IE에서는 안됨!

```javascript
var 후보군 = Array(45); 
var 필 = 후보군.fill();
console.log(필);

(45) [undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined]

//1부터 45까지 넣는방법
필.forEach(function(요소, 인덱스){    //두번째 파라미터,매개변수로 인덱스
    console.log(요소, 인덱스);
});
undefined 0
undefined 1
undefined 22 undefined 3
VM6200:2 undefined 4
VM6200:2 undefined 5
VM6200:2 undefined 6
VM6200:2 undefined 7
VM6200:2 undefined 8
VM6200:2 undefined 9
VM6200:2 undefined 10
VM6200:2 undefined 11
VM6200:2 undefined 12
VM6200:2 undefined 13
VM6200:2 undefined 14
VM6200:2 undefined 15
VM6200:2 undefined 16
VM6200:2 undefined 17
VM6200:2 undefined 18
VM6200:2 undefined 19
VM6200:2 undefined 20
VM6200:2 undefined 21
VM6200:2 undefined 22
VM6200:2 undefined 23
VM6200:2 undefined 24
VM6200:2 undefined 25
VM6200:2 undefined 26
VM6200:2 undefined 27
VM6200:2 undefined 28
VM6200:2 undefined 29
VM6200:2 undefined 30
VM6200:2 undefined 31
VM6200:2 undefined 32
VM6200:2 undefined 33
VM6200:2 undefined 34
VM6200:2 undefined 35
VM6200:2 undefined 36
VM6200:2 undefined 37
VM6200:2 undefined 38
VM6200:2 undefined 39
VM6200:2 undefined 40
VM6200:2 undefined 41
VM6200:2 undefined 42
VM6200:2 undefined 43
VM6200:2 undefined 44
undefined

```

## 자바스크립트로 CSS 조작법

