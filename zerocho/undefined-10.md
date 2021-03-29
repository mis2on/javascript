# 변수를 사용해 중복 제거하기

```javascript
document.querySelectorAll('.btn').forEach(function(btn){
    btn.addEventListener('click', function(){
        clearInterval(인터벌);
        setTimeout(function(){
            인터벌메이커();
        }, 5000);
        var 나의선택 = this.textContent;
        if(점수표[나의선택] - 점수표[컴퓨터의선택(이미지좌표)] === 0) {
            승패.textContent = '비겼습니다.';
        } else if(점수표[나의선택] - 점수표[컴퓨터의선택(이미지좌표)] === -1 || 점수표[나의선택] - 점수표[컴퓨터의선택(이미지좌표)] === -2) {
            승패.textContent = '이겼습니다!!';
        } else {
            승패.textContent = '졌습니다ㅠㅠ';
        }
    });
})
```

## 배열.includes로 \|\| 관계를 줄일 수 있다.

```javascript
document.querySelectorAll('.btn').forEach(function(btn){
    btn.addEventListener('click', function(){
        clearInterval(인터벌);
        setTimeout(function(){
            인터벌메이커();
        }, 5000);
        var 나의선택 = this.textContent;
        if(점수표[나의선택] - 점수표[컴퓨터의선택(이미지좌표)] === 0) {
            승패.textContent = '비겼습니다.';
        } else if([-1, -2].includes(점수표[나의선택] - 점수표[컴퓨터의선택(이미지좌표)])) {
            ////점수표[나의선택] - 점수표[컴퓨터의선택(이미지좌표)] === -1 || 점수표[나의선택] - 점수표[컴퓨터의선택(이미지좌표)] === -2
            승패.textContent = '이겼습니다!!';
        } else {
            승패.textContent = '졌습니다ㅠㅠ';
        }
    });
})
```

## 변수를 사용해서 중복되는 것을 제거해야한다.

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
}

인터벌메이커();

var 점수표 = {
    가위: 1,
    바위: 0,
    보: -1
}

document.querySelectorAll('.btn').forEach(function(btn){
    btn.addEventListener('click', function(){
        clearInterval(인터벌);
        setTimeout(function(){
            인터벌메이커();
        }, 5000);
        var 나의선택 = this.textContent;
        var 나의점수 = 점수표[나의선택];
        var 컴퓨터점수 = 점수표[컴퓨터의선택(이미지좌표)];
        if(나의점수 - 컴퓨터점수 === 0) {
            승패.textContent = '비겼습니다.';
        } else if([-1, -2].includes(나의점수 - 컴퓨터점수)) {
            //점수표[나의선택] - 점수표[컴퓨터의선택(이미지좌표)] === -1 || 점수표[나의선택] - 점수표[컴퓨터의선택(이미지좌표)] === -2
            승패.textContent = '이겼습니다!!';
        } else {
            승패.textContent = '졌습니다ㅠㅠ';
        }
    });
})

```

