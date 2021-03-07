# 별찍기\(반복문 연습\)

## 별 더하기

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

## 별 빼기

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

## 문제

```javascript
**********    //10개
********      // 8개
******        // 6개
****          // 4개
**            // 2개

for(var star = 10; star >= 2; star -= 2) {
    console.log('*'.repeat(star))
}
```

