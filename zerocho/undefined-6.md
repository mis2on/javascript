# 가위바위보 규칙 찾기

```javascript
var 이미지좌표 = 0;
var 가위바위보 = {
    바위: '0',
    가위: '-142px',
    보: '-284px'
};
var 승패 = document.createElement('div');
document.body.append(승패);

console.log(Object.entries(가위바위보));
function 컴퓨터의선택(이미지좌표) {
    return Object.entries(가위바위보).find(function(y){
        console.log(y);
        return y[1] === 이미지좌표;
    })[0];
} 

var 인터벌 = setInterval(function(){
    if(이미지좌표 === 가위바위보.바위) {
        이미지좌표 =  가위바위보.가위;
    } else if (이미지좌표 === 가위바위보.가위) {
        이미지좌표 = 가위바위보.보;
    } else {
        이미지좌표 = 가위바위보.바위;
    }
    document.querySelector('#computer').style.background = 'url(https://en.pimg.jp/023/182/267/1/23182267.jpg)' + 이미지좌표 + ' 0'; 
}, 100);

document.querySelectorAll('.btn').forEach(function(btn){
    btn.addEventListener('click', function(){
        clearInterval(인터벌);
        setTimeout(function(){
            인터벌 = setInterval(function(){
                if(이미지좌표 === 가위바위보.바위) {
                    이미지좌표 =  가위바위보.가위;
                } else if (이미지좌표 === 가위바위보.가위) {
                    이미지좌표 = 가위바위보.보;
                } else {
                    이미지좌표 = 가위바위보.바위;
                }
                document.querySelector('#computer').style.background = 'url(https://en.pimg.jp/023/182/267/1/23182267.jpg)' + 이미지좌표 + ' 0'; 
            }, 100);
        }, 5000);
        var 나의선택 = this.textContent;
        console.log(나의선택, 컴퓨터의선택(이미지좌표));
        if(나의선택 === '가위') {
            if(컴퓨터의선택(이미지좌표) === '가위') {
                승패.textContent = '비겼습니다.';
            } else if(컴퓨터의선택(이미지좌표) === '바위') {
                승패.textContent = '졌습니다ㅠㅠ';
            } else {
                승패.textContent = '이겼습니다.';
            }
        } else if(나의선택 === '바위') {
            if(컴퓨터의선택(이미지좌표) === '가위') {
                승패.textContent = '이겼습니다.';
            } else if(컴퓨터의선택(이미지좌표) === '바위') {
                승패.textContent = '비겼습니다.';
            } else { 
                승패.textContent = '졌습니다ㅠㅠ';
            }
        } else {
            if(컴퓨터의선택(이미지좌표) === '가위') {
                승패.textContent = '졌습니다ㅠㅠ';
            } else if(컴퓨터의선택(이미지좌표) === '바위') {
                승패.textContent = '이겼습니다.';
            } else {
                승패.textContent = '비겼습니다.';
            }
        }
    });
})
```

// 가위: 1, 바위: 0, 보: -1

| 나/컴퓨터 | 가위 | 바 |  |
| :--- | :--- | :--- | :--- |
| 가위 |   1 1 |   1 0 |   1 -1 |
| 바 |   0 1 |   0 0 |   0 -1 |
| 보 | -1 1 | -1 0 | -1 -1 |

