# 로또추첨기 마무리 & querySelector

공색상  
1번 ~ 10번 빨간색  
11번 ~ 20번 주황색  
21번 ~ 30번 노랑색  
31번 ~ 40번 파랑색  
41번 ~ 50번 초록색 

```javascript
    var 테두리색;
    if(숫자 <= 10) {    //10 같거나 작은수를 걸러서 테두리을 변경
        테두리색 = 'red';
    } else if(숫자 <= 20) {
        테두리색 = 'orange';
    } else if(숫자 <= 30) {
        테두리색 = 'yellow';
    } else if(숫자 <= 40) {
        테두리색 = 'blue';
    } else {
        테두리색 = 'green';
    }
    공.style.borderColor = 테두리색;
```

```javascript
var 후보군 = Array(45)
  .fill()
  .map(function(요소, 인덱스) {
    return 인덱스 + 1;
});
console.log(후보군);

var 셔플 = [];
while(후보군.length > 0) {
  var 이동값 = 후보군.splice(Math.floor(Math.random() * 후보군.length), 1)[0];
  셔플.push(이동값);
}
console.log(셔플);
var 보너스 = 셔플[셔플.length - 1]; //셔플 중 마지막자리 숫자 가져오기
var 당첨숫자들 = 셔플.slice(0, 6);
console.log('당첨숫자들', 당첨숫자들.sort(function(b, c) {
    return c - b; }), '보너스', 보너스);
    
var 결과창 = document.getElementById('결과창');    //id로 찾아 선택

function 공색칠하기(숫자, 결과창) {
    var 공 = document.createElement('div');
    공.textContent = 숫자;
    공.style.display = 'inline-block';
    공.style.border = '10px solid white';
    공.style.borderRadius = '50%';
    공.style.width = '35px';
    공.style.height = '35px';
    공.style.textAlign = 'center';
    공.style.lineHeight = '35px';
    공.style.marginRight = '10px';
    공.id = '공아이디' + 숫자;
    var 테두리색;
    if(숫자 <= 10) {
        테두리색 = 'red';
    } else if(숫자 <= 20) {
        테두리색 = 'orange';
    } else if(숫자 <= 30) {
        테두리색 = 'yellow';
    } else if(숫자 <= 40) {
        테두리색 = 'blue';
    } else {
        테두리색 = 'green';
    }
    공.style.borderColor = 테두리색;
    결과창.appendChild(공);
}

    setTimeout(function 비동콜백함수(){
        공색칠하기(당첨숫자들[0], 결과창);
    }, 1000);    //1000밀리초 = 1초
    setTimeout(function 비동콜백함수(){
        공색칠하기(당첨숫자들[1], 결과창);
    }, 2000)
    setTimeout(function 비동콜백함수(){
        공색칠하기(당첨숫자들[2], 결과창);
    }, 3000)
    setTimeout(function 비동콜백함수(){
        공색칠하기(당첨숫자들[3], 결과창);
    }, 4000)
    setTimeout(function 비동콜백함수(){
        공색칠하기(당첨숫자들[4], 결과창);
    }, 5000)
    setTimeout(function 비동콜백함수(){
        공색칠하기(당첨숫자들[5], 결과창);
    }, 6000)


    setTimeout(function 비동기콜백함수() {
        var 칸 = document.getElementsByClassName('보너스')[0];
        공색칠하기(보너스, 칸);
    }, 7000);

```

```javascript
공.id = '공아이디' + 숫자;

<div id="공아이디34">34</div>
```

