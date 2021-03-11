# split & join

```javascript
var 바디 = document.body;

var 숫자후보 = [1,2,3,4,5,6,7,8,9];
var 숫자배열 = [];

for(var i = 0; i < 4; i += 1) {
    var 뽑은것 = 숫자후보.splice(Math.floor(Math.random() * (9 - i)), 1)[0];
    숫자배열.push(뽑은것);
}
// console.log(숫자배열);

var 결과 = document.createElement('h1');
바디.append(결과);
var 폼 = document.createElement('form');
document.body.append(폼);
var 입력창 = document.createElement('input');
입력창.maxLength = 4;
폼.append(입력창);
var 버튼 = document.createElement('button');
버튼.textContent = '입력!';
폼.append(버튼);

폼.addEventListener('submit', function 비동기(e) {//엔터를 쳤을 때
    e.preventDefault();
    var 답 = 입력창.value;
    console.log(답, 숫자배열, 답 === 숫자배열);
    if(답 === 숫자배열) {//답이 맞으면

    } else {//답이 틀리면

    }
});
```

```javascript
var 숫자배열 = [2, 8, 6, 9];
String(숫자배열[0]) + String(숫자배열[1]) + String(숫자배열[2]) + String(숫자배열[3])
"2869"
숫자배열.join('');    //인자로 빈문자열을 넣으면
"2869"
숫자배열.join(',');    //인자로 ,를 넣으면
"2,8,6,9"
```

문자.split\(구분자\) -&gt; 배열  
숫자.join\(구분자\) -&gt; 문자

