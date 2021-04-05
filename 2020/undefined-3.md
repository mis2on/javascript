# 변수의 생명\(블록 스코프\)

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

한번만 쓰이는 것들은 변수로 만들지 말고 그냥 넣자!  
ex\) const w = input\[0\];  
       const i = word\[lastIndex\];

```javascript
const btn = document.querySelector('#button');
// document.querySelector('#아이디')는 그 아이디의 태그를 가져온다.
btn.addEventListener('click', () => {
    const word = document.querySelector('#word').textContent;
    // .은 ~의를 의미
    const input = document.querySelector('#input').value;
    if(word[word.length -1] === input[0]) {
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

