# 자료형

자바스크립트에는 8가지 자료형이 있다.  
자바스크립트 변수는 자료형에 관계없이 모든 데이터일 수 있다. 따라서 변수는 어떤 순간에 문자열일 수 있고 다른 순간엔 숫자가 될 수도 있다. 이처럼 자료의 타입은 있지만 변수에 저장되는 값의 타입은 언제든지 바꿀 수 있는 동적 타입 언어이다.

```javascript
let message = 'Hello!';
message = 123456;
```

## 숫자형

숫자형은 정수 및 부동소수점 숫자를 나타냄.  
숫자형과 관련된 연산은 곱셈 \*, 나눗셈 /, 덧셈 +, 뺄셈 - 등이 대표적이다.  
일반적인 숫자외에 Infinity, -Infinity, NaN 이 포함된다.

NaN은 계산 중에 에러가 발생했다는 것을 나타내주는 값이다. 부정확하거나 정의되지 않은 수학 연산을 사용하면 이와 같은 에러가 발생한다.

```javascript
alert("숫자가 아님"/ 2);
//NaN 문자열을 숫자로 나누면 오류가 발생한다.
```

## BigInt

길이 제약 없이 정수를 나타낼 수 있다. BigInt형은 정수 리터럴 끝에 n을 붙이면 만들 수 있다.

## 문자형

문자열은 따옴표로 묶는다.  
· 작은따옴표\(' '\)  
· 큰따옴표\(" "\)  
· 역 따옴표 백틱\(\` \`\)

```javascript
let str = "Hello";
let str2 = 'Single quotes are ok too';
let phrase = `can embed another $(str)`;
```

## 불린형

불린형\(논리타입\)은 긍정을 나타내는 true와 부정을 의미하는 false 두가지 값 밖에 없다.

## null 값

null 값은 오로지 null 값만 포함하는 별도의 자료형을 만든다.  
존재하지 않는 값, 비어 있는 값, 알 수 없는 값을 나타내는데 사용

```javascript
let age = null;
//나이(age)를 알 수 없거나 그 값이 비어있음을 보여준다.
```

## undefined 값

null 값처럼 자신만의 자료형을 형성한다. 값이 할당되지 않은 상태를 나타낼 때 사용한다.  
변수는 선언했지만 값을 할당하지 않았다면 해당 변수에 undefined가 자동으로 할당된다. 

개발자가 변수에 undefined를 명시적으로 할당하는 것도 가능하나  
변수가 비어있거나, 알 수 없는 상태라는 걸 나타내려면 null을 사용하자!  
undefined는 값이 할당되지 않은 변수의 초기값을 위해 예약어로 남겨두자

## 객체와 심볼

객체형은 특수한 자료형이다.

## typeof 연산자

typeof 연산자는 인수의 자료형을 반환한다. 자료형을 빠르게 알아내고자 할 때 유용

```javascript
typeof undefined //"undefined"
typeof 0 //"number"
typeof 10n //"binint"
typeof true //"boolean"
typeof "foo" //"string"
typeof Symbol("id") //"symbol"
typeof Math //"object"
//Math는 수학연산을 제공하는 내장객체

typeof null //"object"
/* 하위 호환성을 유지하기 위해 오류를 수정하지 않고 남겨둠
null은 언어상의 오류이다. null이 객체가 아니다.*/

typeof alert //"function"
//피연산자가 함수면 function을 반환한다.
```

