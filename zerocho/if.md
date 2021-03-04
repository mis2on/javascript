# 조건문\(if\)

`if (조건) {       
 조건이 참일 때  
} else {  
 조건이 거짓일   
}`

```javascript
if(5 * 5 === prompt('답?')) {
    '딩동댕'
} else {
    '땡'
} 
```

![](../.gitbook/assets/image%20%281%29.png)

![](../.gitbook/assets/image%20%286%29.png)

5 \* 5는 25가 맞는데 "땡"???? 이유는 숫자25와 prompt로 입력받은 값은 문자데이터 "25"를 비교했기 때문  
문자열데이터"25"를 number 함수를 이용해 숫자데이로 변경해 주어야 한다.

`prompt 함수 : 사용자로부터 입력받은 값. 문자데이터를 입력받을 수 있다.  
number 함수 : 문자열을 숫로 변환하는 함수.`

```javascript
var result = prompt('답?')
    if(5 * 5 === Number(result)) {
        '딩동댕'
    } else {
        '땡'
    }
"딩동댕"
```

