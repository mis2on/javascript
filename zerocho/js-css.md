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

## JS로 CSS 조

```javascript
공.style.display = 'inline-block';
공.style.border = '1px solid black';
공.style.borderRadius = '50%';
공.style.width = '50px';
공.style.height = '50px';
공.style.textAlign = 'center';
공.style.lineHeight = '50px';
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
    
   
    setTimeout(function 비동콜백함수(){
        var 결과창 = document.getElementById('결과창'); //id로 찾아 선택
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[0];
        공.style.display = 'inline-block';
        공.style.border = '1px solid black';
        공.style.borderRadius = '50%';
        공.style.width = '50px';
        공.style.height = '50px';
        공.style.textAlign = 'center';
        공.style.lineHeight = '50px';
        결과창.appendChild(공);
    }, 1000);    //1000밀리초 = 1초
    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[1];
        공.style.display = 'inline-block';
        공.style.border = '1px solid black';
        공.style.borderRadius = '50%';
        공.style.width = '50px';
        공.style.height = '50px';
        공.style.textAlign = 'center';
        공.style.lineHeight = '50px';
        결과창.appendChild(공);
    }, 2000)
    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[2];
        공.style.display = 'inline-block';
        공.style.border = '1px solid black';
        공.style.borderRadius = '50%';
        공.style.width = '50px';
        공.style.height = '50px';
        공.style.textAlign = 'center';
        공.style.lineHeight = '50px';
        결과창.appendChild(공);
    }, 3000)
    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[3];
        공.style.display = 'inline-block';
        공.style.border = '1px solid black';
        공.style.borderRadius = '50%';
        공.style.width = '50px';
        공.style.height = '50px';
        공.style.textAlign = 'center';
        공.style.lineHeight = '50px';
        결과창.appendChild(공);
    }, 4000)
    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[4];
        공.style.display = 'inline-block';
        공.style.border = '1px solid black';
        공.style.borderRadius = '50%';
        공.style.width = '50px';
        공.style.height = '50px';
        공.style.textAlign = 'center';
        공.style.lineHeight = '50px';
        결과창.appendChild(공);
    }, 5000)
    setTimeout(function 비동콜백함수(){
        var 공 = document.createElement('div');
        공.textContent = 당첨숫자들[5];
        공.style.display = 'inline-block';
        공.style.border = '1px solid black';
        공.style.borderRadius = '50%';
        공.style.width = '50px';
        공.style.height = '50px';
        공.style.textAlign = 'center';
        공.style.lineHeight = '50px';
        결과창.appendChild(공);
    }, 6000)


    setTimeout(function 비동기콜백함수() {
        var 보너스칸 = document.getElementsByClassName('보너스')[0];    //class로 찾아 선택
        var 보너스공 = document.createElement('div');
        보너스공.textContent = 보너스;
        보너스칸.appendChild(보너스공);
        보너스공.style.display = 'inline-block';
        보너스공.style.border = '1px solid black';
        보너스공.style.borderRadius = '50%';
        보너스공.style.width = '50px';
        보너스공.style.height = '50px';
        보너스공.style.textAlign = 'center';
        보너스공.style.lineHeight = '50px';
    }, 7000);
    

//↑ 반복이 너무 많아... 함수를 만들어 줄여볼까?

function 공색칠하기(숫자) {
        공.textContent = 당첨숫자들[숫];
        공.style.display = 'inline-block';
        공.style.border = '1px solid black';
        공.style.borderRadius = '50%';
        공.style.width = '50px';
        공.style.height = '50px';
        공.style.textAlign = 'center';
        공.style.lineHeight = '50px';
        결과창.appendChild(공);
}

```

## 함수 만들어 줄여보기

function 공색칠하기 함수를 만들어 반복되는 코드를 줄이기

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
    

function 공색칠하기(숫자) {
    var 결과창 = document.getElementById('결과창');    //id로 찾아 선택
    var 공 = document.createElement('div');
    공.textContent = 당첨숫자들[숫자];
    공.style.display = 'inline-block';
    공.style.border = '1px solid black';
    공.style.borderRadius = '50%';
    공.style.width = '50px';
    공.style.height = '50px';
    공.style.textAlign = 'center';
    공.style.lineHeight = '50px';
    결과창.appendChild(공);
}

    setTimeout(function 비동콜백함수(){
        공색칠하기(0);
    }, 1000);    //1000밀리초 = 1초
    setTimeout(function 비동콜백함수(){
        공색칠하기(1);
    }, 2000)
    setTimeout(function 비동콜백함수(){
        공색칠하기(2);
    }, 3000)
    setTimeout(function 비동콜백함수(){
        공색칠하기(3);
    }, 4000)
    setTimeout(function 비동콜백함수(){
        공색칠하기(4);
    }, 5000)
    setTimeout(function 비동콜백함수(){
        공색칠하기(5);
    }, 6000)


    setTimeout(function 비동기콜백함수() {
        var 보너스칸 = document.getElementsByClassName('보너스')[0];    //class로 찾아 선택
        var 보너스공 = document.createElement('div');
        보너스공.textContent = 보너스;
        보너스칸.appendChild(보너스공);
        보너스공.style.display = 'inline-block';
        보너스공.style.border = '1px solid black';
        보너스공.style.borderRadius = '50%';
        보너스공.style.width = '50px';
        보너스공.style.height = '50px';
        보너스공.style.textAlign = 'center';
        보너스공.style.lineHeight = '50px';
    }, 7000);

```

var 공 = document.createElement\('div'\);  
공.textContent = 당첨숫자들\[숫자\];

var 칸 = document.getElementsByClassName\('보너스'\)\[0\];   
공.textContent = 보너스;

서로 다른 부분은 매개변수로 만들어

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
    공.style.border = '1px solid black';
    공.style.borderRadius = '50%';
    공.style.width = '50px';
    공.style.height = '50px';
    공.style.textAlign = 'center';
    공.style.lineHeight = '50px';
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
        var 칸 = document.getElementsByClassName('div')[0];
        공색칠하기(보너스, 칸);
    }, 7000);

```



