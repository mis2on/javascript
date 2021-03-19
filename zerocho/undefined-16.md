# 딕셔너리 자료구조

가위, 바위, 보 버튼을 누르는 시점에 컴퓨터는 무엇을 냈는지?  
컴퓨터 → 바위 : '0', 가위 : '-142px', 보: '-284px'

```javascript
var left = 0;
var dictionary = {
    바위 : '0',
    가위 : '-142px',
    보 : '-284px'
};

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

document.querySelectorAll('.btn').forEach(function(btn){
    btn.addEventListener('click', function() {
        console.log(this.textContent, left);    //left는 컴퓨터가 뭘 냈는지
    });
});
```

