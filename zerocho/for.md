# 반복문\(for\)

`for (처음; 조건; 실행) {   
 실  
}`

```javascript
for(var a = 0; a < 5; a + 3) {
    console.log('딸기 좋아')
}
```

## for반복문을 while반복문으로 바꾸기 

```javascript
for(var a = 0; a < 5; a + 3) {
    console.log('딸기 좋아')
}

var a = 0;
while(a < 5) {
    console.log('딸기 좋아')
    a = a + 3;
}
```

