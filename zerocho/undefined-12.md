# 이차원 배열

배열안에 배열을 넣을 수도 있고, 객체, 함수 등 다양하게 넣을 수 있다.  
이차원배열? 배열안에 배열이 들어있는 것

var 배열 = \[1, 2, 3, 4, 5\];  
var 배열 = \[  
    \[1, 2, 3\],  
    \[4, 5, 6\],  
    \[7, 8, 9\],  
\];

```javascript
var 바디 = document.body;
var 테이블 = document.createElement('table');
var 줄들 = [];
var 칸들 = [];

var 비동기콜백 = function(e) {
    console.log(e.target);
};

for(var i = 1; i <= 3; i += 1) {
    var 줄 = document.createElement('tr');
    줄들.push(줄);
    칸들.push([]);
    for(var j = 1; j <= 3; j += 1) {
        var 칸 = document.createElement('td')
        칸.addEventListener('click', 비동기콜백);
        칸들[i - 1].push(칸);
        줄.appendChild(칸);
    }
    테이블.appendChild(줄);
}
바디.appendChild(테이블);
console.log(줄들, 칸들);
```

