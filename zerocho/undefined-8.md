# 구구단 구현

![](../.gitbook/assets/image%20%2814%29.png)

```javascript
Math.random() * 9    //0~9사이
Math.floor(Math.random() * 9)    //0~9사이 소수점내리고 정수값
Math.floor(Math.random() * 9) + 1    //구구단은 0단이 없기 때문에 1을 더해 1단부터!!

var num1 = Math.floor(Math.random() * 9) + 1
var num2 = Math.floor(Math.random() * 9) + 1
var result = num1 * num2
prompt(String(num1) + '곱하기' + String(num2) + '눈?')
 
```

