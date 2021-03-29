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

