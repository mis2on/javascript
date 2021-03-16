# e.target과 parentNode

## e.target === 클릭된 애

클릭한 칸 td는 e.target

![](../.gitbook/assets/image%20%2830%29.png)

## e.target.parentNode === 클릭된 애 부모 태그

클릭한 td의 부모 tr은 e.target.parentNode

![](../.gitbook/assets/image%20%2829%29.png)

그렇다면 table 전체는?? e.target.parentNode.parentNode  
자식은? e.target.children

```javascript
var 바디 = document.body;
var 테이블 = document.createElement('table');
var 줄들 = [];
var 칸들 = [];

var 비동기콜백 = function(이벤트) {
    console.log(이벤트.target);    //칸
    console.log(이벤트.target.parentNode);    //줄
    console.log(이벤트.target.parentNode.parentNode);   //테이블

    var 몇줄 = 줄들.indexOf(이벤트.target.parentNode);
    console.log();
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

