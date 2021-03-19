# 딕셔너리 자료구조

가위, 바위, 보 버튼을 누르는 시점에 컴퓨터는 무엇을 냈는지?  
컴퓨터 → 0은 바위, -142px은 가위, -284px은 보

```javascript
document.querySelectorAll('.btn').forEach(function(btn){
    btn.addEventListener('click', function() {
        console.log(this.textContent, left);    //left는 컴퓨터가 뭘 냈는지
    });
});
```

