# 별찍기\(반복문 연습\)

## 별 더하

```javascript
for(var star = 1; star <= 5; star += 1) {
    console.log('*'.repeat(star))
}

//결과값
*
**
***
****
*****
```

star += 1  
star = star + 1

## 별 빼

```javascript
for(var star = 5; star >= 1; star -= 1) {
    console.log('*'.repeat(star))
}

//결과값
*****
****
***
**
*
```

star -= 1  
star = star - 1

