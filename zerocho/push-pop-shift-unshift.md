# 배열 push pop shift unshift splice

```markup
<!DOCTYPE html>
<html lang="ko">
    <head>
        <meta charset="UTF-8">
        <title>숫자야구</title>
    </head>
    <body>
        <h1>1스트라이크 1볼</h1>
        <form>
            <input type="text">
            <button>버튼</button>
        </form>
        <!-- srcipt -->
        <script src="숫자야구.js"></script>
    </body>
</html>
```

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
입력창.maxLength = 4;    //입력할 수 있는 최대 문자수
폼.append(입력창);
var 버튼 = document.createElement('button');
버튼.textContent = '입력!';
폼.append(버튼);

폼.addEventListener('submit', function 비동기(e) {//엔터를 쳤을 때
    e.preventDefault();
    var 답 = 입력창.value;
    console.log(답);
    ㅑ==
});
```

그룹으로 묶어질 수 있는 것들은 배열이나 객체를 사용  
변수를 너무 많이 사용하면 코드가 지저분하기 때문에 배열이나 객체로 묶어주면 좋다.

배열에 값을 제거   
.shift\(\) : 배열의 맨 앞 값을 제거 1 -&gt; 2 -&gt; 3 -&gt; 4  
.pop\(\) : 배열의 맨 끝 값을 제거 9 -&gt; 8 -&gt; 7 -&gt; 6  
  
배열에 값을 추가   
.unshift\(\) : 배열의 맨 앞에 값을 추가  
.push\(\) : 배열의 맨 끝에 값을 추가

.splice\(위치 , 개수\) 위치로부터 개수만큼 배열에서 뽑아 배열로 반  
뽑고 나면 기존의 배열에서 값이 사라진다.  
  


