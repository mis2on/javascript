# JS로 CSS 조작하기

1초마다 1개씩 번호가 나옴

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


    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[0];
        결과창.appendChild(공);
    }, 1000);    //1000밀리초 = 1초
    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[1];
        결과창.appendChild(공);
    }, 2000)
    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[2];
        결과창.appendChild(공);
    }, 3000)
    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[3];
        결과창.appendChild(공);
    }, 4000)
    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[4];
        결과창.appendChild(공);
    }, 5000)
    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[5];
        결과창.appendChild(공);
    }, 6000)


    setTimeout(function 비동콜백함수(){
    var 보너스칸 = document.getElementsByClassName('보너스')[0];    //class로 찾아 선택
        var 보너스공 = document.createElement('div');
        보너스공.textContent = 보너스;
        보너스칸.appendChild(보너스공);
    }, 7000);
```

## JS로 CSS 조자

```javascript
공.style.display = 'inline-block';
공.style.border = '1px solid black';
공.style.borderRadius = '50%';
공.style.width = '50px';
공.style.height = '50px';
공.style.textAlign = 'center';
공.style.lineHeight = '50px';
```

