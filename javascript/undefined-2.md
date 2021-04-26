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

변수 값을 변경할 수 있다. 값을 변경하면 이전의 값을 제거된다.

```javascript
let message; 
message = 'Hello!';
message = 'World!'; // 값이 변경되었습니다.
alert(message);
```

변수를 두번 선언하면 에러가 발생한다.

```javascript
let message = 'This';
//let을 반복하면 에러가 발생한다.
let message = 'That';
```

## 변수 명명 규칙

변수명에는 오직 문자와 숫자, 그리고 기호 $와 \_만 들어갈 수 있다.  
첫 글자는 숫자가 될 수 없다.  
여러 단어를 조합해 변수명을 만들 때는 카멜 표기법을 사용.

변수명은 숫자로 시작할 수 없다.  
let 1a;  
하이픈'-'은 변수명에 올 수 없다.  
let my-name; 

예약어는 변수명으로 사용할 수 없다.  
ex\) let, class, return, function

## 상수

변화하지 않는 변수를 선언할때 const를 사용

```javascript
const myBirthday = '30.03.1992';
```

상수는 재할당할 수 없으므로 상수를 변경하려고 하면 에러가 발생한다.  
값이 변경되는 것을 방지하기 위해 const를 사용해 변수를 선언한다.

#### 변수는 간결하고 명확해야 한다. 사람이 읽을 수 있는 이름을 사용해라 

