# indexOf & 숫자야구 구현

배열.indexOf\(값\) : 값의 위치를 알 수 있다. 없으면 -1

```javascript
[4, 8, 5, 9]
숫자배열.indexOf(5) //숫자배열안에서 5가 어디에 있나 찾음
2
숫자배열.indexOf(4)
0
숫자배열.indexOf(3) //숫자배열안에 3이 없기 때문에 -1을 반환
-1
```

```javascript
var 바디 = document.body;

var 숫자후보 = [1,2,3,4,5,6,7,8,9];
var 숫자배열 = [];
for(var i = 0; i < 4; i += 1) {
    var 뽑은것 = 숫자후보.splice(Math.floor(Math.random() * (9 - i)), 1)[0];
    숫자배열.push(뽑은것);
}
console.log(숫자배열);

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
    if(답 === 숫자배열.join('')) {//답이 맞으면
        결과.textContent = '홈런';
        입력창.value = '';
        입력창.focus();
        //답이 맞으면 새로운 문제를 다시
        숫자후보 = [1,2,3,4,5,6,7,8,9];
        숫자배열 = [];
        for(var i = 0; i < 4; i += 1) {
            var 뽑은것 = 숫자후보.splice(Math.floor(Math.random() * (9 - i)), 1)[0];
            숫자배열.push(뽑은것);
        }
        console.log(숫자배열);

    } else {//답이 틀리면
        var 답배열 = 답.split('');
        var 스트라이크 = 0;
        var 볼 = 0;
        for(var i = 0; i < 3; i += 1) {
            if(답배열[i] === 숫자배열[i]) {//같은위치에 같은값이 있는지 확인
                스트라이크 += 1;
            } else if (숫자배열.indexOf(답배열[i]) > -1) { //같은위치가 아닌 같은값만 확인
                볼 += 1;
            }
        }
        결과.textContent = 스트라이크 + '스트라이크' + 볼 + '볼입니다.';
        입력창 = '';
        입력창.focus();
    }
});
```

## 10회 제한 추가하기

```javascript
var 바디 = document.body;

var 숫자후보 = [1,2,3,4,5,6,7,8,9];
var 숫자배열 = [];
for(var i = 0; i < 4; i += 1) {
    var 뽑은것 = 숫자후보.splice(Math.floor(Math.random() * (9 - i)), 1)[0];
    숫자배열.push(뽑은것);
}
console.log(숫자배열);

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
    if(답 === 숫자배열.join('')) {//답이 맞으면
        결과.textContent = '홈런';
        입력창.value = '';
        입력창.focus();
        //답이 맞으면 새로운 문제를 다시
        숫자후보 = [1,2,3,4,5,6,7,8,9];
        숫자배열 = [];
        for(var i = 0; i < 4; i += 1) {
            var 뽑은것 = 숫자후보.splice(Math.floor(Math.random() * (9 - i)), 1)[0];
            숫자배열.push(뽑은것);
        }
        틀린횟수 = 0;   //문제를 맞췄을때 틀린횟수를 초기화
    } else {//답이 틀리면
        var 답배열 = 답.split('');
        var 스트라이크 = 0;
        var 볼 = 0;
        틀린횟수 += 1;
        if(틀린횟수 > 10) {
            결과.textContent = '10번 넘게 틀려서 실패! 답은' + 숫자배열.join('') + '였습니다.'; //10번이상 틀리면 답을 공개
            입력창.value = '';
            입력창.focus();
            숫자후보 = [1,2,3,4,5,6,7,8,9];
            숫자배열 = [];
            for(var i = 0; i < 4; i += 1) {
                var 뽑은것 = 숫자후보.splice(Math.floor(Math.random() * (9 - i)), 1)[0];
                숫자배열.push(뽑은것);
            }
            틀린횟수 = 0;
        }
        console.log('답이틀리면', 답배열);
        for(var i = 0; i < 3; i += 1) {
            if(Number(답배열[i]) === 숫자배열[i]) {//같은위치에 같은값이 있는지 확인
                console.log('같은자리?');
                스트라이크 += 1;
            } else if (숫자배열.indexOf(답배열[i]) > -1) { //같은위치가 아닌 같은값만 확인
                console.log('겹치는 숫자?');
                볼 += 1;
            }
        }
        결과.textContent = 스트라이크 + '스트라이크 ' + 볼 + '볼입니다.';
        입력창.value = '';
        입력창.focus();
    }
});
```

