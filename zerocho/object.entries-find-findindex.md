# Object.entries, find, findIndex

object.entries\(객체\)로 객체를 배열로 바꿀 수 있다.

```javascript
var 컴퓨터의선택 = 0;
var 가위바위보 = {
    바위: '0',
    가위: '-142px',
    보: '-284px'
};
var 가위바위보2 = {
    '0': '바위',
    '-142px': '가위' ,
    '-284px': '보'
};


setInterval(function(){
    if(컴퓨터의선택 === 가위바위보.바위) {
        컴퓨터의선택 =  가위바위보.가위;
    } else if (컴퓨터의선택 === 가위바위보.가위) {
        컴퓨터의선택 = 가위바위보.보;
    } else {
        컴퓨터의선택 = 가위바위보.바위;
    }
    document.querySelector('#computer').style.background = 'url(https://en.pimg.jp/023/182/267/1/23182267.jpg)' + 컴퓨터의선택 + ' 0'; 
}, 100);

document.querySelectorAll('.btn').forEach(function(btn){
    btn.addEventListener('click', function(){
        var 나의선택 = this.textContent;
        console.log(나의선택, 가위바위보2[컴퓨터의선택]);
    });
})

```

![](../.gitbook/assets/image%20%2836%29.png)



```javascript
var 가위바위보 = {
    바위: '0',
    가위: '-142px',
    보: '-284px'
};
var 가위바위보2 = {
    '0': '바위',
    '-142px': '가위' ,
    '-284px': '보'
};

// 100개면.....어떻게 바꿔?
Object.entries(객체)
```

## 배열에서 특정한 값을 찾기 .find

```javascript
Object.entries(가위바위보).find(function(y){
    return y[0] === '바위';
});
//0번째가 바위인것을 찾는다.
```

배열.find는 반복문이지만 원하는 것을 찾으면 \(return이 true\) 멈춘다.

.findIndex 인덱스를 찾아준다

1차원 배열일 때는 indexOf  
2차원 배열일 때는  find, findIndex 를 자주 사용한다.

