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
const a = document.querySelector('#first').value;
const b = document.querySelector('#second').value;
```

input은 value  
span은 textContent

```javascript
if(a) {
    const a = document.querySelector('#first').value;
    const b = document.querySelector('#second').value;
    
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
    const a = document.querySelector('#first').value;
    const b = document.querySelector('#second').value;
      
    if(a) {
        if(b) {
            const c = a * b
            const r = document.querySelector('#result');
            r.textContent = c
        } else {
            r.textContent = '두번째 값을 입력해주세요.'
        }
    } else {
        r.textContent = '첫번째 값을 입력해주세요.'
    }
});

-------------------------ES6문법---------------------------------------------
//버튼을 클릭할 때
document.querySelector('#click').addEventListener('click', () => {
    const a = document.querySelector('#first').value;
    const b = document.querySelector('#second').value;
      
    if(a) {
        if(b) {
            const c = a * b
            const r = document.querySelector('#result');
            r.textContent = c
        } else {
            r.textContent = '두번째 값을 입력해주세요.'
        }
    } else {
        r.textContent = '첫번째 값을 입력해주세요.'
    }
});

```

코드는 위에서부터 아래로! 왼쪽에서 오른쪽으로 실행된다! 항상X  
= 수학에서는 같다라는 뜻이지만 프로그래밍에서는 =은 대입,저장의 뜻

```javascript
const a = document.querySelector('#first').value
변수a를 만들고 값을 가지고와서 저장한다
```

