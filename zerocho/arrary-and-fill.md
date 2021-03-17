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
필.forEach(function(요소, 인덱스) {    //두번째 파라미터,매개변수로 인덱스
    console.log(요소, 인덱스);
});
undefined 0    //요소 인덱스 짝지어 나옴 1부터가 아닌 0부터나온다
undefined 1
undefined 2
undefined 3
undefined 4
undefined 5
undefined 6
undefined 7
undefined 8
undefined 9
undefined 10
undefined 11
undefined 12
undefined 13
undefined 14
undefined 15
undefined 16
undefined 17
undefined 18
undefined 19
undefined 20
undefined 21
undefined 22
undefined 23
undefined 24
undefined 25
undefined 26
undefined 27
undefined 28
undefined 29
undefined 30
undefined 31
undefined 32
undefined 33
undefined 34
undefined 35
undefined 36
undefined 37
undefined 38
undefined 39
undefined 40
undefined 41
undefined 42
undefined 43
undefined 44

//0이 아닌 1부터 나오게 하는 방법
필.forEach(function(요소, 인덱스) {
    console.log(요소, 인덱스 + 1);
});
undefined 1
undefined 2
undefined 3
undefined 4
undefined 5
undefined 6
undefined 7
undefined 8
undefined 9
undefined 10
undefined 11
undefined 12
undefined 13
undefined 14
undefined 15
undefined 16
undefined 17
undefined 18
undefined 19
undefined 20
undefined 21
undefined 22
undefined 23
undefined 24
undefined 25
undefined 26
undefined 27
undefined 28
undefined 29
undefined 30
undefined 31
undefined 32
undefined 33
undefined 34
undefined 35
undefined 36
undefined 37
undefined 38
undefined 39
undefined 40
undefined 41
undefined 42
undefined 43
undefined 44
undefined 45
```

## 자바스크립트로 CSS 조작법

