# 배열 map 메서드

## map

forEach 대신 map을 사

```javascript
[undefined, undefined, undefined];
[1, 2, 3];
//mapping, 맵핑

필.map(function(요소, 인덱스) {
    return 인덱스 + 1;
});
console.log(필);
```

```javascript
var 맵 = 필.map(function(요소, 인덱스){
return 1;
});
console.log(맵);
(45) [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]
```

