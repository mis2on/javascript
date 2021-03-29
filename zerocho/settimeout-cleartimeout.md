# setTimeout, clearTimeout

clearInterval로 setInterval로 멈춘다.

```javascript
var 이미지좌표 = 0;
var 가위바위보 = {
    바위: '0',
    가위: '-142px',
    보: '-284px'
};
console.log(Object.entries(가위바위보));
function 컴퓨터의선택(이미지좌표) {
    return Object.entries(가위바위보).find(function(y){
        console.log(y);
        return y[1] === 이미지좌표;
    })[0];
} 

var 인터벌;
function 인터벌메이커(){
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
};


//clearInterval과 setInterval을 반복
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
        }, 1000);
        var 나의선택 = this.textContent;
        console.log(나의선택, 컴퓨터의선택(이미지좌표));
        if(나의선택 === '가위') {
            if(컴퓨터의선택(이미지좌표) === '가위') {
                console.log('비겼습니다.');
            } else if(컴퓨터의선택(이미지좌표) === '바위') {
                console.log('졌습니다ㅠㅠ');
            } else {
                console.log('이겼습니다.');
            }
        } else if(나의선택 === '바위') {
            if(컴퓨터의선택(이미지좌표) === '가위') {
                console.log('이겼습니다.');
            } else if(컴퓨터의선택(이미지좌표) === '바위') {
                console.log('비겼습니다.');
            } else { 
                console.log('졌습니다ㅠㅠ');
            }
        } else {
            if(컴퓨터의선택(이미지좌표) === '가위') {
                console.log('졌습니다ㅠㅠ');
            } else if(컴퓨터의선택(이미지좌표) === '바위') {
                console.log('이겼습니다.');
            } else {
                console.log('비겼습니다.');
            }
        }
    });
})

```

