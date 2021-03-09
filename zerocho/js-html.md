# js로 HTML 태그 만들기

document 객체의 메서드를 사용해 HTML을 만들 수 있다.

```javascript
var 바디 = document.body;
var 단어 = document.createElement('div');
단어.textContent = '몽실';
////컴퓨터의 메모리 속에 기억만 하고 있다
```

![](../.gitbook/assets/image%20%2822%29.png)

```javascript
var 바디 = document.body;
var 단어 = document.createElement('div');
단어.textContent = '몽실';    
document.body.append();    //기억하고 있는 내용을 화면에 표시하기 위해 추가
```

![](../.gitbook/assets/image%20%2823%29.png)

```javascript
var 바디 = document.body;
var 단어 = document.createElement('div');
단어.textContent = '몽실';
document.body.append(단어);
var 입력창 = document.createElement('input');
document.body.append(입력창);
var 버튼 = document.createElement('button');
버튼.textContent = '등록';
document.body.append(버튼);
var 결과창 = document.createElement('div');
document.body.append();
```

결과

```markup
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <title>끝말잇기</title>
    </head>
    <body>
        <!--<div>몽실</div>-->
        <!--<input type="text">-->
        <!--<button>등록</button>-->
        <!--<div>딩동댕</div>-->
        <script src="끝말잇기.js"></script>
    </body>
</html>
```

이처럼 자바스크립트로 html을 만들 수 있지만 효율적이지 못함 

