# 가위바위보\(이미지 스프라이트\)

이미지 스프라이트?  
각각의 이미지파일을 낱개로 준비하는게 아니라 이미지들을 한개의 이미지파일로 묶어 놓음으로  
서버로의 요청을 최소화 해주고 로딩속도를 높여준다.

```javascript
var left = 0;
setInterval(() => {
    document.querySelector('#computer').style.background = 'url(https://en.pimg.jp/023/182/267/1/23182267.jpg)' + left + '0';
}, 100);

setInterval(function() {
    if(left === 0) {
        left = '-142px';
    } else if(left === '-142px') {
        left = '-284px';
    } else {
        left = 0;
    }
    document.querySelector('#computer').style.background = 'url(https://en.pimg.jp/023/182/267/1/23182267.jpg)' + left + '0';
}, 100)
```

## setInterval

일정시간 간격으로 코드를 반복 실행

## setTimeout

지정한 시간간격에 딱 한번만 코드가 실행

```markup
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <title>가위바위보</title>
        <style>
            #computer {
                width: 150px;
                height: 243px;
                background: url('https://en.pimg.jp/023/182/267/1/23182267.jpg') 0 0;
            }
        </style>
    </head>
    <body>
        <div id="computer"></div>
        <div>
            <button id="rock">바위</button>
            <button id="scissor">가위</button>
            <button id="paper">보</button>
        </div>
        <script src="가위바위보.js"></script>
    </body>
</html>
```

```javascript
var left = 0;
setInterval(() => {
    if(left === 0) {
        left = '-142px';
    } else if(left === '-142px') {
        left = '-284px';
    } else {
        left = 0;
    }
    document.querySelector('#computer').style.background = 'url(https://en.pimg.jp/023/182/267/1/23182267.jpg)' + left + '0';
}, 100);
var left = 0;
setInterval(function() {
    if(left === 0) {
        left = '-142px';
    } else if(left === '-142px') {
        left = '-284px';
    } else {
        left = 0;
    }
    document.querySelector('#computer').style.background = 'url(https://en.pimg.jp/023/182/267/1/23182267.jpg)' + left + ' 0';
}, 100);
```

