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
필.forEach(function(요소, 인덱스){    //두번째 매개변수로 인덱스
    console.log(요소, 인덱스);
});
```

## 자바스크립트로 CSS 조작법

