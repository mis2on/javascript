# 구구단 구현

![](../.gitbook/assets/image%20%2814%29.png)

```javascript
Math.random() * 9    //0~9사이
Math.floor(Math.random() * 9)    //0~9사이 소수점내리고 정수값
Math.floor(Math.random() * 9) + 1    //구구단은 0단이 없기 때문에 1을 더해 1단부터!!

var num1 = Math.floor(Math.random() * 9) + 1
var num2 = Math.floor(Math.random() * 9) + 1
var result = num1 * num2
var answer = prompt(String(num1) + ' 곱하기 ' + String(num2) + ' 는?')
if(result === Number(answer)) {
    alert('딩동댕')
} else {
    alert('떙')
}

ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ

while(true) {    //컴퓨터 문제 무한반복 출제
    var num1 = Math.floor(Math.random() * 9) + 1
    var num2 = Math.floor(Math.random() * 9) + 1
    var result = num1 * num2
    var 조건 = true;
    while(조건) {
        var answer = prompt(String(num1) + ' 곱하기 ' + String(num2) + ' 는?')
        if(result === Number(answer)) {
            alert('딩동댕')
            조건 = false;    //답이 맞으면 대답하는 것을 멈추고 새로운 문제
        } else {
            alert('떙')    // 답이 틀렸을 때는 같은문제로 다시 답을 입력해야
        }
    }
}
```

무한반복을 끄고 싶은면 shift + esc를 눌러 크롬 관리자 창에서 현재 탭을 종료한다.

