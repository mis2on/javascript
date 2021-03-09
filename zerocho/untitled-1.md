# window 객체

window 브라우저가 제공하는 객체  
window 객체안에 화면을 표시하는 document가 들어있다.   
window는 브라우저 전체  
document는 페이지\(탭\)

![](../.gitbook/assets/image%20%2816%29.png)

![](../.gitbook/assets/image%20%2815%29.png)

```javascript
window.open() : 새창열
open()    //window 생략가능 

window.alert('경고창') : 경고창
alert('경고창')    //window 생략가능

1ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ
var name = '몽실'
window.name
"몽실" 

function 반복(반복횟수) {
    console.log('*'.repeat(반복횟수))
}
반복(5)
*****
반복(10)
**********

function 기억하세요(){
    var 몸무게 = 70;
}
window.무게
undefined    //함수 안

```



