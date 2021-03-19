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



