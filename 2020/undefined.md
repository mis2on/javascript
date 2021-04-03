# 변수와 조건문

## ★ .value 입력된 값을 가져온다.

```javascript
document.querySelector('#first').value;
document.querySelector('#secont').value;
```

first라는 아이디를 가진 input의 입력값을 가져온다.  
second라는 아이디를 가진 input의 입력값을 가져온다.

## ★ 가져온 값을 변수에 저장한다.

```javascript
const a = document.querySelector('#first').value
const b = document.querySelector('#second').value
```

input은 value  
span은 textContent

```javascript
if(a) {
    var a = document.querySelector('#first').value
    var b = document.querySelector('#second').value
    
    if(b) {
        a * b
        document.querySelector('#result').textContent = a * b
    } else {
        document.querySelector('#result').textContent =  '두번째 값을 입력해주세요.'
    }
} else {
    document.querySelector('#result').textContent = '첫번째 값을 입력해주세요.'
}
```

## 함수표현시 function\(\){}을 ES6문법으로 \(\) =&gt; {}

```javascript
//버튼을 클릭할 때
document.querySelector('#click').addEventListener('click', function(){
    var a = document.querySelector('#first').value
    var b = document.querySelector('#second').value
    
    if(a) {
        if(b) {
            a * b
            document.querySelector('#result').textContent = a * b
        } else {
            document.querySelector('#result').textContent =  '두번째 값을 입력해주세요.'
        }
    } else {
        document.querySelector('#result').textContent = '첫번째 값을 입력해주세요.'
    }
});

-------------------------ES6문법---------------------------------------------
//버튼을 클릭할 때
document.querySelector('#click').addEventListener('click', () => {
    var a = document.querySelector('#first').value
    var b = document.querySelector('#second').value
    
    if(a) {
        if(b) {
            a * b
            document.querySelector('#result').textContent = a * b
        } else {
            document.querySelector('#result').textContent =  '두번째 값을 입력해주세요.'
        }
    } else {
        document.querySelector('#result').textContent = '첫번째 값을 입력해주세요.'
    }
});

```

코드는 위에서부터 아래로! 왼쪽에서 오른쪽으로 실행된다!

