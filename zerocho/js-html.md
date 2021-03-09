# js로 HTML 태그 만들기

document 객체의 메서드를 사용해 HTML을 만들 수 있다.

```javascript
var 바디 = document.body;
var 단어 = document.createElement('div');
단어.textContent = '몽실';
////컴퓨터의 메모리 속에 기억만 하고 있
```

![](../.gitbook/assets/image%20%2821%29.png)

```javascript
var 바디 = document.body;
var 단어 = document.createElement('div');
단어.textContent = '몽실';    
document.body.append();    //기억하고 있는 내용을 화면에 표시하기 위해 추가
```

![](../.gitbook/assets/image%20%2822%29.png)

