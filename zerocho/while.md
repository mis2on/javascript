# 반복문\(while\)

`while (조건) {  
 조건이 참인 동안 반복할 일   
}`

```javascript
var result = 0
while(result < 100) {
    console.log(result)
    result = result + 1
}
1
2
3
4
.
.
.
100    //반복문 멈춤

100 < 100
false
```

```javascript
var num = 0    //실행순서1
while(num < 5) {    //실행순서2, 실행순서5(조건과 비교해 false로 반복문을 벗어남)
    console.log('딸기가 좋아')    //실행순서3
    num = num + 10;    //실행순서4
}
'망고가 좋아'    //6
```



