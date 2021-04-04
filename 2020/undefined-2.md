# 변수 값 수정과 상수

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

## 중복제거 왜 못해요?

const word = document.querySelector\('\#word'\).textContent;  
word는 문자열  
word라는 공간에 input입력값으로 바꾸려는거지  
word 안에 제시어를 input으로 바꾸려는게 아니다  
=은 같다라는 뜻이 아니라 잠시 넣어둔다 대입한다!  
값을 저장하는건 x, 태그 자체를 저장하는건 o

