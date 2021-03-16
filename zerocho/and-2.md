# 틱택토 순서도 & 화면

틱택토? 두명이 번갈아가며 O, X를 3x3 판에 표기하여 가로,세로, 대각선 놓이도록 하는 놀이.  
순서도를 작성해보자!  


![](../.gitbook/assets/image%20%2826%29.png)

```javascript
var 바디 = document.body;
var 테이블 = document.createElement('table'); 
for(var i = 1; i <= 3; i += 1) {
    var 줄 = document.createElement('tr');
    for(var j = 1; j <= 3; j += 1) {
        var 칸 = document.createElement('td')
        줄.appendChild(칸);
    }
    테이블.appendChild(줄);
}
바디.appendChild(테이블);    //body와 table를 추가
```

append와 appendChild 차이?  
여러가지를 동시에 추가할 수 있느냐 또는 텍스트를 추가할 수 있느냐 등  
append가 더 다재다능



