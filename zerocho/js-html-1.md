# JS로 HTML 태그 선택하기

```markup
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <title>로또추첨기</title>
        <style>
            
        </style>
    </head>
    <body>
        <div id="결과창"></div>
        <div class="보너스"></div>
        <script src="로또추첨기.js"></script>
    </body>
</html>
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

for(var i = 0; i < 당첨숫자들.length; i += 1){
    var 공 = document.createElement('div');
    공.textContent = 당첨숫자들[i];
    결과창.appendChild(공);
}

var 보너스칸 = document.getElementsByClassName('보너스')[0];    //class로 찾아 선택
    var 보너스공 = document.createElement('div');
    보너스공.textContent = 보너스;
    보너스칸.appendChild(보너스공);
```

## id로 찾기

.getElementById\('아이디명'\);

## 태그로 찾기

.getElementsByTagName\(\);

## class로 찾기

.getElementsByClassName\('클래스명'\)\[0\];  
class는 여러번 쓰일 수 있기 때문에 뒤에 숫자를 붙여 몇번째 class인지 지정

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

for(var i = 0; i < 당첨숫자들.length; i += 1){
setTimeout(function 콜백함수(){
    var 공 = document.createElement('div');
    공.textContent = 당첨숫자들[i];
    결과창.appendChild(공);
});
}

var 보너스칸 = document.getElementsByClassName('보너스')[0];    //class로 찾아 선택
    var 보너스공 = document.createElement('div');
    보너스공.textContent = 보너스;
    보너스칸.appendChild(보너스공);
```



## setTimeout

