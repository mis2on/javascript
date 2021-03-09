# 끝말잇기 화면에 표시

반복되는 동작은 보통 함수로 만든다.

enter기능x, 마우스로 입력버튼을 클릭해야

```javascript
var 바디 = document.body;
var 단어 = document.createElement('div');
단어.textContent = '몽실';
document.body.append(단어);
var 입력창 = document.createElement('input');
document.body.append(입력창);
var 버튼 = document.createElement('button');
버튼.textContent = '입력';
document.body.append(버튼);
var 결과창 = document.createElement('div');
document.body.append(결과창);

버튼.addEventListener('click', function 콜백함수 () {
    if(단어.textContent[단어.textContent.length - 1] === 입력창.value[0]){
        결과창.textContent = '딩동댕';
        입력창.value = '';    //맞으면 input 입력창을 빈 값으로 변경
        입력창.focus();    //input 입력창에 자동 포커스(깜빡임) 
    } else {
        결과창.textContent = '땡';
        입력창.value = '';    //틀려도 input 입력창을 빈 값으로 변경
        입력창.focus(); 
    }
});
```

## enter 기능 추가하기\(form 태그 필요\)

```markup
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <title>끝말잇기</title>
    </head>
    <body>
        <!--<div>몽실</div>-->
        <!--
        <form>
            <input type="text">
            <button>입력</button>
        </form>
        -->
        <!--<div>딩동댕</div>-->
        <script src="끝말잇기.js"></script>
    </body>
</html>
```

```javascript
var 바디 = document.body;
var 단어 = document.createElement('div');
단어.textContent = '몽실';
document.body.append(단어);
var 폼 = document.createElement('form');
document.body.append(폼);
var 입력창 = document.createElement('input');
폼.append(입력창);    //document.body가 아니라 form안에 넣기
var 버튼 = document.createElement('button');
버튼.textContent = '입력';
폼.append(버튼);    //document.body가 아니라 form안에 넣기
var 결과창 = document.createElement('div');
document.body.append(결과창);

버튼.addEventListener('submit', function 콜백함수 () {    //click를 submit로 변경
    if(단어.textContent[단어.textContent.length - 1] === 입력창.value[0]){
        결과창.textContent = '딩동댕';
        입력창.value = '';    //맞으면 input 입력창을 빈 값으로 변경
        입력창.focus();    //input 입력창에 자동 포커스(깜빡임) 
    } else {
        결과창.textContent = '땡';
        입력창.value = '';    //틀려도 input 입력창을 빈 값으로 변경
        입력창.focus(); 
    }
});
```

결과! 페이지가 깜빡이며 새로고침

