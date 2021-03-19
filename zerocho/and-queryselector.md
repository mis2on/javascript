# 로또추첨기 마무리 & querySelector

공색상  
1번 ~ 10번 빨간색  
11번 ~ 20번 주황색  
21번 ~ 30번 노랑색  
31번 ~ 40번 파랑색  
41번 ~ 50번 초록색

```javascript
var 배경색;
    if(숫자 <= 10) {    //10 같거나 작은수를 걸러서 배경색을 변경
        배경색 = 'red';
    } else if(숫자 <= 20) {
        배경색 = 'orange';
    } else if(숫자 <= 30) {
        배경색 = 'yellow';
    } else if(숫자 <= 40) {
        배경색 = 'blue';
    } else {
        배경색 = 'green';
    }
    공.style.background = '배경색';
```

