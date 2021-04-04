# 문자열과 인덱스

`string(문자열)  
number(숫자)  
boolean(T/F)  
object(객체)  
null  
undefined  
symbol`

input 은 .value  
나머지는 .textContent로 값을 가져온다.

```javascript
// input에 자동커서
document.querySelector('#input').focus();
```

```javascript
const btn = document.querySelector('#button');
// document.querySelector('#아이디')는 그 아이디의 태그를 가져온다.
btn.addEventListener('click', () => {
    const word = document.querySelector('#word').textContent;
    // .은 ~의를 의미
    const input = document.querySelector('#input').value;
    const lastIndex = word.length -1;
    const w = input[0];
    const i = word[lastIndex];
    if(w === i) {
        document.querySelector('#word').textContent = input;
        document.querySelector('#error').textContent = '';
        document.querySelector('#input').value = '';
        document.querySelector('#input').focus();
    } else {
        document.querySelector('#error').textContent = '땡';
        document.querySelector('#input').value = '';
        document.querySelector('#input').focus();
    }
});
```



