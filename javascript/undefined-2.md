# 변수와 상수

## 변수\(variable\)

데이터를 저장할 때 쓰이는 '이름이 붙은 저장소'  
let 키워드를 사용해 변수를 생성한다.

```javascript
let message;
//'message'라는 이름을 가진 변수를 생성(선언)

let message;
message = 'Hello!';
//message변수에 'Hello!' 문자를 저장

let message;
message = 'Hello!';
alert(message);    //변수에 저장된 값을 보여준다.

let message = 'Hello!'; //한 줄로 작성
alert(message);
```

동시에 여러개의 변수를 선언할 수 있다.

```javascript
let user = 'Miseon', age = 26, message = 'Hello!';
//여러개의 변수를 선언할 때 한 줄에 작성시 가독성이 떨어진다. 다음과 같은 방법을 추천

let user = 'Miseon';
let age = 26;
let message = 'Hello!';
//각각 키워드

let user = 'Miseon',
    age = 26;
    message = 'Hello!';
//한개의 키워드로 변수선
```

var 도 변수를 선언하는 키워드가 맞지만 오래된 방식이다.

## 변수 명명 규칙



## 상수



