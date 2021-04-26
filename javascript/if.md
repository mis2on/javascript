# if와 '?'를 사용한 조건 처리

## 'if'문

if\( \) 문은 괄호 안에 들어가는 조건을 평가해, 그 결과가 참\(true\)이면 코드 블록이 실행된다.

```javascript
let year = prompt('ECMAScript-2015 명세는 몇 년도에 출판되었을까요?', '');
if(year == 2015) alert('정답입니다.');
```

중괄호{ }를 이용해 코드의 가독성 증가

```javascript
let year = prompt('ECMAScript-2015 명세는 몇 년도에 출판되었을까요?', '');
if(year == 2015){
    alert('정답입니다.');
    alert('똑똑하시네요!');    
}
```

## 불린형으로의 변환

숫자0, 빈 문자열 " ", null, undefined, NaN은 불린형으로 변환 시 모두 false가 됩니다.   
이런 값들은 'falsy\(거짓 같은\)' 값이라고 부른다.

이 외의 값은 불린형으로 변환시 true가 되므로 'truthy\(참 같은\)' 값이라고 부른다.

## 'else'절

if문에 else 절을 붙일 수 있다. else 뒤에 이어지는 코드 블록은 조건이 거짓일 때 실행된다.

```javascript
let year = prompt('ECMAScript-2015 명세는 몇 년도에 출판되었을까요?', '');

if(year == 2015) {
    alert('정답입니다!');
} else {
    alert('오답입니다!');    //2015 이외의 값을 입력한 경우
}
```

## 'else if'로 복수 조건 처리하기

```javascript
let year = prompt('ECMAScript-2015 명세는 몇 년도에 출판되었을까요?', '');

if(year < 2015) {
    alert('숫자를 좀 더 올려보세요.');
} else if ( year > 2015) {
    alert('숫자를 좀 더 내려보세요.');
} else {
    alert('정답입니다.');
}
```

## 조건부 연산자 '?'

조건에 따라 다른 값을 변수에 할당해줘야 할 때  
조건부 연산자는 물음표 ? 로 표시한다.

```javascript
let accessAllowed;
let age = prompt('나이를 입력해 주세요.', '');

if(age > 18) {
    accessAllowed = true;
} else {
    accessAllowed = false;
}

alert(accessAllowed);
```

`let result = condition ? value1 : value2;`

평가대상인 condition이 truthy라면 value1이, 그렇지 않으면 value2가 반환

```javascript
let accessAllowed = (age > 18) ? ture : false;
```

## 다중 '?'

물음표 연산자 ? 를 여러 개 연결하면 복수의 조건을 처리할 수 있다.

```javascript
let age = prompt('나이를 입력해주세요.', 18);

let message = (age < 3) ? '아가야 안녕?' :
    (age < 18) ? '안녕!' :
    (age < 100) ? '환영합니다!' :
    '나이가 아주 많으시거나, 나이가 아닌 값을 입력 하셨군요!;

alert(message);
```

```javascript
if(age < 3) {
    message = '아가야 안녕?';
} else if (age < 18) {
    message = '안녕!';
} else if (age > 100) {
    message = '환영합니다!';
} else {
    '나이가 아주 많으시거나, 나이가 아닌 값을 입력 하셨군요!;
}
```

## 부적절한 '?'

물음표? 를 if 대용으로 쓰는 경우가 종종 있다.

```javascript
let company = prompt('자바스크립트는 어떤 회사가 만들었을까요?', '');

(company == 'Netscape') ?
    alert('정답입니다!') : alert('오답입니다!');
```

if문을 사용할 때보다 물음표?를 사용할 때 코드 길이가 짧아진다는 점 때문에 물음표?를 if 대용으로 쓰는게 매력적일 수 있으나 가독성이 떨어진다. 따라서 다음과 같이 작성해야 가독성을 높일 수 있다..

```javascript
let company = prompt('자바스크립트는 어떤 회사가 만들었을까요?', '');

if(company == 'Netscape') {
    alert('정답입니다!');
} else {
    alert('오답입니다!');
}
```

우리 눈은 코드를 읽을 때 수직으로 움직인다.   
따라서 수평으로 길게 늘어진 코드보다는 여러 줄로 나뉘어 작성한 코드블록이 더 읽기 쉽다.

